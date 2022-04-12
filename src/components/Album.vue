<template>
    <div>
        <img class="img" :src="albums.poster" :alt="albums.title">
        <div class="titolo">
            <h4 class="album">
                {{albums.title}}
            </h4>
            <p class="artist">{{albums.author}}<br>
                {{albums.year}}
            </p>
        </div>
    </div>
</template>


<script>
export default {
    name: 'Album',
    props: ['album', 'albums']
    // è possibile esportarlo anche come obj
}
</script>


<style lang="scss">
.square {
    background-color: #2762797e;
        padding: 5px 5px 45px 5px;
        display: flex;
        flex-wrap: wrap;
        width: calc(100% / 1 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 53%, 14%, 0.24);

    .img {
        width: 100%;
        padding: 0px 0px 10px 0px; 
        // position: relative;
        // clip-path: inset(0% 0% 0% 0%);
    }

    .titolo {
        text-align: center;
        color: white;
        // border: 5px solid rgba(255, 255, 255, 0.219);
        max-width: 100%;
    }
}

.album {
    font-size: 20px;
    color: rgb(255, 255, 255);
}

.artist {
color:rgb(87, 87, 87);     
}
</style>