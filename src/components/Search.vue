<template>
    <main>
        <form class="box">

            <button type="submit" class="buttonUno" 
                @click.prevent="$emit('filter', searchGenre)">
                Genre <i class="fa-solid fa-music"></i>
            </button>

            <input class="ricerca" type="text" placeholder="Search Music" 
            v-model="searchGenre">

            <button class="buttonDue"
                @click.prevent="reset">
                Cancel <i class="fa-solid fa-eject"></i>
            </button>
        </form>
    </main>
</template>

<script>
export default {
    name: "Search",
    data() {
        return{
            searchGenre: ""
        }
    },

    methods: {
        reset() {
            this.searchGenre = "";
            this.$emit('filter', "");
        }
    }

}
</script>

<style scoped lang="scss">
.box{
    max-width: 100%;
    margin:auto;
    // border: 5px solid rgb(255, 0, 0);
    display: flex;
    justify-content: center;
    padding: 110px 10px 20px 10px;
    background: linear-gradient(#224787, #ffffff00);
}
.buttonUno, .buttonDue {
    display: flex;
    padding: 5px 30px 5px 30px;
    // margin-top: 55px;
    // position: absolute;
    // top: 10%;
    // left: 30%;
    // transform: translate(-50%, -50%);
    border: 4px solid rgba(255, 255, 255, 0);
    border-radius: 5px;
    color: white;
    // background-color: rgb(71, 174, 71);
    background-color: rgb(63, 119, 63);
    display: none;
    justify-content: center;
    margin: 10px;

    &:hover.buttonUno {
        background-color: rgb(71, 196, 113);
        border: 3px solid rgb(0, 153, 38);
        font-weight: bold;
        // text-transform: uppercase;
    }
}

.buttonDue {
    // left: 70%;
    // background-color: rgb(53, 101, 213);
    background-color: rgb(68, 77, 100);

    &:hover.buttonDue {
        background-color: rgb(98, 160, 215);
        border: 3px solid rgb(26, 97, 210);
        font-weight: bold;
        // text-transform: uppercase;
    }
}

.ricerca {
    display: flex;
    padding: 5px 30px 5px 30px;
    // margin-top: 55px;
    // position: absolute;
    // top: 10%;
    // left: 50.4%;
    // transform: translate(-50%, -50%);
    border: none;
    border-radius: 5px;
    display: none;
    width: 30%;
    text-align: center;
    color: rgb(0, 174, 93);
    margin: 10px;
    text-transform: uppercase;



    &:hover.ricerca {
        background-color: rgba(36, 58, 90, 0.254);
    }
        &.ricerca::placeholder {
        color: rgba(255, 255, 255, 0.228);
        text-transform: uppercase;
    }
}

input:focus{
outline:none;
background-color: rgba(0, 30, 44, 0.692);
text-transform: uppercase;
cursor: pointer;
}

.fa-solid {
    padding-left: 5px ;
}

//-------------------RESPONSIVE WITHOUT FRAMEWORK---------------------//
// responsive SMALL SM
@media screen and (min-width: 576px) {

    .buttonUno {
        display: block;
    }

    .buttonDue {
        display: block;
    }

    .ricerca {
        display: block;
    }
}


</style>