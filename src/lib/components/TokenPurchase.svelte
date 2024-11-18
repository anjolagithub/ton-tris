<script>
  let purchaseAmount = 0;
  let transactionStatus = "";

  async function purchaseTokens() {
    transactionStatus = "Purchase successful!";
  }
</script>

<div class="token-purchase">
  <h2>Buy Tokens</h2>
  <input type="number" bind:value={purchaseAmount} placeholder="Enter amount" />
  <button on:click={purchaseTokens}>Buy Tokens</button>
  <p>{transactionStatus}</p>
</div>

<style>
  .token-purchase {
    margin-top: 20px;
    text-align: center;
  }
</style>
