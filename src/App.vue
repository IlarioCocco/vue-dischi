<template>
  <div id="app">
    <Header/>
    <MainSectionDischi/>
  </div>
</template>




<script>
import Header from './components/Header.vue'
import MainSectionDischi from './components/MainSectionDischi.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainSectionDischi
  }
}
</script>



// importazione
<style lang="scss">
@import "./assets/scss/common.scss";

</style>
