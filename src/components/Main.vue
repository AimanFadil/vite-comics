<script>
export default {
  name: 'Main',
  data() {
    return {
      informazioni: [
        {
          img: '../assets/img/buy-comics-digital-comics.png',
          text: 'DIGITAL COMICS'
        },
        {
          img: '../assets/img/buy-comics-merchandise.png',
          text: 'DC MERCHANDISE'
        },
        {
          img: '../assets/img/buy-comics-shop-locator.png',
          text: 'SUBSCRIPTION'
        },
        {
          img: '../assets/img/buy-comics-subscriptions.png',
          text: 'COMIC SHOP LOCATOR'
        },
        {
          img: '../assets/img/buy-dc-power-visa.png',
          text: 'DC POWER VISA'
        },
      ]
    }
  }
}
</script>
<template lang="">
  <main>
    <div class="cards">
      <div class="textWhite">-- > CONTENT GO HERE</div>
    </div>
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
    text-align: left;
  }
}

.center {
  display: flex;
  justify-content: space-around;
  background-color: rgba(2, 130, 249, 255);
  height: 200px;

  .info {
    display: flex;
    flex-direction: row;

    li {
      list-style: none;
      padding: 50px;
      color: white;
    }

  }
}
</style>