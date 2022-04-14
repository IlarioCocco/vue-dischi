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
            <h6 class="genre">
                {{albums.genre}}
            </h6>
        </div>
    </div>
</template>


<script>
export default {
    name: 'Album',
    props: ['album', 'albums']
    // è possibile esportarlo anche come obj
    // props: {albums: Object}
}
</script>


<style scoped lang="scss">
.img {
    width: 100%;
    padding: 0px 0px 10px 0px; 
    cursor: pointer;
    // position: relative;
    // clip-path: inset(0% 0% 0% 0%);

    &.img:hover {
        padding: 2px 2px 12px 2px; 
        filter: brightness(70%);
    }
}

.titolo {
    text-align: center;
    color: white;
    // border: 5px solid rgba(255, 255, 255, 0.219);
    max-width: 100%;
}

.album {
    font-size: 20px;
    color: rgb(255, 255, 255);
   
}

.artist {
    color:rgb(123, 123, 123);
}

.genre {
    color:rgb(149, 105, 17);

    &.genre:hover {
            color:rgb(244, 231, 205);
            cursor: pointer; 
    }
}
</style>

