<template>
    <header>

        <div class="container">

            <!-- header left -->
            <div class="header-left">
                <div class="logo">
                    <img src="../assets/img/dc-logo.png" alt="dc-logo-header">
                </div>
            </div>

            <!-- header right -->
            <div class="header-right">

                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :class=" link.current ? 'active' : ''" :href=link.url>{{link.text}}</a>
                    </li>
                </ul>

            </div>


        </div>

    </header>
</template>

<script>
export default {
  name: 'myHeader',

  data(){

      return {

        links: [

            {
                text: 'characters',

                url: '#',

                current: false

            },

            {
                text: 'comics',

                url: '#',

                current: true

            },

            {
                text: 'movies',

                url: '#',

                current: false

            },

            {
                text: 'tv',

                url: '#',

                current: false

            },

            {
                text: 'games',

                url: '#',

                current: false

            },

            {
                text: 'collectibles',

                url: '#',

                current: false

            },

            {
                text: 'videos',

                url: '#',

                current: false

            },

            {
                text: 'fans',

                url: '#',

                current: false

            },

            {
                text: 'news',

                url: '#',

                current: false

            },

            {
                text: 'shop',

                url: '#',

                current: false

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

    header{
        .container{
            @include my_flex_row;
            justify-content: space-between;
            gap: 10px;

            .header-left{
                height: 80px;
                @include my_flex_row;

                .logo{
                    width: 60px;
                    height: 60px;

                    img{
                        width: 100%;
                        height: 100%;
                        object-fit: contain;
                        
                    }
                }
            }

            .header-right{
                text-transform: uppercase;
                height: 80px;

                ul{
                    list-style-type: none;
                    height: 100%;
                    @include my_flex_row;
                    justify-content: space-around;

                    li{
                        margin: 0px 2px;
                        height: 100%;
                        line-height: 80px;

                        a{
                            color: $colorDark;
                            height: 100%;
                            padding: 0px 8px;
                            display: inline-block;
                            text-decoration: none;
                            font-size: 0.8em;
                            border-bottom: 5px solid transparent;

                            &.active, &:hover{
                                border-bottom: 5px solid $colorBlue;
                                color:$colorBlue
                            }
                        }
                    }
                }
            }
        }


    }
</style>