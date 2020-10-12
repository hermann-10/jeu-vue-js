<template>
  <div id="app">
    <game :player="player" v-on:score="updateScore"></game>
    <player v-on:player="updatePlayer" class="text-center"></player>
    <score :score="score" :player="player" class="text-center"></score>
  </div>
</template>

<script>
import Game from './components/Game'
import Score from './components/Score'
import Player from './components/Player'

export default {
  name: 'app',
  data: function () {
    return { score: 0, player: false }
  },
  components: {
    Game,
    Score,
    Player
  },
  methods: {
    updateScore: function (score) {
      this.score = score
    },
    updatePlayer: function () {
      this.player = true
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 500px;
  display: block;
}
</style>
