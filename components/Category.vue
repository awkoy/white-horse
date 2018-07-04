<template lang="pug">
  .category
    .container
      .category__heading.row
        a(href="#").category__title {{ name }}
        a(href="#").category__showall Посмотреть все

</template>
<script>
  import data from '@/plugins/data.json'
  export default {
    name: 'hi-category',
    components: {
    },
    data() {
      return {
        name: 'Новости',
        //categories: data[0].categories
      }
    }
  }
</script>
<style lang="sass">
  @import './assets/styles/variables'
  .category
    padding: 24px 0
    background-color: $white
    &__heading
      display: flex
      justify-content: space-between
      align-items: center
      padding: 0 15px 2px 0
      border-bottom: 0.5px solid $hover-bar-border
    &__title, &__showall
      text-transform: uppercase
      cursor: pointer
      text-decoration: none
    &__showall
      font-size: $_11
      color: $grey-all
      transition: all .3s ease-in-out
      position: relative
      padding: 5px 0
      &:hover
        color: $default-green
        &:after
          width: 100%
          opacity: 1
          right: 0
          transition: all .2s ease-in-out
      &:after
        content: ''
        position: absolute
        width: 0
        height: 1px
        bottom: -2px
        right: calc(-50%)
        transform: translateX(0)
        opacity: 0
        background-color: $default-green
        transition: all .5s ease-in-out
    &__title
      font-size: $_17
      color: $h-black
      position: relative
      padding: 0 5px
      transition: all .3s ease-in-out
      transition-delay: .1s
      &:hover
        color: $default-green
        &:before,
        &:after
          transition: all .5s ease-in-out
          opacity: 0
          width: 0
      &:after,
      &:before
        content: ''
        position: absolute
        width: 50%
        height: 1px
        bottom: -3px
        transform: translateX(0)
        opacity: 1
        background-color: $default-green
        transition: all .5s ease-in-out
      &:after
        right: calc(50%)
      &:before
        left: calc(50%)
</style>
