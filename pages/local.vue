<template>
    <div>
        <div>
            <h1 class="title">LOCAL</h1>
            <nuxt-link to="/" class="button">Home</nuxt-link>
        </div>
        <Board />
    </div>
</template>

<script>
import Board from "/components/Board.vue";

export default { components: { Board } }
</script>

<style scoped>

</style>