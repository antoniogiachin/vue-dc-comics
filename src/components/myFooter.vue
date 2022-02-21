<template>

  <footer>

    <div class="footer-top">
    
      <div class="container">

        <div class="ft-top-left">

          <div class="col" v-for ="(link, index) in ftLinks" :key="index">
            
            <ul>
              <li class="ft-list-title">{{link.type}}</li>
              <li v-for="(go, indice) in link.listLinks" :key="indice"><a :href="go.url">{{go.text}}</a></li>
            </ul>

          </div>

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
          <ul>
            
            <li v-for="(social, indici) in socialLinks" :key="indici">
              <a :href=social.url>
                <img :src=social.src alt="ft-logo">                
              </a>
            </li>

          </ul>
        </div>


      </div>

    </div>

  </footer>

</template>

<script>
export default {
  name: 'myFooter',

  data(){

    return {

      ftLinks: [

        {

          type: 'dc comics',

          listLinks: [

            {
              text:'characters',

              url: '#'
            },

            {
              text:'comics',

              url: '#'
            },

            {
              text:'movies',

              url: '#'
            },

            {
              text:'tv',

              url: '#'
            },

            {
              text:'games',

              url: '#'
            },

            {
              text:'videos',

              url: '#'
            },

            {
              text:'news',

              url: '#'
            },

          ],

        },

        {

          type: 'shop',

          listLinks: [

            {
              text:'shop DC',

              url: '#'
            },

            {
              text:'shop Dc collectibles',

              url: '#'
            },

          ],

        },

        {

          type: 'dc',

          listLinks: [

            {
              text:'terms of use',

              url: '#'
            },

            {
              text:'privacy policy (new)',

              url: '#'
            },

            {
              text:'shop DC',

              url: '#'
            },

            {
              text:'ad choices',

              url: '#'
            },

            {
              text:'advertising',

              url: '#'
            },

            {
              text:'jobs',

              url: '#'
            },

            {
              text:'subscriptions',

              url: '#'
            },

            {
              text:'talent workshops',

              url: '#'
            },

            {
              text:'CPSC certificates',

              url: '#'
            },

            {
              text:'ratings',

              url: '#'
            },

            {
              text:'shop help',

              url: '#'
            },

            {
              text:'contact us',

              url: '#'
            },

          ],

        },

        {

          type: 'sites',

          listLinks: [

            {
              text:'DC',

              url: '#'
            },

            {
              text:'MAD magazine',

              url: '#'
            },

            {
              text:'Dc kids',

              url: '#'
            },

            {
              text:'Dc universe',

              url: '#'
            },

            {
              text:'cDc power visa',

              url: '#'
            },

          ],

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

          .col{

            ul{
              list-style-type: none;

              .ft-list-title{
                color: $colorWhite;
                text-transform: uppercase;
                margin: 15px 0px;
              }

              li{

                a{
                  color: $colorGrey;
                  text-decoration: none;
                  font-size: 0.8em;
                  text-transform: capitalize;

                  &:hover{
                    color: $colorWhite
                  }
                }

              }
            }
          }

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

        span{
          text-transform: uppercase;
          color: $colorBlue;
          font-weight: bold;
          margin: 0px 30px;
        }

        ul{

          list-style-type: none;
          @include my_flex_row;
          gap: 20px;

          li{
            
            a{
              
            }
          }

        }

      }

    }

</style>