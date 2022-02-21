<template>
  <main>
    <div class="container">
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

      .container{
        height: 100px;
        @include my_flex_row;

      }
    }
</style>