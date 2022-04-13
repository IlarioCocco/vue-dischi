<template>
    <main>
        <section>
            <div class="square" v-for="(todo, i) in musica" :key="i"> 
              <Album :albums="todo"/>
            </div>
        <!-- <Album v-for="(todo, i) in music" :key="i" :album="todo"/> -->
        </section>
    </main>
</template>


<script>
import axios from 'axios';
import Album from '../components/Album.vue';
// import prods from '../data/music.json';

export default {
    name: "Albums",
    components: {
        Album
    },

    data() {
        return {
            // music: prods,
            musica: []
        }
    },

    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then( (res) => {
            console.log(res)
            this.musica = res.data.response;
        })
    }
}    
</script>


<style scoped lang="scss">
main {
    padding: 0px 0px 50px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
}

section {
    padding: 120px 0px 10px 0px;  
    display: flex;
    flex-wrap: wrap;
    max-width: 80%;
    margin:auto;
    // border: 5px solid hsla(196, 53%, 14%, 0.486);

    .square {
        background-color: #2762797e;
        padding: 5px 5px 45px 5px;
        display: flex;
        flex-wrap: wrap;
        width: calc(100% / 1 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 53%, 14%, 0.116);
    }
}


//-------------------RESPONSIVE WITHOUT FRAMEWORK---------------------//
// responsive SMALL SM
@media screen and (min-width: 576px) {

    main {
    padding: 0px 0px 50px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
}

    section {
        padding: 120px 0px 10px 0px;  
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        // border: 5px solid hsla(196, 53%, 14%, 0.486);

        .square {
        padding: 5px 5px 45px 5px;
        width: calc(100% / 2 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 53%, 14%, 0.116);

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
            color: rgb(223, 223, 223);
        }

    .artist {
        color:grey;     
        }
    }
}

// responsive MEDIUM MD
@media screen and (min-width: 768px) {

    main {
    padding: 0px 0px 50px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
}

    section {
        padding: 120px 0px 10px 0px;  
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        // border: 5px solid hsla(196, 53%, 14%, 0.486);

        .square {
        padding: 5px 5px 45px 5px;
        width: calc(100% / 3 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 53%, 14%, 0.116);

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
            color: rgb(223, 223, 223);
        }

    .artist {
        color:grey;     
        }
    }
}

// responsive LARGE XL
@media screen and (min-width: 992px) {
    
    main {
    padding: 0px 0px 50px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
}

    section {
        padding: 120px 0px 10px 0px;      
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        // border: 5px solid hsla(196, 53%, 14%, 0.486);

        .square {
        padding: 5px 5px 45px 5px;
        width: calc(100% / 5 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 53%, 14%, 0.116);

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
            color: rgb(223, 223, 223);
        }

    .artist {
        color:grey;     
        }
    }
}
</style>