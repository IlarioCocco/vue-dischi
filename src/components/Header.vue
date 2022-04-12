<template>
    <header>
        <div class="header">
            <img class="logo" src="../assets/img/spotify-logo.png" alt="logo Spotify">
            <h2 class="title">{{title}}</h2>
        </div>
        <!-- <p class="insert">header</p> -->
    </header>
</template>



<script>
export default {
  name: 'Header',
  props: ['title']
}
</script>



<style scoped lang="scss">
.header {
    background-color: #112e388c;
    display: flex;
    align-items: center;
    justify-content: space-around;
    position: fixed;
    width: 100%;
    margin: auto;
    // border: 5px solid rgba(13, 156, 85, 0.712);

    .title {
    font-size: 40px;
    color: rgb(255, 255, 255);
    display: flex;
}

    .logo {
    max-width: 60px;
    padding: 20px 0px 20px 0px;
    margin-right: 20px;
    }
}

    // .insert {
    //     position: absolute;
    //     top: 0px;
    //     padding: 15px;
    // }
</style>

