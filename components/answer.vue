<template>
    <section class="answer">
      <h1 class="title">Добавить опрос</h1>
      <div class="answer__form">
        <div v-for="(item, index) in data" :key="'answer-' + item.id + '-' + index" class="answer__form-item">
          <field @change="changeField(item)" :ref="'condition-' + item.id" :name="'Условие ' + (index + 1)" placeholder="Выберите условие" component="selectField" :selectData="selectData"/>
          <div v-if="item.type" class="">
            <field :ref="'condition-element-' + item.id" v-for="index in item.count" :key="'type-' + index" :name="item.label + ' ' + index" :selectData="getSchema(item.type)" :placeholder="'Выберите ' + item.label" component="selectField"/>
          </div>
          <div class="answer__button">
            <button class="button button_success" @click="addElement(item)">Добавить {{ item.label }}</button>
            <button v-if="data.length > 1" class="button button_danger" @click="deleteCondition(item)">Удалить условие</button>
          </div>
        </div>
        <div class="answer__button answer__button_c">
          <button class="button button_success" @click="addData">Добавить условие</button>
        </div>
      </div>
      <div class="answer__button">
        <button class="button button_success" @click="submitData">Протестировать опрос</button>
      </div>
    </section>
</template>

<script>
    import Field from "./field";
    export default {
        name: "answer",
        components: {Field},
        data() {
            return {
                data: [{id: 1, type: false, count: 1, items: [], label: '', name: ''}],
                selectActive: 0,
                selectData:[
                    {
                        value: 1,
                        label: 'Тип карты лояльности',
                        schema: [
                            {
                                value: 1,
                                label: 'Бронза'
                            },
                            {
                                value: 2,
                                label: 'Серебро'
                            },
                            {
                                value: 3,
                                label: 'Золото'
                            }
                        ]
                    },
                    {
                        value: 2,
                        label: 'Статус карты лояльности',
                        schema: [
                            {
                                value: 1,
                                label: 'Активна'
                            },
                            {
                                value: 2,
                                label: 'Не активна'
                            }
                        ]
                    }
                ]
            }
        },
        methods: {
            submitData() {
                // Можно было создать компонент форму у него getData и сделать лучше(но из-за времени не стал), если надо могу скинуть сайт, где делал формы, там намного больше сделано.
                let url = '/opros';
                let dataParams = '';
                this.data.map((item) => {
                    let value = [];
                    this.$refs["condition-element-" + item.id].map((el) => {
                        value.push(el.$children[0].getData());
                    });
                    if (!dataParams) {
                        dataParams += `?${item.name}=${value.join(',')}`;
                    } else {
                        dataParams += `&${item.name}=${value.join(',')}`;
                    }
                })
                if (dataParams) {
                    url += dataParams;
                }
                console.log(`Отправлен запрос по url: ${url}`);

            },
            getSchema(id) {
                // Вытащить данные для select
                return this.selectData.find((item) => item.value === id ).schema;
            },
            changeField(item) {
                // Изменение типа условия, тут зашиты 1,2 , но с условием что это тестовое, а не даные с бэка решил так сделать
                let type = this.$refs['condition-' + item.id][0].$children[0].getData();
                if (type === 1) {
                    item.label = 'тип';
                    item.name = 'type'
                }
                if (type === 2) {
                    item.label = 'статус';
                    item.name = 'status'
                }
                item.type = type;
                item.count = 1;
                this.data = this.data.slice();
            },
            addElement(item) {
                item.count++;
            },
            addData() {
                this.data.push({
                    id: this.data.length + 1,
                    count: 1,
                    items: [],
                    label: '',
                    name: ''
                })
            },
            deleteCondition(item) {
                let data = this.data.filter((element) => {
                    if (element.id !== item.id) {
                        return element
                    }
                })
                if (!data.length) {
                    data = [{id: 1, count: 1, items: [], label: '', name: ''}];
                }
                this.$refs['condition-' + item.id][0].$children[0].$data.value = 0;
                this.data = data;
            }
        }
    }
</script>

<style lang="scss" scoped>
  .button {
    min-width: 162px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 8px;
    cursor: pointer;
    outline: none;
    &_danger {
      color: red;
      border: 2px solid #ffd2d2;
    }
    &_success {
      color: green;
      border: 2px solid #dbf28b;
    }
  }

  .answer {
    &__button {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 30px;
      &_c {
        justify-content: center;
      }
    }
  }

</style>
