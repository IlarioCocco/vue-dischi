<template>
  <footer>
      <section>
          <h2 class="titoliFooter">Spotify</h2>
      </section>
  </footer>
</template>



<script>
export default {
    name: 'Footer',
}
</script>



<style lang="scss" scoped>
section {
    background-color: rgba(0, 0, 0, 0.692);
    padding: 30px;
    color: rgb(106, 212, 106);
}

.titoliFooter{
    display: flex;
    justify-content: center;
    font-size: 40px;
}
</style>