<script>
  let score = 0;

  function playGame() {
    score += Math.floor(Math.random() * 100);
  }
</script>

<div class="game-container">
  <h2>TONtris Game</h2>
  <button on:click={playGame}>Play</button>
  <p>Current Score: {score}</p>
</div>

<style>
  .game-container {
    text-align: center;
  }
</style>
