<template>
  <div>
      <div class="title">
        <h1>TicTacToe</h1>
        <p>By SchauT and Shasame :)</p>
      </div>

      <div class="button-menu">
        <nuxt-link class="button" to="local">LOCAL GAME</nuxt-link>
        <nuxt-link class="button" to="lan">LAN</nuxt-link>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.button-menu {
  display: flex;
  align-items: center;
  flex-direction: row;
  width: 100%;
  text-align: center;
  margin: 10% 0;
  min-height: 200px;
  align-items: center;
}
</style>