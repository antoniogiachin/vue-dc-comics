<template>
  <section id="my_links">

    <div class="container">

      <a href="#" class="link-card">
        <div class="card-img">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="digital-img">
        </div>
        <div class="card-txt">
          <span>digital comics</span>
        </div>
      </a>

      <a href="#" class="link-card">
        <div class="card-img">
          <img src="../assets/img/buy-comics-merchandise.png" alt="digital-img">
        </div>
        <div class="card-txt">
          <span>dc merchandise</span>
        </div>
      </a>

      <a href="#" class="link-card">
        <div class="card-img">
          <img src="../assets/img/buy-comics-subscriptions.png" alt="digital-img">
        </div>
        <div class="card-txt">
          <span>subscription</span>
        </div>
      </a>

      <a href="#" class="link-card">
        <div class="card-img">
          <img src="../assets/img/buy-comics-shop-locator.png" alt="digital-img">
        </div>
        <div class="card-txt">
          <span>comic shop locator</span>
        </div>
      </a>

      <a href="#" class="link-card">
        <div class="card-img">
          <img src="../assets/img/buy-dc-power-visa.svg" alt="digital-img">
        </div>
        <div class="card-txt">
          <span>dc power visa</span>
        </div>
      </a>

    </div>

  </section>
</template>

<script>
export default {
  name: 'myLinksSection',
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