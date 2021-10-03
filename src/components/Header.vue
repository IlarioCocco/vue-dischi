<template>
    <div class="Header">
        <img class="logo" src="../assets/img/spotify-logo.png" alt="logo Spotify">
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
    background-color: rgb(15, 107, 107);
    height: 80px;
    display: flex;
    align-items: center;

    .logo{
        height: 60px;
    }

}
</style>
