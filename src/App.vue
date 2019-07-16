<template>
  <div id="app" class="container">
    <h1 class="text-center">Player Counter</h1>
    <div class="card">
      <div class="card-body text-center">
        <h3>Player 1</h3>
        <div class="info">
          <button
            v-on:click="player_1_score > 0 ? player_1_score -= 1 : 0"
            class="btn btn-danger"
          >Down</button>
          <span class="player-score">{{player_1_score}}</span>
          <button v-on:click="player_1_score += 1" class="btn btn-success">Up</button>
        </div>
      </div>
    </div>
    <div class="card">
      <div class="card-body text-center">
        <h3>Player 2</h3>
        <div class="info">
          <button
            v-on:click="player_2_score > 0 ? player_2_score -= 1 : 0"
            class="btn btn-danger"
          >Down</button>
          <span class="player-score">{{player_2_score}}</span>
          <button v-on:click="player_2_score += 1" class="btn btn-success">Up</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      player_1_score: 0,
      player_2_score: 0
    };
  }
};
</script>

<style>
.card:first-of-type {
  margin-bottom: 2rem;
}
.info {
  display: flex;
  justify-content: space-around;
}
.info:first-of-type {
  margin-bottom: 2rem;
}
.player-score {
  font-size: 2rem;
}
</style>
