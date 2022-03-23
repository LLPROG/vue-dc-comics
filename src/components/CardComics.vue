<template>
  <div class="card">
    <img :src="img" :alt="serie">
    <p>{{serie}}</p>
  </div>
</template>

<script setup lang="ts">
export default {
  name: 'CardComics',
  props: {
    img: String,
    serie: String
  }
}
</script>

<style scoped lang="scss">
.card {
  width: 200px;
  height: 400px;
  img {
    width: 100%;
  }
}
</style>
