<template>
  <header>
    <div class="background">
      <div class="container">
        <img src="../assets/img/dc-logo.png" alt="logo dc">
        <ul class="nav-bar">
          <li v-for="link in links" :key="link.id">
            <a :href="link.href">
              {{link.text}}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
export default {
  name: 'HeaderComics',
  data () {
    return {
      links: [
        {
          id: 0,
          href: '#!',
          text: 'characters'
        },
        {
          id: 1,
          href: '#!',
          text: 'comics'
        },
        {
          id: 2,
          href: '#!',
          text: 'movies'
        },
        {
          id: 3,
          href: '#!',
          text: 'tv'
        },
        {
          id: 4,
          href: '#!',
          text: 'games'
        },
        {
          id: 5,
          href: '#!',
          text: 'collectibles'
        },
        {
          id: 6,
          href: '#!',
          text: 'videos'
        },
        {
          id: 7,
          href: '#!',
          text: 'fans'
        },
        {
          id: 8,
          href: '#!',
          text: 'news'
        },
        {
          id: 9,
          href: '#!',
          text: 'shop'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/style.scss';
@import '../assets/partial/_mixin.scss';

header {
  background-color: black;
  padding-top: 2rem;

  .background {
    background-color: white;
    padding: 5px;
    .container {
      display: flex;
      height: 6rem;

      img {
        height: 100%;;
      }

      .nav-bar {
        @include flexBox ($just: space-between);
        margin-left: auto;
        height: 100%;

        li {
          height: 100%;
          display: inline-block;
          list-style: none;
          margin-right: 1rem;

          a {
            display: inline-block;
            text-decoration: none;
            line-height: 6rem;
            color: $black_text;
            text-transform: uppercase;

            &:hover {
              border-bottom: 5px solid $blue_text;
              color: $blue_text;
            }
          }
        }
      }
    }
  }
}

</style>
