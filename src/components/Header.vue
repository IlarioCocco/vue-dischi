<template>
    <div class="Header">
        <img class="logo" src="../assets/img/spotify-logo.png" alt="logo Spotify">
        <h2>{{title}}</h2>
    </div>
</template>



<script>
export default {
  name: 'Header',
  props: ['title']
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.Header {
    background-color: #2E3A46;
    height: 90px;
    display: flex;
    align-items: center;
    width: 100%;

    .logo {
        height: 60px;
    }

    h2 {
    font-size: 30px;
    color: beige;
    font-weight: 600;
    margin-left: 43%;
    // text-align: center;
}

}


</style>

