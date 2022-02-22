<template>
  <main>
    
    <!-- jumbotron -->
    <section id="jumbotron">

    </section>

    <div class="container">

      <div class="current-series"><span>current series</span></div>

      <div class="main-card" v-for="n in 12" :key="n">
        <div class="card-img">
          <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX" alt="main-card-img">
        </div>
        <div class="card-text">
          <span>action comics</span>
        </div>
      </div>


      <button class="load-more">Load More</button>
      
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
        @include my_flex_row;
        flex-wrap: wrap;
        position: relative;
        justify-content: center;
        padding: 50px 0px;

        .current-series{
          display: inline-block;
          position: absolute;
          top: -20px;
          left: 0;
          background-color: $colorBlue;
          text-transform: uppercase;
          color:$colorWhite;
          padding: 5px 20px;
          font-size: 1.2em;
          font-weight: bold;
        }

        .main-card{
          width: calc(100% / 6 - 20px);
          margin: 0px 10px 30px 10px;

          .card-img{
            width: 150px;
            height: 150px;
            margin-bottom: 10px;

            img{
              width: 100%;
              height: 100%;
              object-fit: cover;
              object-position: top;
            }
          }

          .card-text{
            text-transform: uppercase;
            font-size: 0.8em;
          }
        }

        .load-more{
          display: inline-block;
          background-color: $colorBlue;
          border: none;
          color: $colorWhite;
          text-transform: uppercase;
          font-weight: bold;
          padding: 8px 60px;
          margin-top: 30px;
          cursor: pointer;

          &:hover{
            filter: saturate(2);
            transform: scale(1.1);
          }
        }
      }

    }
</style>