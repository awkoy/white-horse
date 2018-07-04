<template lang="pug">
  .hover-bar#hover-bar
    .container
      .hover-bar__wrapper.row
        .hover-bar__item.col-2(v-for="(el, index) in publications" :key="index")
          img(:src="el.picture" alt="").hover-bar__img
          .hover-bar__title {{ el.title }}
          .hover-bar__date  {{ el.content }}
</template>
<script>
  import data from '@/plugins/data.json'
  export default {
    name: 'hi-hoverbar',
    created(){
      console.log(data);
    },
    data() {
      return {
        publications: data[0].publications,
      }
    }
  }
</script>

<style lang="sass">
  @import './assets/styles/variables'
  .hover-bar
    height: 244px
    display: block
    position: fixed
    z-index: 2
    left: 0
    right: 0
    top: 142px
    visibility: hidden
    opacity: 0
    transition: all .3s ease-in-out
    transform: translateY(-25px)
    background-color: $white
    &:hover
      transform: translateY(0)
      visibility: visible
      opacity: 1
    .container
      border: 1px solid $hover-bar-border
      border-top: none
    &__wrapper
      max-width: 1000px
      padding: 24px 24px 30px 24px
      margin: auto
      display: flex
    &__item
      margin: auto
      padding: 0
      width: 170px
      max-width: 100%
    &__img
      height: 100px
      width: 170px
      margin-bottom: 16px
    &__title
      margin-bottom: 20px
</style>
