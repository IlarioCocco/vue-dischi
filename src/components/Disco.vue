<template>
        <div class="square">
            <img class="img" :src="disco.poster" alt="">
            <div class="titolo">
                <h4 class="album">{{disco.title}}</h4>
                <p class="artist">{{disco.author}}<br>{{disco.year}}</p>
            </div>
        </div>
</template>
















<script>
export default {
    name: "Disco",
    props: ['disco']

}
</script>














<style scoped lang="scss">

  .square {
            padding: 10px 10px 25px 10px;
            display: flex;
            flex-wrap: wrap;
            width: calc(100% / 2 - 20px);
            margin: 10px;
            justify-content: center;
            border: 1px solid rgb(248, 178, 0);

        .img {
            width: 100%;
            padding: 0px 0px 10px 0px; 
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
        color: rgb(248, 178, 0);
    }

   .artist {
    color:grey;     
    }

</style>