<template>
    <div>
        <div>
            <h1>LOCAL</h1>
            <nuxt-link to="/">
                <button>Home</button>
            </nuxt-link>
        </div>
        <Board />
    </div>
</template>

<script>
import Board from "../components/board.vue";

export default { components: { Board } }
</script>