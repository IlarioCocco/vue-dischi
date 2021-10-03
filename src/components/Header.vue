<template>
    <div class="Header">
        <img class="logo" src="../assets/img/spotify-logo.png" alt="logo Spotify">
        <h2>Spotify</h2>
    </div>
</template>



<script>
export default {
  name: 'Header'

 
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.Header {
    background-color: rgb(76, 105, 122);
    height: 90px;
    display: flex;
    align-items: center;

    .logo {
        height: 60px;
    }

    h2 {
       font-size: 30px;
       color: beige;
    }

}

</style>

