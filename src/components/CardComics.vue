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
  width: calc(100% / 6 - 1rem);
  // overflow: hidden;
  img {
    width: 100%;
    height: 60%;
    object-fit: cover;
    object-position: top;
  }

  p {
    margin-top: 2rem;
  }
}
</style>
