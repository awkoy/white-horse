<template lang="pug">
  .footer
    .container.footer__wrapper.row
      .footer__info.col-5
        .footer__info__logo HEALTH INFO
        .footer__info__subtitle Cпециализированное интернет-издание для врачей и студентов медицинских вузов
        ul.header__social.footer__info__social
          li
            a(href="#").header__social__img.hm-telegram
          li
            a(href="#").header__social__img.hm-pinterest
          li
            a(href="#").header__social__img.hm-instagram
          li
            a(href="#").header__social__img.hm-facebook
      .footer__feedback.col-4
        .footer__feedback__title Обратная связь
        a(href="#").footer__feedback__mail E-mail
        a(href="#").footer__feedback__telegram Telegram
      .footer__subscription.col-3
        .footer__feedback__title Подписка
        .footer__info__subtitle Подпишитесь на наши обновления чтобы получать свежие статьи на почту
        .footer__sender
          input(placeholder="E-mail...").footer__input
          button.footer__button
    .container.row.footer__copyright
      .footer__copyright__title.col-12 © 2018 health info

</template>
<script>
  export default {
    name: 'hi-footer',
  }
</script>
<style lang="sass">
  @import './assets/styles/variables'
  .footer
    padding: 50px 0
    position: relative
    height: 270px
    background-color: $title-black
    &:after
      content: ''
      display: block
      width: 100%
      height: .5px
      background-color: $grey-line
      position: absolute
      bottom: 48px
      left: 0
      right: 0
    &__wrapper
      display: flex
      justify-content: space-between
      margin: auto
      padding: 0 5px
    &__info
      padding: 0
      &__logo
        font-size: $_24
        font-weight: bold
        margin-bottom: 15px
        color: $dark-green
      &__subtitle
        font-size: $_11
        color: $footer-grey
        max-width: 265px
        margin-bottom: 20px
      &__social
        padding: 0
        text-align: left
    &__feedback
      padding: 0
      &__title
        text-transform: uppercase
        font-weight: bold
        color: $footer-grey
        margin-bottom: 15px
      &__mail
        margin-bottom: 15px
        &:before
          background: url("~assets/images/ft-post.png") center center no-repeat
          background-size: cover
      &__telegram
        &:before
          background: url("~assets/images/hm-telegram.png") center center no-repeat
          background-size: cover
      &__mail,
      &__telegram
        font-size: $_11
        color: $footer-grey
        padding: 4px 0 0 34px
        text-decoration: none
        display: block
        position: relative
        &:before
          content: ''
          display: block
          width: 20px
          height: 20px
          position: absolute
          left: 0
          top: 0
    &__subscription
      padding: 0
    &__sender
      display: flex
      align-items: center
    &__input
      width: 229px
      height: 35px
      padding: 0 5px
      background-color: $white
      font-size: $_11
      color: $grey-all
    &__button
      background: $default-green url("~assets/images/ft-arrow.png") center center no-repeat
      background-size: 15px
      height: 35px
      width: 35px
    &__copyright
      height: 48px
      margin: auto
      padding: 0 5px
      position: absolute
      left: 0
      right: 0
      bottom: 0
      &__title
        padding: 0
        display: flex
        justify-content: flex-end
        align-items: center
        font-size: $_11
        color: $copyright-grey
        text-transform: capitalize
</style>
