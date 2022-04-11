<template>
    <main>
        <section>

            <div class="square" v-for="(todo, i) in dischi" :key="i">
                <img class="img" :src="todo.poster" alt="">
                <div class="titolo">
                    <h4 class="album">{{todo.title}}</h4>
                    <p class="artist">{{todo.author}}<br>{{todo.year}}</p>
                </div>
            </div>

        </section>
    </main>
</template>






<script>
export default {
    name: 'Main',
    data() {
        return {
                dischi: [
                {
                    poster: "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
                    title: "New Jersey",
                    author: "Bon Jovi",
                    genre: "Rock",
                    year:  1988
                },
                {
                    poster: "https://img.discogs.com/vknPDdrqRbT92pNRX0W4I5N91jg=/fit-in/300x300/filters:strip_icc():format(jpeg):mode_rgb():quality(40)/discogs-images/R-1246953-1448927086-6590.jpeg.jpg",
                    title: "Live at Wembley 86",
                    author: "Queen",
                    genre: "Pop",
                    year: 1992
                },
                {
                    poster: "https://images-na.ssl-images-amazon.com/images/I/41JD3CW65HL.jpg",
                    title: "Ten's Summoner's Tales",
                    author: "Sting",
                    genre: "Pop",
                    year: 1993
                },
                {
                    poster: "https://cdn2.jazztimes.com/2018/05/SteveGadd-800x723.jpg",
                    title: "Steve Gadd Band",
                    author: "Steve Gadd Band",
                    genre: "Jazz",
                    year: 2018
                },
                {
                    poster: "https://images-na.ssl-images-amazon.com/images/I/810nSIQOLiL._SY355_.jpg",
                    title: "Brave new World",
                    author: "Iron Maiden",
                    genre: "Metal",
                    year: 2000
                },
                {
                    poster: "https://upload.wikimedia.org/wikipedia/en/9/97/Eric_Clapton_OMCOMR.jpg",
                    title: "One more car, one more raider",
                    author: "Eric Clapton",
                    genre: "Rock",
                    year: "2002"
                },
                {
                    poster: "https://images-na.ssl-images-amazon.com/images/I/51rggtPgmRL.jpg",
                    title: "Made in Japan",
                    author: "Deep Purple",
                    genre: "Rock",
                    year: 1972
                },
                {
                    poster: "https://images-na.ssl-images-amazon.com/images/I/81r3FVfNG3L._SY355_.jpg",
                    title: "And Justice for All",
                    author: "Metallica",
                    genre: "Metal",
                    year: 1988
                },
                {
                    poster: "https://img.discogs.com/KOBsqQwKiNKH-q927oHMyVdDzSo=/fit-in/596x596/filters:strip_icc():format(jpeg):mode_rgb():quality(90)/discogs-images/R-6406665-1418464475-6120.jpeg.jpg",
                    title: "Hard Wired",
                    author: "Dave Weckl",
                    genre: "Jazz",
                    year: 1994
                },
                {
                    poster: "https://m.media-amazon.com/images/I/71K9CbNZPsL._SS500_.jpg",
                    title: "Bad",
                    author: "Michael Jacjson",
                    genre: "Pop",
                    year: 1987 
                },
                {
                    poster: "https://images-na.ssl-images-amazon.com/images/I/51rggtPgmRL.jpg",
                    title: "Made in Japan",
                    author: "Deep Purple",
                    genre: "Rock",
                    year: 1972
                },
                {
                    poster: "https://images-na.ssl-images-amazon.com/images/I/81r3FVfNG3L._SY355_.jpg",
                    title: "And Justice for All",
                    author: "Metallica",
                    genre: "Metal",
                    year: 1988
                },
            ]
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
        width: calc(100% / 3 - 20px);
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
        width: calc(100% / 4 - 20px);
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
        width: calc(100% / 6 - 20px);
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
    }
}
</style>






