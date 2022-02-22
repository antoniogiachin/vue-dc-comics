<template>

  <div class="main-card" >

        <div class="card-img">
          <img :src="thumbs">
        </div>

        <div class="card-text">
          <span>{{series}}</span>
        </div>

    </div>

</template>

<script>
export default {
    name: 'mainCard',

    props: {

        "series": String,

        "thumbs": String

    }
}
</script>

<style lang="scss" scoped>
    @import "../../assets/style/variables.scss";

    .main-card{
        width: calc(100% / 6 - 20px);
        height: 150px;
        margin:  10px;

        .card-img{
        width: 100%;
        height: 70%;
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
        font-size: 0.7em;
        padding: 0px 2px;
        }
    }

</style>