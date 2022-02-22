<template>

    <div class="col">
        <span class="ft-list-title">{{title}}</span>

        <ul>
            <li v-for="(item, index) in items" :key="index"><a :href="item.url">{{item.text}}</a></li>
        </ul>

    </div>


</template>

<script>
export default {
    name: 'menuFooter',

    props: {

        "title": String,

        "items": Array
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/variables.scss";

.ft-list-title{
    color: $colorWhite;
    text-transform: uppercase;
    font-weight: bold;
    margin: 10px 0px;
    display: inline-block;
}
ul{

    list-style-type: none;


    li{

        a{
            color: $colorLightGrey;
            text-decoration: none;
            font-size: 0.8em;
            text-transform: capitalize;

            &:hover{
            color: $colorWhite
            }
        }

    }
}

</style>