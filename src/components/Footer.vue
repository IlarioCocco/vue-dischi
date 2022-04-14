<template>
  <footer>
      <section>
        <h2 class="titoliFooter">Spotify</h2>
        <img class="logo" src="../assets/img/spotify-logo.png" alt="logo Spotify">
      </section>
  </footer>
</template>



<script>
export default {
    name: 'Footer',
}
</script>



<style lang="scss" scoped>
section {
    background-color: rgba(0, 0, 0, 0.907);
    padding: 40px;
    color: rgb(106, 212, 106);
    display: flex;
    justify-content: center;
}

.titoliFooter{
    display: none;
    justify-content: center;
    font-size: 40px;
}

   .logo {
    max-width: 100px;
    display: block;
}

//-------------------RESPONSIVE WITHOUT FRAMEWORK---------------------//
// responsive SMALL SM
@media screen and (min-width: 576px) {

        .titoliFooter {
        display: block;
        justify-content: center;
        font-size: 40px;
    }
        .logo {
        max-width: 60px;
        padding: 20px 0px 20px 0px;
        display: none;
        }
    }
</style>