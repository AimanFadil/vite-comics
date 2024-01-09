<script>
import ContCards from '../components/ContCards.vue'
export default {
  components: {
    ContCards

  },
  name: 'Main',
  data() {
    return {
      informazioni: [
        {
          img: './public/imgs/buy-comics-digital-comics.png',
          text: 'DIGITAL COMICS'
        },
        {
          img: './public/imgs/buy-comics-merchandise.png',
          text: 'DC MERCHANDISE'
        },
        {
          img: './public/imgs/buy-comics-shop-locator.png',
          text: 'SUBSCRIPTION'
        },
        {
          img: './public/imgs/buy-comics-subscriptions.png',
          text: 'COMIC SHOP LOCATOR'
        },
        {
          img: './public/imgs/buy-dc-power-visa.svg',
          text: 'DC POWER VISA'
        },
      ]
    }
  }
}
</script>
<template lang="">
  <main>
    <ContCards />
    <div class="center">
      <ul class="info">
        <li v-for="infos, index in informazioni" :key="index" ><img :src="infos.img" > <span>{{ infos.text}}</span></li>
      </ul>
    </div>
  </main>
</template>

<style lang="scss" scoped>
.cards {
  background-color: rgba(28, 28, 28, 255);
  height: 200px;

  .textWhite {
    color: white;

  }
}

.center {
  display: flex;
  justify-content: space-around;
  background-color: rgba(2, 130, 249, 255);
  height: 200px;

  img {
    width: 25%;
  }

  .info {
    display: flex;
    flex-direction: row;

    li {
      list-style: none;
      padding-top: 50px;
      color: white;
    }

  }
}
</style>