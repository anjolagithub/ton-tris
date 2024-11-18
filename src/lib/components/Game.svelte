<script>
  let score = 0;
  let gameStatus = "Press Start to Begin!";
  
  function startGame() {
    gameStatus = "Game in Progress...";
    // Placeholder logic to simulate game progress
    const interval = setInterval(() => {
      score += 10;
      if (score >= 100) {
        clearInterval(interval);
        gameStatus = "Game Over!";
      }
    }, 1000);
  }
  
  function pauseGame() {
    gameStatus = "Game Paused";
  }
  
  function resetGame() {
    score = 0;
    gameStatus = "Game Reset. Press Start to Begin!";
  }
</script>

<h2>TONtris Game</h2>
<p class="score">Current Score: <strong>{score}</strong></p>
<p class="status">{gameStatus}</p>

<div class="button-group">
  <button on:click={startGame}>Start</button>
  <button on:click={pauseGame}>Pause</button>
  <button on:click={resetGame}>Reset</button>
</div>

<style>
  .score {
    font-size: 1.5em;
    color: #333;
  }

  .status {
    font-style: italic;
    margin-bottom: 10px;
  }

  .button-group button {
    margin: 5px;
    padding: 10px 15px;
    font-size: 1em;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #4CAF50;
    color: white;
  }

  .button-group button:hover {
    background-color: #45a049;
  }
</style>
