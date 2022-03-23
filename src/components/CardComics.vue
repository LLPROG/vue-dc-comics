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
  height: 17rem;
  img {
    width: 100%;
    height: 80%;
    object-fit: cover;
    object-position: top;
  }

  p {
    margin-top: 1.5rem;
  }
}
</style>
