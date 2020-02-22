<template>
  <div class="input">
    <label v-if="label" class="input__label">{{label}}</label>
    <input v-model="value" class="input__input" :class="{'input__input_icon': icon}" :placeholder="placeholder">
    <svg v-if="icon" @click="clickIcon" class="input__icon" :class="{'input__icon_cp': isClickIcon}"><use x="0" y="0" :xlink:href="'#' + icon" /></svg>
  </div>
</template>

<script>
    export default {
        props: {
            placeholder: String,
            icon: String,
            isClickIcon: Boolean,
            label: String
        },
        data() {
            return {
                value: ''
            }
        },
        methods: {
            clickIcon() {
                if (this.isClickIcon) {
                    this.$emit('clickIcon', this.value)
                }
            },
            getData() {
                return this.value
            }
        },
        name: "string"
    }
</script>

<style lang="scss" scoped>
  .input {
    position: relative;
    width: 100%;
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
