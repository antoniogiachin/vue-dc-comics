<template>
  <main>
    
    <!-- jumbotron -->
    <section id="jumbotron">

    </section>

    <div class="container">

      <div class="current-series"><span>current series</span></div>

      <p>--> Content goes Here  </p>
    </div>
  </main>
</template>

<script>
export default {
  name: 'myMain',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "../assets/style/variables.scss";

    main{
      background-color: $colorDark;
      color : $colorWhite;
      font-weight: bold;

      #jumbotron{
        min-height: 350px;
        width: 100%;
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: cover;
      }

      .container{
        height: 100px;
        @include my_flex_row;
        position: relative;

        .current-series{
          display: inline-block;
          position: absolute;
          top: -20px;
          background-color: $colorBlue;
          text-transform: uppercase;
          color:$colorWhite;
          padding: 5px 20px;
          font-size: 1.2em;
          font-weight: bold;
        }
      }

    }
</style>