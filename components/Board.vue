<template>
    <div class="board">
        <div v-for="x in 3" :key="x" class="row">
            <div v-for="y in 3" :key="y" class="square" v-on:click="place(x,y)">
            O</div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                Board :[
                    ['','',''],
                    ['','',''],
                    ['','','']]
            }
        },
        methods: {
            getboard(x,y){
                return //{ Board[x][y] }
            },
            place(x,y){
                this.Board[x][y] = 'X'
            },
        }
    }

</script>

<style scoped>
.board {
    margin: 50px;
    display: grid;
    grid-column: 3;
    grid-row: 3;
}
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
</style>
