<template>
  <div id="app">
    <myHeader />
    <myMain />
    <myLinksSection />
    <myFooter />
  </div>
</template>

<script>
import myHeader from './components/myHeader.vue'
import myMain from './components/myMain.vue'
import myLinksSection from './components/myLinksSection.vue'
import myFooter from './components/myFooter.vue'


export default {
  name: 'App',
  components: {
    myHeader,
    myMain,
    myLinksSection,
    myFooter
  }
}
</script>

<style lang="scss">
    @import "./assets/style/variables.scss";
    @import "./assets/style/general.scss";
</style>
