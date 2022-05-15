<template>
<div>
    <div>
        <h1 v-if="winner" class="winner">Winner : {{ winner }}</h1>
        <h1 v-else class="player">Now Playing : {{ player }}</h1>
    </div>
    <div class="container">
        <div v-for="x in 3" :key="x" class="row">
            <button v-for="y in 3" :key="y" class="square" v-on:click="count++,place(x-1,y-1)">
                {{ board[x-1][y-1] }}
            </button>
        </div>
    </div>
</div>
</template>

<script>
    export default{
        data() {
            return{

                winner : null,

                player : 'O',
                
                board : [['','',''],['','',''],['','','']],

                count : 1
            }
        },
        methods: {
            
            place(x,y) {
                this.board[x][y] = this.player
                this.player = this.player === 'O' ? 'X':'O'
            },
            getPlace(x,y) {return this.board[x][y]}
        }
    }
</script>

<style scoped>
.square {
  background: #212121;
  border: 1px solid #fff;
  float: left;
  font-size: 70px;
  font-weight: bold;
  line-height: 34px;
  height: 100px;
  margin-right: -1px;
  margin-top: -1px;
  padding: 0;
  text-align: center;
  width: 100px;
  color: #E55E5B;
}

.player {
    color: #fff;
}
</style>
