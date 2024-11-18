<script>
  import Game from "$lib/components/Game.svelte";
  import Leaderboard from "$lib/components/Leaderboard.svelte";
  import TokenPurchase from "$lib/components/TokenPurchase.svelte";
</script>

<main>
  <h1>Welcome to TONtris!</h1>
  <Game />
  <Leaderboard />
  <TokenPurchase />
</main>

<style>
  /* Basic styling */
  h1 { text-align: center; }
</style>
