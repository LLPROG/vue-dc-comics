<template>
  <body>
    <HeaderComics />
    <MainComics />
    <FooterComics />
  </body>
</template>

<script>
import HeaderComics from '../src/components/HeaderComics.vue'
import MainComics from '../src/components/MainComics.vue'
import FooterComics from '../src/components/FooterComics.vue'

export default {
  name: 'App',
  components: {
    HeaderComics,
    MainComics,
    FooterComics
  }
}
</script>

<style lang="scss">
@import '../src/assets/style.scss';

</style>
