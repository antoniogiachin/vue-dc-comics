<template>

  <footer>

    <div class="footer-top">
    
      <div class="container">

        <div class="ft-top-left">

          <div class="col">
            
            <ul>
              <li class="ft-list-title">dc comics</li>
              <li><a href="#">home</a></li>
              <li><a href="#">home</a></li>
              <li><a href="#">home</a></li>
              <li><a href="#">home</a></li>
              <li><a href="#">home</a></li>
              <li><a href="#">home</a></li>
              <li><a href="#">home</a></li>
            </ul>

            <ul>
              <li class="ft-list-title">shop</li>
              <li><a href="#">home</a></li>
              <li><a href="#">home</a></li>
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
            
            <li>
              <a href="#">
                <img src="../assets/img/footer-facebook.png" alt="ft-logo">                
              </a>
            </li>

            <li>
              <a href="#">
                <img src="../assets/img/footer-facebook.png" alt="ft-logo">                
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
          margin: 0px 10px;
        }

        ul{

          list-style-type: none;
          @include my_flex_row;
          gap: 10px;

          li{
            
            a{
              
            }
          }

        }

      }

    }

</style>