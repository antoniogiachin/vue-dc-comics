<template>

  <footer>

    <div class="footer-top">
    
      <div class="container">

        <div class="ft-top-left">
         
          <menuFooter title="dc comics" :items="menuComics"/>

          <menuFooter title="shop" :items="menuShop"/>

          <menuFooter title="dc" :items="menuDC"/>

          <menuFooter title="sites" :items="menuSites"/>

        </div>

        <div class="ft-top-right">
          <div class="footer-dc-logo">
            <img src="../assets/img/dc-logo-bg.png" alt="footer-logo">
          </div>
        </div>

      </div>

    </div>

    <div class="footer-bottom">

      <div class="container">

        <div class="ft-btn">
          <a href="#">Sign-up now!</a>
        </div>

        <div class="ft-social">

          <span>follow us</span>
          
          <socialList :links="socialLinks"/>

        </div>


      </div>

    </div>

  </footer>

</template>

<script>
import menuFooter from './partials/menuFooter.vue'
import socialList from './partials/socialList.vue'


export default {
  name: 'myFooter',

  components: {
    menuFooter,
    socialList,
  },

  data(){

    return {

      menuComics: [

        {
          text: 'Characters',

          url: '#'

        },

        {
          text: 'Comics',

          url: '#'

        },

        {
          text: 'movies',

          url: '#'

        },

        {
          text: 'tv',

          url: '#'

        },

        {
          text: 'games',

          url: '#'

        },

        {
          text: 'videos',

          url: '#'

        },

        {
          text: 'news',

          url: '#'

        },
      ],  

      menuShop: [

        {
          text : 'shop DC',

          url: '#'

        },

        {
          text : 'shop DC colectibles',

          url: '#'

        },
      ],

      menuDC: [

        {
          text: 'terms of use',

          url: '#'

        },

        {
          text: 'privacy policy (new)',

          url: '#'

        },

        {
          text: 'ad choices',

          url: '#'

        },

        {
          text: 'advertising',

          url: '#'

        },

        {
          text: 'jobs',

          url: '#'

        },

        {
          text: 'sucscriptions',

          url: '#'

        },

        {
          text: 'talent workshops',

          url: '#'

        },

        {
          text: 'CPSC certificates',

          url: '#'

        },

        {
          text: 'ratings',

          url: '#'

        },

        {
          text: 'shop help',

          url: '#'

        },

        {
          text: 'contact us',

          url: '#'

        },

      ], 

      menuSites : [

        {
          text: 'CDC',

          url: '#'

        },

        {
          text: 'MAD magazine',

          url: '#'

        },

        {
          text: 'DC kids',

          url: '#'

        },

        {
          text: 'DC universe',

          url: '#'

        },

        {
          text: 'DC power visa',

          url: '#'

        },

      ],

      socialLinks : [

        {

          src : require('../assets/img/footer-facebook.png'),
          url : '#'

        },

        {

          src : require('../assets/img/footer-twitter.png'),
          url : '#'

        },

        {

          src : require('../assets/img/footer-youtube.png'),
          url : '#'

        },

        {

          src : require('../assets/img/footer-pinterest.png'),
          url : '#'

        },

        {

          src : require('../assets/img/footer-periscope.png'),
          url : '#'

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

    .footer-top{
      width: 100%;
      height: 300px;
      min-height: 300px;
      background-image: url("../assets/img/footer-bg.jpg");
      background-repeat: no-repeat;
      background-size: cover;
      filter: contrast(0.8);
      
      .container{
        height: 100%;
        @include my_flex_row;

        .ft-top-left{
          width: 50%;
          height: 100%;
          @include my_flex_col;
          flex-wrap: wrap;
        }

        .ft-top-right{
          width: 50%;
          height: 100%;
          overflow: hidden;

          .footer-dc-logo{
            width: 100%;
            height: 100%;

            img{
              width: 100%;
              height: 100%;
              object-fit: cover;
              transform: scaleY(1.1);
            }
          }
        }
        
      }
      
    }

    .footer-bottom{

      background-color: $colorDarkGrey;
      height: 80px;

      .container{
        @include my_flex_row;
        height: 100%;
      }

      .ft-btn{
        width: 50%;

        a{
          display: inline-block;
          border: 3px solid $colorBlue;
          padding: 13px;
          color: $colorWhite;
          text-decoration: none;
          text-transform: uppercase;
        }
      }

      .ft-social{

        width: 50%;
        @include my_flex_row;
        justify-content: flex-end;

        span{
          text-transform: uppercase;
          color: $colorBlue;
          font-weight: bold;
          margin: 0px 30px;
        }

      }

    }

</style>