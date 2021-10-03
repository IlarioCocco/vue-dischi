<template>
  <div id="app">
    <Header/>
    <MainSection/>
    <Album/>
    <Artist/>

  </div>
</template>
// USARE



// IMPORTARE
// REGISTRARE
<script>
import Header from './components/Header.vue'
import MainSection from './components/MainSection.vue'
import Album from './components/Album.vue'
import Artist from './components/Artist.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainSection,
    Album,
    Artist,
  }
}
</script>



// importazione
<style lang="scss">
@import "./assets/scss/common.scss";
</style>
