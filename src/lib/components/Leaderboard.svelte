<script>
  let leaderboard = [
    { name: "Alice", score: 500 },
    { name: "Bob", score: 300 },
  ];
  
  function refreshLeaderboard() {
    console.log("Leaderboard refreshed");
  }
</script>

<h2>Leaderboard</h2>
<ul class="leaderboard-list">
  {#each leaderboard as player}
    <li>{player.name}: {player.score}</li>
  {/each}
</ul>

<button on:click={refreshLeaderboard} class="refresh-button">Refresh</button>

<style>
  .leaderboard-list {
    list-style: none;
    padding: 0;
    font-size: 1.2em;
    color: #333;
  }

  .leaderboard-list li {
    margin: 5px 0;
  }

  .refresh-button {
    margin-top: 10px;
    padding: 8px 12px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #2196F3;
    color: white;
  }

  .refresh-button:hover {
    background-color: #1976D2;
  }
</style>
