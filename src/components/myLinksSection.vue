<template>
  <section id="my_links">

    <div class="container">

      <a href="#" class="link-card" v-for="(link, index) in links" :key="index">
        <div class="card-img">
          <img :src="link.src" alt="link-img">
        </div>
        <div class="card-txt">
          <span>{{link.text}}</span>
        </div>
      </a>

    </div>

  </section>
</template>

<script>
export default {
  name: 'myLinksSection',

  data(){

    return{

      links : [

        {

          text: 'digital comics',

          src: require('../assets/img/buy-comics-digital-comics.png'),

        },

        {

          text: 'dc merchandise',

          src: require('../assets/img/buy-comics-merchandise.png'),

        },

        {

          text: 'subscription',

          src: require('../assets/img/buy-comics-subscriptions.png'),

        },

        {

          text: 'comic shop locator',

          src: require('../assets/img/buy-comics-shop-locator.png'),

        },

        {

          text: 'dc power visa',

          src: require('../assets/img/buy-dc-power-visa.svg'),

        },

      ],

    }

  },

  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "../assets/style/variables.scss";

    #my_links{
      background-color: $colorBlue;
      
      .container{
        height: 120px;
        @include my_flex_row;
        justify-content: space-around;

        .link-card{
          @include my_flex_row;
          gap: 20px;
          text-transform: uppercase;
          color: $colorWhite;
          font-size: 0.8em;
          text-decoration: none;
        
          .card-img{
            width: 50px;
            height: 50px;

            img{
              width: 100%;
              height: 100%;
              object-fit: contain;
            }
          }

        }

      }

    }
</style>