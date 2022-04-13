<template>
    <header>
        <div class="header">
            <i class="fa-solid fa-bars"></i>
            <img class="logo" src="../assets/img/spotify-logo.png" alt="logo Spotify">
            <h2 class="title">{{title}}</h2>
        </div>
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
    background-color: hsla(196, 53%, 14%, 0.87);
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
    padding: 15px;
}

    .logo {
    max-width: 60px;
    padding: 20px 0px 20px 0px;
    margin-right: 20px;
    display: none;
    }
}
    .fa-bars {
    display: block;
    color: white;
    font-size: 30px;
}


//-------------------RESPONSIVE WITHOUT FRAMEWORK---------------------//
// responsive SMALL SM
@media screen and (min-width: 576px) {
        .header {
        background-color: hsla(195, 53%, 14%, 0.549);
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
        display: block;
        }
    }

        .fa-bars {
        display: none;
        color: white;
        font-size: 30px;
    }
}
</style>

