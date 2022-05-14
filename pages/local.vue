<template>
    <div>
        <div>
            <h1 class="title">LOCAL</h1>
            <nuxt-link to="/" class="button">Home</nuxt-link>
        </div>
        <Board class="board"/>
    </div>
</template>

<script>
import Board from "/components/Board.vue";

export default { components: { Board } }
</script>

<style scoped>
    .title {
        margin: 20px;
    }
    .board {
        margin-top: 50px;
    }

</style>