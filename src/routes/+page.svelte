<script>
  import Game from '../lib/components/Game.svelte';
  import Leaderboard from '../lib/components/Leaderboard.svelte';
  import TokenPurchase from '../lib/components/TokenPurchase.svelte';
  import WalletConnection from '../lib/components/WalletConnection.svelte';
</script>

<h1>Welcome to TONtris!</h1>

<WalletConnection />

<div class="main-container">
  <div class="game-section">
    <Game />
  </div>
  
  <div class="leaderboard-section">
    <Leaderboard />
  </div>
  
  <div class="purchase-section">
    <TokenPurchase />
  </div>
</div>

<style>
  h1 {
    text-align: center;
    font-size: 2em;
    margin-bottom: 20px;
    color: #333;
  }

  .main-container {
    display: flex;
    gap: 20px;
    justify-content: space-around;
    padding: 20px;
  }

  .game-section, .leaderboard-section, .purchase-section {
    flex: 1;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    background-color: #f9f9f9;
  }

  .game-section {
    background-color: #FFF3E0;
  }

  .leaderboard-section {
    background-color: #E3F2FD;
  }

  .purchase-section {
    background-color: #FFFDE7;
  }

  @media (max-width: 768px) {
  .main-container {
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }

  .game-section, .leaderboard-section, .purchase-section {
    width: 90%;
  }

  h1 {
    font-size: 1.5em;
  }
}

</style>
