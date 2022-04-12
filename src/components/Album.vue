<template>
        <div class="square">
            <img class="img" :src="album.poster" :alt="album.title">
            <div class="titolo">
                <h4 class="album">
                    {{album.title}}
                </h4>
                <p class="artist">
                    {{album.author}}<br>
                    {{album.year}}
                </p>
            </div>
        </div>
</template>


<script>
export default {
    name: 'Album',
    props: ['album']
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