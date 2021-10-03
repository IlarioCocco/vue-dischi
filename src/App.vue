<template>
  <div id="app">
    <Header/>
    <MainSection/>
  </div>
</template>




<script>
import Header from './components/Header.vue'
import MainSection from './components/MainSection.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainSection
  }
}
</script>



// importazione
<style lang="scss">
@import "./assets/scss/common.scss";
</style>
