<template>
<div>
    <div>
        <div v-if="winner">
            <h1 class="winner">Winner : {{ winner }}</h1>
            <button class="button" v-on:click="reset()">Reset</button>
        </div>
        <h1 v-else class="player">Now Playing : {{ player }}</h1>
    </div>
    <div class="container">
        <div v-for="x in 3" :key="x" class="row">
            <button v-for="y in 3" :key="y" class="square" v-on:click="place(x-1,y-1)">
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

                count : 0
            }
        },
        methods: {
            
            place(x,y) {
                if(this.winner === null && this.board[x][y] === ''){
                    this.board[x][y] = this.player
                    this.player = this.player === 'O' ? 'X':'O'
                    this.count++

                    this.winner = this.getWinner()
                }
                
            },

            getPlace(x,y) {return this.board[x][y]},
            
            getWinner() {
                for(let i = 0; i < 2; i++){
                    for(let j = 0; j < 3; j++){
                        if (i){
                            if(this.board[j][0] != '' && this.board[j][0] === this.board[j][1] && this.board[j][0] === this.board[j][2]){
                                return this.board[j][0]
                            }
                        }
                        else{
                           if(this.board[0][j] != '' && this.board[0][j] === this.board[1][j] && this.board[0][j] === this.board[2][j]){
                                return this.board[0][j]
                            } 
                        }
                    }
                }
                
                //TEST DIAGONALS
                if((this.board[0][0] != '' && this.board[0][0] === this.board[1][1] && this.board[0][0] === this.board[2][2]) || (this.board[0][2] != '' && this.board[0][2] === this.board[1][1] && this.board[0][2] === this.board[2][0])){
                    return this.board[1][1]
                }
                
                if(this.count === 9){
                    return "Draw !"
                }
                return null
            },

            reset() {
                this.winner = null
                this.board = [['','',''],['','',''],['','','']]
                this.count = 0
            }
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
.winner {
    color: #fff;
}
.test {
    color: #fff;
}
</style>
