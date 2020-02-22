<template>
  <div class="field">
    <slot name="label"></slot>
    <span class="field__name" v-if="name" :class="'field__label-color-' + nameColor">{{ name }} </span>
    <span v-if="required" class="required">*</span>
    <component :selectData="selectData" @change="changeField" :placeholder="placeholder" :name="name" :value="data" :isForm="true"
               :is="component"></component>
    <svg v-if="icon" @click="clickIcon" class="field__icon" :class="{'field__icon_cp': isClickIcon}"><use x="0" y="0" :xlink:href="'#' + icon" /></svg>
  </div>
</template>

<script>
      import string from "./elements/string";
      import selectField from "./elements/selectField";
      export default {
          components: {selectField, string},
          props: {
              placeholder: String,
              icon: String,
              isClickIcon: Boolean,
              component: String,
              data: [String, Number],
              name: String,
              selectData: Array,
              nameColor: {
                  type: String,
                  default: 'black'
              },
              required: Boolean
          },
          data() {
              return {
                  value: ''
              }
          },
          methods: {
              changeField(data) {
                  this.$emit('change', data)
              },
              clickIcon() {
                  if (this.isClickIcon) {
                      this.$emit('clickIcon', this.value)
                  }
              },
              getData() {
                  return { field: this.field, value: this.value}
              }
          },
          name: "field"
      }
</script>

<style lang="scss" scoped>
    .field {
      position: relative;
      width: 100%;
      display: flex;
      align-items: center;
      margin-bottom: 40px;
      &__name {
        max-width: 240px;
        width: 100%;
        &:first-letter {
          text-transform: uppercase;
        }

      }
      &__input {
        height: 50px;
        width: 100%;
        border-radius: 8px;
        border: 2px solid #e3e3e3;
        position: relative;
        padding: 0 15px;
        font-size: 14px;
        outline: none;
        &_icon {
          padding: 0 50px 0 15px;
        }
      }
      &__icon {
        position: absolute;
        right: 15px;
        top: 50%;
        transform: translateY(-50%);
        max-width: 25px;
        max-height: 22px;
        &_cp {
          cursor: pointer;
        }
      }
    }
</style>
