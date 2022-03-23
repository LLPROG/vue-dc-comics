<template>
  <div>
    <div class="top-content">
      <div class="container">
        <div class="cont-list-left">
          <ul class="list-link">
            <li class="title-link">
              {{ listLinks[0].name }}
            </li>
              <ul class="under-list" v-for="link in listLinks[0].link" :key="link.id">
                <li>
                  {{link.text}}
                </li>
              </ul>
          </ul>

          <ul class="list-link bottom-list">
            <li class="title-link">
              {{ listLinks[1].name}}
            </li>
              <ul class="under-list" v-for="link in listLinks[1].link" :key="link.id">
                <li>
                  {{link.text}}
                </li>
              </ul>
          </ul>
        </div>

        <ul class="list-link">
          <li class="title-link">
            {{ listLinks[2].name}}
          </li>
            <ul class="under-list" v-for="link in listLinks[2].link" :key="link.id">
              <li>
                {{link.text}}
              </li>
            </ul>
        </ul>

        <ul class="list-link">
          <li class="title-link">
            {{ listLinks[3].name}}
          </li>
            <ul class="under-list" v-for="link in listLinks[3].link" :key="link.id">
              <li>
                {{link.text}}
              </li>
            </ul>
        </ul>

      </div>
    </div>

    <div class="bottom-content">
      <div class="container">
        <button class="sign">
          sign-up now
        </button>
        <div class="socials">
          <span>
            follow us
          </span>
          <img src="../assets/img/footer-facebook.png" alt="facebook">
          <img src="../assets/img/footer-twitter.png" alt="facebook">
          <img src="../assets/img/footer-youtube.png" alt="facebook">
          <img src="../assets/img/footer-pinterest.png" alt="facebook">
          <img src="../assets/img/footer-periscope.png" alt="facebook">

        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
export default {
  name: 'HeaderComics',
  data () {
    return {
      listLinks: [
        {
          name: 'dc comics',
          link: [
            {
              id: 0,
              text: 'Characters',
              href: '#!'
            },
            {
              id: 1,
              text: 'Comics',
              href: '#!'
            },
            {
              id: 2,
              text: 'Movies',
              href: '#!'
            },
            {
              id: 3,
              text: 'TV',
              href: '#!'
            },
            {
              id: 4,
              text: 'Games',
              href: '#!'
            },
            {
              id: 5,
              text: 'Videos',
              href: '#!'
            },
            {
              id: 6,
              text: 'GamNewses',
              href: '#!'
            }
          ]
        },
        {
          name: 'shop',
          link: [
            {
              id: 0,
              text: 'Shop DC',
              href: '#!'
            },
            {
              id: 1,
              text: 'Shop DC Collectibles',
              href: '#!'
            }
          ]
        },
        {
          name: 'DC',
          link: [
            {
              id: 0,
              text: 'Terms Of Use',
              href: '#!'
            },
            {
              id: 1,
              text: 'Privacy policy (News)',
              href: '#!'
            },
            {
              id: 2,
              text: 'Ad Choices',
              href: '#!'
            },
            {
              id: 3,
              text: 'Advertaising',
              href: '#!'
            },
            {
              id: 4,
              text: 'Jobs',
              href: '#!'
            },
            {
              id: 5,
              text: 'Subscriptions',
              href: '#!'
            },
            {
              id: 6,
              text: 'Talent workshops',
              href: '#!'
            },
            {
              id: 6,
              text: 'CPSC Certificates',
              href: '#!'
            },
            {
              id: 6,
              text: 'ratings',
              href: '#!'
            },
            {
              id: 6,
              text: 'Shop Help',
              href: '#!'
            },
            {
              id: 6,
              text: 'Contact Us',
              href: '#!'
            }
          ]
        },
        {
          name: 'sites',
          link: [
            {
              id: 0,
              text: 'Dc',
              href: '#!'
            },
            {
              id: 1,
              text: 'MAD Magazine',
              href: '#!'
            },
            {
              id: 1,
              text: 'DC Kids',
              href: '#!'
            },
            {
              id: 1,
              text: 'DC Universe',
              href: '#!'
            },
            {
              id: 1,
              text: 'DC Power Visa',
              href: '#!'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/style.scss';
.top-content {
  background-image: url('../assets/img/footer-bg.jpg');
  .container {
    display: flex;
    padding: 2rem 0;

    .list-link {
      color: white;
      list-style: none;
      margin-right: 4rem;

      .title-link {
        margin: 0.5rem 0;
        text-transform: uppercase;
      }

      .under-list {
        list-style: none;
        color: gray;
      }
    }
  }
}

.bottom-content {
  background-color: #303030;
  text-transform: uppercase;

  .container {
    height: 6rem;
    display: flex;
    align-items: center;
    .sign {
      background-color: transparent;
      border-radius: 0;
      border: 3px solid $blue_slice;
      color: white;
      font-weight: bold;
      font-size: 1.3em;
      text-transform: uppercase;
      padding: 1rem;
    }
    .socials {
      font-size: 1.8em;
      display: flex;
      align-items: center;
      margin-left: auto;
      color: $blue_text;
      gap: 1rem;
    }
  }
}

</style>
