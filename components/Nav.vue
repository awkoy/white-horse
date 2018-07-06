<template lang="pug">
  .nav
    .container.nav__wrapper.row
      a(href="/").nav__logo.col-3 HEALTH INFO
      ul.nav__menu.col-6
        li(v-for="(el, index) in categories" :key="index")
          a(href="#").nav__menu__tab {{ el.name }}
          HoverBar
      ul.nav__actions.col-3
        li
          a(href="#").nav__actions__img.hm-search
        li
          a(href="#").nav__actions__img.hm-post
</template>
<script>
  import data from '@/plugins/data.json'
  import HoverBar from '~/components/HoverBar.vue';
  export default {
    name: 'hi-nav',
    components: {
      HoverBar,
    },
    created() {
      console.log(data[0].categories);
    },
    data() {
      return {
        categories: data[0].categories
      }
    }
  }
</script>

<style lang="sass">
  @import './assets/styles/variables'
  .nav
    height: 90px
    box-shadow: 0 2px rgba(0, 0, 0, 0.05)
    position: relative
    z-index: 2
    &__wrapper
      margin: auto
      height: 100%
      padding: 0 12px
      display: flex
      justify-content: space-between
      align-items: center
      align-content: center
    &__logo
      font-size: $_30
      font-weight: bold
      color: $default-green
      text-decoration: none
    &__menu
      height: 100%
      margin: 0
      li
        padding-top: 35px
        height: 100%
        display: inline-block
        margin-right: 20px
        &:last-child
          margin-right: 0
        &:hover  .hover-bar
          transform: translateY(0)
          visibility: visible
          opacity: 1
      &__tab
        color: $text-black
        text-transform: uppercase
        text-decoration: none
        font-size: $_14
        padding: 6px 13px 6px 6px
        transition: .3s
        position: relative
        &:after
          content: ''
          display: block
          position: absolute
          right: 0
          top: 10px
          width: 8px
          height: 8px
          background: url("~assets/images/hm-arrow.svg") center center no-repeat
        &:hover
          color: $default-green
    &__actions
      text-align: right
      margin: 0
      li
        display: inline-block
        height: 30px
        width: 30px
        border-radius: 50%
        transition: .3s
        position: relative
        margin-right: 14px
        cursor: pointer
        &:last-child
          margin-right: 0
        &:hover
          background-color: $social-hover-white
      &__img
        display: inline-block
        position: absolute
        top: 0
        right: 0
        left: 0
        bottom: 0
        margin: auto
        text-decoration: none
        &.hm-search
          width: 15px
          height: 15px
          background: url("~assets/images/hm-search.png") center center no-repeat
          background-size: cover
        &.hm-post
          width: 18px
          height: 15px
          background: url("~assets/images/hm-post.png") center center no-repeat
          background-size: cover
</style>
