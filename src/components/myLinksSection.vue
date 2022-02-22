<template>
  <section id="my_links">

    <div class="container">

      <myLinkCard v-for="(link, index) in links" :key="index" :href="link.href" :src="link.src" :text="link.text"/>

    </div>

  </section>
</template>

<script>
import myLinkCard from './partials/myLinkCard.vue'

export default {
  name: 'myLinksSection',

  components: {
    myLinkCard,
  },

  data(){

    return{

      links : [

        {

          text: 'digital comics',

          src: require('../assets/img/buy-comics-digital-comics.png'),

          href: '#',

        },

        {

          text: 'dc merchandise',

          src: require('../assets/img/buy-comics-merchandise.png'),

          href: '#',

        },

        {

          text: 'subscription',

          src: require('../assets/img/buy-comics-subscriptions.png'),

          href: '#',

        },

        {

          text: 'comic shop locator',

          src: require('../assets/img/buy-comics-shop-locator.png'),

          href: '#',

        },

        {

          text: 'dc power visa',

          src: require('../assets/img/buy-dc-power-visa.svg'),

          href: '#',

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
      }

    }
</style>