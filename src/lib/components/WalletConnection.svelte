<script>
  import { ethers } from "ethers";
  
  let walletConnected = false;
  let walletAddress = "";
  let provider;
  let signer;

  async function connectWallet() {
    if (window.ethereum) {
      try {
        // Request account access
        await window.ethereum.request({ method: 'eth_requestAccounts' });
        provider = new ethers.providers.Web3Provider(window.ethereum);
        signer = provider.getSigner();
        
        // Get the user's wallet address
        walletAddress = await signer.getAddress();
        walletConnected = true;
        
        console.log("Wallet connected:", walletAddress);
      } catch (error) {
        console.error("Wallet connection error:", error);
      }
    } else {
      alert("Please install a MetaMask wallet to use this feature.");
    }
  }
  
  function disconnectWallet() {
    walletConnected = false;
    walletAddress = "";
    provider = null;
    signer = null;
  }
</script>

<div class="wallet-connection">
  {#if walletConnected}
    <p>Connected: {walletAddress}</p>
    <button on:click={disconnectWallet} class="wallet-button">Disconnect</button>
  {:else}
    <button on:click={connectWallet} class="wallet-button">Connect Wallet</button>
  {/if}
</div>

<style>
  .wallet-connection {
    margin-bottom: 20px;
  }

  .wallet-button {
    padding: 10px 15px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #673AB7;
    color: white;
  }

  .wallet-button:hover {
    background-color: #5E35B1;
  }
</style>
