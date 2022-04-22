<template>
    <main>
        <form>
            <Search @filter="searchGenre"/>
        </form>
        <section> 
            <div class="square" v-for="(todo, i) in musicaFilter" :key="i"> 
                <Album :albums="todo"/>
            </div>
        <!-- <Album v-for="(todo, i) in music" :key="i" :album="todo"/> -->
        </section>
         <!-- <Search/> -->
    </main>
</template>


<script>
import axios from 'axios';
import Album from '../components/Album.vue';
import Search from '../components/Search.vue';
// import prods from '../data/music.json';

export default {
    name: "Albums",
    components: {
        Album,
        Search
    },

    data() {
        return {
            // music: prods,
            musica: [],
            // musicaFilter: []
            filter: ""
        }
    },

    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then( (res) => {
            console.log(res)
            this.musica = res.data.response;
            // this.musicaFilter = res.data.response;
        })
    },

    // methods: {
    //     searchComics(info) {
    //         // console.log(text)
    //         this.musica = this.musica.filter((elm) => {
    //             return elm.genre.toUpperCase().includes(info.toUpperCase());  // solo filter
    //             }
    //         )
    //     }
    // },

    // methods: {
    //     searchComics(info) {
    //         // console.log(text)
    //         this.musicaFilter = this.musica.filter((elm) => {
    //             return elm.genre.toUpperCase().includes(info.toUpperCase()); // codice duplicato vedi this in created
    //             }
    //         );
    //     }
    // },

    methods: {
        searchGenre(info) {
           this.filter = info;
        }
    },

    computed: {
        musicaFilter() {
            return  this.musica.filter((elm) => {
                return elm.genre.toUpperCase().includes(this.filter.toUpperCase()); // computed properties solution  true o false
                }
            );
        }
    }
}    
</script>


<style scoped lang="scss">
main {
    padding: 0px 0px 0px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
    background-color: rgb(37, 37, 37);
}

section {
    // position: relative;
    padding: 0px 0px 30px 0px;  
    display: flex;
    flex-wrap: wrap;
    max-width: 80%;
    margin:auto;
    // border: 5px solid hsl(40, 100%, 50%);

    .square {
        background-color: #243339;
        padding: 5px 5px 5px 5px;
        display: flex;
        flex-wrap: wrap;
        width: calc(100% / 1 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 60%, 61%, 0.116);
    }
}


//-------------------RESPONSIVE WITHOUT FRAMEWORK---------------------//
// responsive SMALL SM
@media screen and (min-width: 576px) {
    .box{
    border: 1px solid green;
}

    main {
    padding: 0px 0px 0px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
}

    section {
        padding: 0px 0px 30px 0px;
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        // border: 5px solid hsla(196, 53%, 14%, 0.486);

        .square {
        padding: 5px 5px 5px 5px;
        width: calc(100% / 2 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 60%, 61%, 0.116);
        }
    }
}

// responsive MEDIUM MD
@media screen and (min-width: 768px) {
    .box{
    border: 1px solid green;
}

    main {
    padding: 0px 0px 0px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
}

    section {
        padding: 0px 0px 30px 0px;  
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        // border: 5px solid hsla(196, 53%, 14%, 0.486);

        .square {
        padding: 5px 5px 5px 5px;
        width: calc(100% / 3 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 60%, 61%, 0.116);
        }
    }
}

// responsive LARGE XL
@media screen and (min-width: 992px) {
    .box{
    border: 1px solid green;
}
    
    main {
    padding: 0px 0px 0px 0px;
    // border: 5px solid hsl(196, 53%, 14%);
}

    section {
        padding: 0px 0px 30px 0px;    
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        // border: 5px solid hsla(196, 53%, 14%, 0.486);

        .square {
        padding: 5px 5px 5px 5px;
        width: calc(100% / 5 - 20px);
        margin: 10px;
        justify-content: center;
        border: 5px solid hsla(196, 60%, 61%, 0.116);

    //         .img {
    //             width: 100%;
    //             padding: 0px 0px 10px 0px; 
    //         }

    //         .titolo {
    //             text-align: center;
    //             color: white;
    //             // border: 5px solid rgba(255, 255, 255, 0.219);
    //             max-width: 100%;
    //         }
    //     }

    //     .album {
    //         font-size: 20px;
    //         color: rgb(223, 223, 223);
    //     }

    // .artist {
    //     color:grey;     
        }
    }
}
</style>