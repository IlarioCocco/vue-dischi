<template>
  <div id="app">
    <Header title="Spotify"/>
    <Albums/>
  </div>
</template>
// USARE





<script>
// IMPORTARE
// REGISTRARE
import Header from './components/Header.vue';
import Albums from './components/Albums.vue';
export default {
  name: 'App',
  components: {
    Header,
    Albums
  }
}
</script>



// importazione
<style lang="scss">
@import "./assets/scss/common.scss";
@import "~bootstrap/scss/bootstrap";
@import "./assets/scss/variables.scss";
</style>
