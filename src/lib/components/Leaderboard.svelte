<script>
  import { onMount } from "svelte";

  let leaderboard = [];

  onMount(async () => {
    leaderboard = [
      { name: "Alice", score: 500 },
      { name: "Bob", score: 300 },
    ];
  });
</script>

<div class="leaderboard">
  <h2>Leaderboard</h2>
  <ul>
    {#each leaderboard as player}
      <li>{player.name}: {player.score}</li>
    {/each}
  </ul>
</div>

<style>
  .leaderboard {
    margin-top: 20px;
  }
</style>
