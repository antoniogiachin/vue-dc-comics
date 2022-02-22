<template>

   <ul>            
        <li v-for="(link, index) in links" :key="index">
            <a :href=link.url>
                <img :src=link.src alt="ft-logo">                
            </a>
        </li>

    </ul>

</template>

<script>
export default {
    name: 'socialList',

    props: {

        "links" : Array
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/variables.scss";
ul{

    list-style-type: none;
    @include my_flex_row;
    gap: 20px;

}

</style>