<template>
  <div class="select">
    <select @change="$emit('change')" v-model="value" class="select__input">
      <option v-for="option in selectData" :key="'select-' + option.value" :value="option.value">{{ option.label }}</option>
    </select>
    <span v-if="!value" class="select__placeholder">{{ placeholder }}</span>
  </div>
</template>

<script>
    export default {
        props: {
            placeholder: String,
            selectData: Array,
        },
        data() {
            return {
                value: ''
            }
        },
        methods: {
            getData() {
                return this.value
            }
        },
        name: "select"
    }
</script>

<style lang="scss" scoped>
  .select {
    position: relative;
    width: 100%;
    &__placeholder {
      position: absolute;
      left: 20px;
      top: 50%;
      font-size: 16px;
      pointer-events: none;
      transform: translateY(-50%);
    }
    &__input {
      height: 50px;
      width: 100%;
      border-radius: 8px;
      border: 2px solid #e3e3e3;
      position: relative;
      padding: 0 15px;
      font-size: 14px;
      cursor: pointer;
      outline: none;
    }
  }
</style>
