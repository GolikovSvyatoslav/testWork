<template>
  <header class="header content">
    <div class="container header__container">
      <string class="header__search" placeholder="Поиск по системе" icon="search"/>
      <div class="header__user">
        <img src="~assets/img/user.png" class="header__user-photo"/>
        <div class="header__user-info">
          <p class="header__user-name">
            Alexander C.
          </p>
          <p class="header__user-position">
            Администратор
          </p>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
    import string from "./elements/string";
    export default {
        name: "headerBase",
        components: {string}
    }
</script>

<style lang="scss" scoped>
  .header {
    padding-top: 25px;
    &__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 65px;
    }
    &__search {
      max-width: 625px;
    }
    &__user {
      display: flex;
      align-items: center;
      &-photo {
        margin-right: 10px;
      }
      &-name {
        font-weight: bold;
        color: black;
        font-size: 14px;
        line-height: 14px;
      }
      &-position {
        color: #747474;
        margin-top: 8px;
        font-size: 14px;
        line-height: 14px;
      }
    }
  }
</style>
