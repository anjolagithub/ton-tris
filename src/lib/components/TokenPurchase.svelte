<script>
  let tokenAmount = 0;
  let userBalance = 100;
  
  function buyTokens() {
    userBalance += tokenAmount;
    alert(`Purchased ${tokenAmount} tokens!`);
  }
</script>

<h2>Buy Tokens</h2>
<p>Your Balance: <strong>{userBalance}</strong> Tokens</p>
<div class="purchase-container">
  <input type="number" bind:value={tokenAmount} min="0" class="token-input" />
  <button on:click={buyTokens} class="buy-button">Buy Tokens</button>
</div>

<style>
  .purchase-container {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-top: 10px;
  }

  .token-input {
    padding: 8px;
    width: 60px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }

  .buy-button {
    padding: 8px 12px;
    font-size: 1em;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #FF9800;
    color: white;
  }

  .buy-button:hover {
    background-color: #FB8C00;
  }
</style>
