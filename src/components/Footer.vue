<script>
export default {
  name: 'Footer',
  data() {
    return {
      elenco: [
        {
          text: 'DC COMICS',
          attivo: true
        },
        {
          text: 'CHARACTERS',
          attivo: false
        },
        {
          text: 'COMICS',
          attivo: false
        },
        {
          text: 'MOVIES',
          attivo: false
        },
        {
          text: 'TV',
          attivo: false
        },
        {
          text: 'GAMES',
          attivo: false
        },
        {
          text: 'VIDOES',
          attivo: false
        },
        {
          text: 'VIDEOS',
          attivo: false
        },
        {
          text: 'NEWS',
          attivo: false
        },
        {
          text: 'SHOP',
          attivo: true
        },
        {
          text: 'SHOP DC',
          attivo: false
        },
        {
          text: 'SHOP DC Collectibles',
          attivo: false
        },
        {
          text: 'DC',
          attivo: true
        },
        {
          text: 'Terms Of Use',
          attivo: false
        },
        {
          text: 'Privacy policy (New)',
          attivo: false
        },
        {
          text: 'Ad choice',
          attivo: false
        },
        {
          text: 'Advertising',
          attivo: false
        },
        {
          text: 'Jobs',
          attivo: false
        },
        {
          text: 'Subscriptions',
          attivo: false
        },
        {
          text: 'Talent Workshops',
          attivo: false
        },
        {
          text: 'CPSC Certificates',
          attivo: false
        },
        {
          text: 'Ratings',
          attivo: false
        },
        {
          text: 'Shop Help',
          attivo: false
        },
        {
          text: 'Contact Us',
          attivo: false
        },
        {
          text: 'Sites',
          attivo: true
        },
        {
          text: 'DC',
          attivo: false
        },
        {
          text: 'MAD Magazine',
          attivo: false
        },
        {
          text: 'Terms Of Use',
          attivo: false
        },
        {
          text: 'DC Kids',
          attivo: false
        },
        {
          text: 'DC Universe',
          attivo: false
        },
        {
          text: 'DC Power Visa',
          attivo: false
        },
      ]

    }
  }
}
</script>
<template lang="">
  <div>
    <footer>
      <div class="footer1">
        <div class="container">
          <ul class="content">
            <li v-for="testo, index in elenco" :key="index" :class="testo.attivo ? 'active' : ''">{{ testo.text}}</li>
            <img class="img-bg" src="../assets/img/dc-logo-bg.png" >
          </ul>
        </div>
      </div>
      <div class="footer2">
        <div class="container">
          <div class="row">
            <div class="col-6">
              <h3 class="sign">SIGN UP NOW!</h3>
            </div>
            <div class="col-6">
              <h3 class="follow">FOLLOW US</h3>
              <span class="space">
                <img src="../assets/img/footer-facebook.png" >
                <img src="../assets/img/footer-periscope.png" >
                <img src="../assets/img/footer-pinterest.png" >
                <img src="../assets/img/footer-twitter.png" >
                <img src="../assets/img/footer-youtube.png" >
              </span>
            </div>
          </div>
        </div>
      </div>

    </footer>
  </div>
</template>

<style lang="scss" scoped>
.footer1 {
  background-image: url('../assets/img/footer-bg.jpg');

  .img-bg {
    width: 31%;
  }



  .content {
    padding: 50px;
    flex-direction: column;
    display: flex;
    max-height: 420px;
    flex-wrap: wrap;
    margin: 0;
  }

  li {
    color: grey;
    list-style: none;

    &.active {
      color: white;
      font-size: x-large;
    }
  }


}

.footer2 {
  background-color: rgba(48, 48, 48, 255);
  margin-top: 0;
  height: 75px;
  padding: 15px;

  .sign {
    border: rgba(2, 130, 249, 255) solid;
    width: fit-content;
    color: white;
  }

  .follow {
    color: rgba(2, 130, 249, 255);
  }

  h3 {
    display: inline;
  }

  img {
    padding: 10px;
  }
}
</style>