<template>
<div class="MainSection">
    <div class="section">

        <div class="square">
            <img class="square-img" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
            <div class="titolo-album">
                <h4 class="titolo-album">new jersey</h4>
                <p>Bon Jovi <br>1988</p>
            </div>
        </div>

        <div class="square">
            <img class="square-img" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
            <div class="titolo-album">
                <h4 class="titolo-album">new jersey</h4>
                <p>Bon Jovi <br>1988</p>
            </div>
        </div>

        <div class="square">
            <img class="square-img" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
            <div class="titolo-album">
                <h4 class="titolo-album">new jersey</h4>
                <p>Bon Jovi <br>1988</p>
            </div>
        </div>

         <div class="square">
            <img class="square-img" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
            <div class="titolo-album">
                <h4 class="titolo-album">new jersey</h4>
                <p>Bon Jovi <br>1988</p>
            </div>
        </div>

        <div class="square">
            <img class="square-img" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
            <div class="titolo-album">
                <h4 class="titolo-album">new jersey</h4>
                <p>Bon Jovi <br>1988</p>
            </div>
        </div>

        <div class="square">
            <img class="square-img" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
            <div class="titolo-album">
                <h4 class="titolo-album">new jersey</h4>
                <p>Bon Jovi <br>1988</p>
            </div>
        </div>

    </div>
</div>
    
</template>



<script>


export default {
  name: 'MainSection',
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.MainSection {
    background-color: #1E2D3B;
}

.section {
    background-color: #1E2D3B;
    padding-top: 150px;
    display: flex;
    flex-wrap: wrap;
    align-content: flex-start;
    max-width: 60%;
    margin:auto;

        .square {
        height: 300px;
        background-color: rgba(92, 92, 92, 0.288);
        display: flex;
        flex-wrap: wrap;
        width: calc(20% - 10px);
        margin: 5px;
        display: flex;
        justify-content: center;
        align-content: center;

            .titolo-album {
            text-align: center;
            color: white;
        }
    }
}

.square-img {
    padding-top: 10px;
    height: 150px;
    display: flex;
    justify-content: center;
}

</style>
