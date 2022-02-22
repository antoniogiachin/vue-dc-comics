<template>
    <a :href="href" class="link-card">
        <div class="card-img">
          <img :src="src" alt="link-img">
        </div>
        <div class="card-txt">
          <span>{{text}}</span>
        </div>
    </a>
</template>

<script>
export default {
    name: 'myLinkCard',

    props: {
        
        "href" : String,

        "src" : String,

        "text" : String
    }
}
</script>

<style lang="scss" scoped>

    @import "../../assets/style/variables.scss";

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


</style>>
    


