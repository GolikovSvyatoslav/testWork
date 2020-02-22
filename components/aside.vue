<template>
    <aside class="aside">
      <div class="d-fc">
        <span class="aside__icon-top"/>
        <div class="aside__menu">
          <nuxt-link exact :to="item.link" v-for="item in menu" :key="'menu-' + item.name" class="aside__menu-item">
            <svg class="aside__menu-icon" :class="{'aside__menu-icon_answer': item.icon === 'answer'}"><use x="0" y="0" :xlink:href="'#' + item.icon" /></svg>
            <p class="aside__menu-name">{{ item.name }}</p>
          </nuxt-link>
        </div>
      </div>
      <img src="~assets/img/answer.png">
    </aside>
</template>

<script>
    export default {
        name: "asideBase",
        data() {
            return {
                menu: [
                    {
                        icon: 'answer',
                        link: '/',
                        name: 'Опросы'
                    },
                    {
                        icon: 'users',
                        link: '/users',
                        name: 'Пользователи'
                    },
                    {
                        icon: 'blackList',
                        link: '/black-list',
                        name: 'Черные списки'
                    },
                    {
                        icon: 'coll',
                        link: '/coll',
                        name: 'Колл-центр'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
  .aside {
    position: fixed;
    width: 175px;
    height: 100%;
    border-right: 1px solid #ededed;
    border-bottom: 1px solid #ededed;
    padding: 25px  10px 34px 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    &__icon-top {
      border-radius: 50%;
      background: #e62101;
      width: 50px;
      height: 50px;
      margin-bottom: 75px;
    }
    &__menu {
      width: 100%;
      &-item {
        width: 100%;
        height: 116px;
        background: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        border-radius: 4px;
        &:hover {
          background: #f7f7f7;
        }
        &_active {
          border: 2px solid #dbf28b;
        }
      }
      &-icon {
        display: block;
        max-width: 50px;
        max-height: 50px;
        &_answer {
          max-width: 39px;
        }
      }
      &-name {
        font-size: 14px;
        color: black;
        margin-top: 10px;
      }
    }
  }
  .aside__menu-item_active {
    .aside__menu-icon {
      filter: drop-shadow(2px 2px 2px black);
    }
    .aside__menu-name {
      color: #dbf28b;
    }
  }
</style>
