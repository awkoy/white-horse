<template lang="pug">
  .header
    .container.header__wrapper.row
        ul.header__lang.col-6
          li
            a(href="#").header__lang__tab РУС
          li
            a(href="#").header__lang__tab.eng ENG
        ul.header__social.col-6
          li
            a(href="#").header__social__img.hm-telegram
          li
            a(href="#").header__social__img.hm-pinterest
          li
            a(href="#").header__social__img.hm-instagram
          li
            a(href="#").header__social__img.hm-facebook
</template>
<script>
export default {
  name: 'hi-header',
}
</script>

<style lang="sass">
  @import './assets/styles/variables'
  .header
    background-color: $h-black
    max-height: 50px
    padding: 8px 0
    &__wrapper
      padding: 0
      margin: auto
      display: flex
      justify-content: space-between
      align-items: center
      align-content: center
    &__lang,
    &__social
      padding: 0 5px
    &__lang
      li
        display: inline-block
      &__tab
        color: $dark-green
        text-transform: uppercase
        text-decoration: none
        font-size: $_14
        padding: 6px 6px 6px 0
        &.eng
          position: relative
          color: white
          padding-left: 6px
          &:before
            content: ''
            position: absolute
            left: 0
            top: 7px
            width: 1px
            height: 14px
            background-color: $white
    &__social
      text-align: right
      li
        margin-top: 2px
        display: inline-block
        height: 32px
        width: 32px
        border-radius: 50%
        transition: .3s
        position: relative
        margin-right: 14px
        &:last-child
          margin-right: 0
        &:hover
          background-color: $social-hover
      &__img
        display: inline-block
        cursor: pointer
        width: 20px
        height: 20px
        position: absolute
        top: 0
        right: 0
        left: 0
        bottom: 0
        margin: auto
        text-decoration: none
        &.hm-telegram
          background: url("~assets/images/hm-telegram.png") center center no-repeat
          background-size: cover
        &.hm-pinterest
          background: url("~assets/images/hm-pinterest.png") center center no-repeat
          background-size: cover
        &.hm-instagram
          background: url("~assets/images/hm-instagram.png") center center no-repeat
          background-size: cover
        &.hm-facebook
          background: url("~assets/images/hm-facebook.png") center center no-repeat
          background-size: cover
</style>
