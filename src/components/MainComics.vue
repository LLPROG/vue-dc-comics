<template>
<div>
    <div class="top-content">
      <div class="hero">
        <button class="current-series">
          current-series
        </button>
      </div>
      <div class="container">
        <div class="cards-cont">
          <CardComics v-for="item, index in comics" :key="index"
          :img="item.thumb"
          :serie="item.series"
        />
        </div>
        <button class="load-cards">
          load more
        </button>
      </div>
    </div>

    <div class="bottom-content">
      <div class="container">
        <div class="card" v-for="card in cards" :key="card.id">
          <img :src="card.img " :alt="card.text">
          <div class="content-card">
            {{ card.text }}
          </div>
        </div>
      </div>
    </div>

</div>

</template>

<script>
import CardComics from './CardComics.vue'
import img1 from '../assets/img/buy-comics-digital-comics.png'
import img2 from '../assets/img/buy-comics-merchandise.png'
import img3 from '../assets/img/buy-comics-subscriptions.png'
import img4 from '../assets/img/buy-comics-shop-locator.png'
import img5 from '../assets/img/buy-dc-power-visa.svg'

export default {
  name: 'MainComics',
  data () {
    return {
      comics: [
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX',
          price: '$19.99',
          series: 'Action Comics',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01',
          price: '$3.99',
          series: 'American Vampire 1976',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb',
          price: '$16.99',
          series: 'Aquaman',
          type: 'graphic novel'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76',
          price: '$2.99',
          series: 'Batgirl',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$3.99',
          series: 'Batman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$2.99',
          series: 'Batman Beyond',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8',
          price: '$3.99',
          series: 'Batman/Superman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk',
          price: '$4.99',
          series: 'Batman/Superman Annual',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8',
          price: '$5.99',
          series: 'Batman: The Joker War Zone',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY',
          price: '$6.99',
          series: 'Batman: Three Jokers',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX',
          price: '$4.99',
          series: 'Batman: White Knight Presents: Harley Quinn',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq',
          price: '$16.99',
          series: 'Catwoman',
          type: 'graphic novel'
        }
      ],
      cards: [
        {
          id: 0,
          img: img1,
          text: 'digital comics'
        },
        {
          id: 1,
          img: img2,
          text: 'dc merchandise'
        },
        {
          id: 2,
          img: img3,
          text: 'subsciption'
        },
        {
          id: 3,
          img: img4,
          text: 'comics shop locator'
        },
        {
          id: 4,
          img: img5,
          text: 'dc power visa'
        }
      ]
    }
  },
  components: {
    CardComics
  }
}
</script>

<style scoped lang="scss">
@import '../assets/style.scss';
.top-content {
  background-color: #1C1C1C;
  color: white;
  position: relative;

  .hero {
    width: 100%;
    height: 30rem;
    background-image: url('../assets/img/jumbotron.jpg');
  }

  .cards-cont {
      padding: 2rem 0;
      display: flex;
      justify-content: stretch;
      flex-wrap: wrap;
      gap: 1rem;
      margin-right: -1rem;
  }

  .load-cards {
    position: absolute;
    left: 50%;
    bottom: 1rem;
    transform: translate(-50%);
  }
}
.bottom-content {
  background-color: $blue_slice;

  .container {
    display: flex;
    justify-content: space-between;

    .card {
      height: 150px;
      width: 100%;
      display: flex;
      align-items: center;
      padding: 1rem;
      color: white;
      text-transform: uppercase;

      img {
        height: 60%;
        margin-right: 0.5rem;
      }
    }
  }
}

</style>
