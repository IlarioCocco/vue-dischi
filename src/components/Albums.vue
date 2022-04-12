<template>
    <main>
        <section>
            <!-- <div class="square" v-for="(todo, i) in dischi" :key="i">
                <img class="img" :src="todo.poster" alt="">
                <div class="titolo">
                    <h4 class="album">{{todo.title}}</h4>
                    <p class="artist">{{todo.author}}<br>{{todo.year}}</p>
                </div>
            </div> -->
        <Album v-for="(todo, i) in music" :key="i" :album="todo"/>
        </section>
    </main>
</template>






<script>
// import axios from 'axios';
import Album from '../components/Album.vue';
import prods from '../data/music.json';

export default {
    name: "Albums",
    components: {
        Album
    },

    data() {
        return {
            // music: [],
            music: prods,
        }
    }
}
</script>







<style scoped lang="scss">
main {
    // height: 100vh;
    padding: 0px 0px 50px 0px;
    border: 5px solid #da4b4b00;
}

section {
    padding: 120px 0px 10px 0px;  
    display: flex;
    flex-wrap: wrap;
    max-width: 80%;
    margin:auto;
    border: 5px solid rgba(23, 201, 0, 0);

//         .square {
//             padding: 10px 10px 25px 10px;
//             display: flex;
//             flex-wrap: wrap;
//             width: calc(100% / 2 - 20px);
//             margin: 10px;
//             justify-content: center;
//             border: 1px solid rgb(248, 178, 0);

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
//         color: rgb(248, 178, 0);
//     }

//    .artist {
//     color:grey;     
//     }
}





//-------------------RESPONSIVE---------------------//
// responsive SMALL SM
@media screen and (min-width: 576px) {

    main {
    // height: 200vh;
    padding: 0px 0px 50px 0px;
    border: 5px solid #da4b4b00;
}

    section {
        padding: 120px 0px 10px 0px;  
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        border: 5px solid rgba(23, 201, 0, 0);

        .square {
        padding: 10px 10px 25px 10px;
        width: calc(100% / 2 - 20px);
        margin: 10px;
        justify-content: center;
        // border: 1px solid rgb(248, 178, 0);

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
    }
}

// responsive MEDIUM MD
@media screen and (min-width: 768px) {

    main {
    // height: 200vh;
    padding: 0px 0px 50px 0px;
    border: 5px solid #da4b4b00;
}

    section {
        padding: 120px 0px 10px 0px;  
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        border: 5px solid rgba(23, 201, 0, 0);

        .square {
        padding: 10px 10px 25px 10px;
        width: calc(100% / 3 - 20px);
        margin: 10px;
        justify-content: center;
        // border: 1px solid rgb(248, 178, 0);

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
    }
}

// responsive LARGE XL
@media screen and (min-width: 992px) {
    
    main {
    // height: 200vh;
    padding: 0px 0px 50px 0px;
    border: 5px solid #da4b4b00;
}

    section {
        padding: 120px 0px 10px 0px;      
        display: flex;
        flex-wrap: wrap;
        max-width: 80%;
        margin:auto;
        border: 5px solid rgba(23, 201, 0, 0);

        .square {
        padding: 10px 10px 25px 10px;
        width: calc(100% / 5 - 20px);
        margin: 10px;
        justify-content: center;
        // border: 1px solid rgb(248, 178, 0);

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
    }
}
</style>






