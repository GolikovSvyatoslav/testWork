<template>
  <div class="content home-page">
    <div class="container">
      <div class="tabs">
        <p class="tabs__item" :class="{'tabs__item_active': activeTabs === tab.id}" v-for="tab in tabs" :key="'tabs-' + tab.id" @click="activeTabs = tab.id">{{ tab.label }}</p>
      </div>
      <div class="tabs-content">
        <div v-if="activeTabs === 1">
          Первый таб
        </div>
        <div v-if="activeTabs === 2">
          Второй таб
        </div>
        <div v-if="activeTabs === 3">
          Третий таб
        </div>
        <div v-if="activeTabs === 4">
          Четвертый таб
        </div>
        <div v-if="activeTabs === 5">
          <answer/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import answer from "../components/answer";
export default {
    name: 'homePage',
    components: {answer},
    data() {
        return {
            activeTabs: 5,
            tabs: [
                {
                    id: 1,
                    label: 'Параметры'
                },
                {
                    id: 2,
                    label: 'Вопросы'
                },
                {
                    id: 3,
                    label: 'Логика'
                },
                {
                    id: 4,
                    label: 'Условия'
                },
                {
                    id: 5,
                    label: 'Респонденты'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
  .tabs {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid #c1e837;
    padding: 0 40px;
    &__item {
      cursor: pointer;
      color: #449755;
      font-size: 16px;
      padding-bottom: 22px;
      &_active {
        color: black;
        border-bottom: 3px solid #c1e837;
        padding-bottom: 19px;
      }
    }
  }
  .tabs-content {
    padding: 0 40px 30px;
    box-shadow: 5px 12px 26px 1px rgba(0, 0, 0, 0.2);
  }
</style>
