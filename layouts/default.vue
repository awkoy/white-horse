<template lang="pug">
  div
    nuxt
    Header
    Nav
    HoverBar
    Category
</template>
<script>
  import Header from '~/components/Header.vue';
  import Nav from '~/components/Nav.vue';
  import HoverBar from '~/components/HoverBar.vue';
  import Category from '~/components/Category.vue';
  export default {
    components: {
      Header,
      Nav,
      HoverBar,
      Category
    },
  }
</script>
<style lang="sass">
@import './assets/index'
</style>
