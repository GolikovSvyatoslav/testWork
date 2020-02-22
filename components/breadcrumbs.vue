<template>
  <div class="content">
    <div class="breadcrumbs">
      <div class="container breadcrumbs__container">
        <nuxt-link class="breadcrumbs__home" to="/">
          <svg class="breadcrumbs__home-icon">
            <use x="0" y="0" xlink:href="#breadcrumbsHome"/>
          </svg>
        </nuxt-link>
        <p v-for="(item, index) in breadcrumbs" :key="'breadcrumbs-' + item.name">
          <svg class="breadcrumbs__arrow">
            <use x="0" y="0" xlink:href="#breadcrumbsArrow"/>
          </svg>
          <span class="breadcrumbs__link breadcrumbs__link_last" v-if="!item.link">{{ item.name }}</span>
          <nuxt-link class="breadcrumbs__link" v-else :to="item.link">{{ item.name }}</nuxt-link>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "breadcrumbs",
        data() {
            return {
                // Нужно делать через store(сделал статикой, чтоб время не тратить)
                breadcrumbs: [
                    {
                        name: 'Опросы',
                        link: '/'
                    },
                    {
                        name: 'Добавить опрос'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
  .breadcrumbs {
    margin: 25px 0 30px;
    &__container {
      display: flex;
      align-items: center;
    }

    &__arrow {
      margin: 0 4px 0 6px;
      height: 8px;
      width: 15px;
    }
    &__home {
      width: 20px;
      height: 23px;
      &-icon {
        width: 100%;
        height: 100%;
      }
    }
    &__link {
      font-size: 14px;
      color: black;
      &_last {
        color: #7b7b7b;
      }
    }
  }

</style>
