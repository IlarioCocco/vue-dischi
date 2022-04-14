<template>
    <main>
        <form class="box">

            <button type="submit" class="buttonUno" 
                @click.prevent="$emit('filter', searchGenre)">
                Genre
            </button>

            <input class="ricerca" type="text" placeholder="Search Music" 
            v-model="searchGenre">

            <button class="buttonDue"
                @click.prevent="reset">
                Cancel
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
    padding: 10px 30px 10px 30px;
    // margin-top: 55px;
    // position: absolute;
    // top: 10%;
    // left: 30%;
    // transform: translate(-50%, -50%);
    border: 3px solid rgba(255, 255, 255, 0);
    border-radius: 5px;
    color: white;
    background-color: rgb(153, 213, 153);
    display: none;
    justify-content: center;
    margin: 10px;

    &:hover.buttonUno {
        background-color: rgb(72, 183, 109);
        border: 2px solid rgba(0, 88, 22, 0.33);
        font-weight: bold;
        // text-transform: uppercase;
    }
}

.buttonDue {
    // left: 70%;
    background-color: rgba(103, 145, 243, 0.548);

    &:hover.buttonDue {
        background-color: rgb(98, 160, 215);
        border: 2px solid rgba(0, 20, 133, 0.239);
        font-weight: bold;
        // text-transform: uppercase;
    }
}

.ricerca {
    display: flex;
    padding: 10px 30px 10px 30px;
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
    color: green;
    margin: 10px;

    &:hover.ricerca {
        background-color: rgba(67, 77, 68, 0.254);
    }
        &.ricerca::placeholder {
        color: rgb(255, 255, 255);
        text-transform: uppercase;
    }
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