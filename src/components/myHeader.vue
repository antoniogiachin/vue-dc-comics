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
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#" class="active">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                    <li>
                        <a href="#">home</a>
                    </li>
                </ul>

            </div>


        </div>

    </header>
</template>

<script>
export default {
  name: 'myHeader',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "../assets/style/variables.scss";

    header{
        height: 80px;
        @include my_flex_row;
        .container{
            height: 100%;
            @include my_flex_row;
            justify-content: space-between;

            .header-left{
                width: 30%;
                @include my_flex_row;

                .logo{
                    @include my_flex_row;
                    justify-content: center;
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
                height: 100%;
                width: 50%;

                ul{
                    list-style-type: none;
                    height: 100%;
                    @include my_flex_row;
                    justify-content: space-around;

                    li{
                        margin: 0px 10px;

                        a{
                            color: $colorDark;
                            height: 80px;
                            display: inline-block;
                            @include my_flex_row;
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