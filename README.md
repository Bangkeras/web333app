# web333app

This project is a demonstration of using the `web333dapper` package for smart contract interactions and blockchain communication.

## Installation

```bash
npm install web333dapper


Usage

const Web333Dapper = require('web333dapper');

// Instantiate Web333Dapper with your Infura API key and private key
const dapper = new Web333Dapper('https://rinkeby.infura.io/v3/YOUR_INFURA_API_KEY', 'YOUR_PRIVATE_KEY');

// Deploy a simple ERC20 token contract
dapper.deployContract().then((contractAddress) => {
  console.log(`Contract deployed at: ${contractAddress}`);
});

// Transfer tokens
dapper.transferTokens('senderAddress', 'recipientAddress', 50).then((transactionHash) => {
  console.log(`Transaction hash: ${transactionHash}`);
});

// Get ETH balance
dapper.getEthBalance('0x1234567890123456789012345678901234567890').then((ethBalance) => {
  console.log(`ETH balance: ${ethBalance} ETH`);
});
