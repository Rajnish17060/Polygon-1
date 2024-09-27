# Building with Polygon Bridge 

> Sepolia to Amoy Bridge

> Can Be Bridged between ETHERIUM and POLYGON Blockchain

> Used ERC721A for less Gas consumption

## Description

This project involves the deployment of a 3-item NFT collection using Bing AI-generated images. The NFTs are stored on IPFS using pinata.cloud, and an ERC721A contract is deployed to the Goerli Ethereum Testnet. The contract includes functionalities such as minting, transferring, and mapping the NFTs.

## Getting Started

### Prerequisites

* Node.js and npm installed.
* Hardhat Ethereum development environment set up.
* Metamask Configured to Polygon Amoy Testnet.
* Test Polygon Amoy Testnet in Account in Testnet Network.

### Installation

1. Clone this repository: `git clone https://github.com/Kshitij251203/Polygon1.git`
2. Navigate to the project folder.
3. Install dependencies: `npm install`
### Wallet Config
- Network name : POLYGON AMOY TESTNET
- New RPC URL :  https://rpc-amoy.polygon.technology/
- Chain ID : 80002
- Currency Symbo : POL
> Block Explorer URL is Optional
### Contract Name and Symbol

```solidity
contract Dinar is ERC721A
```
Name : Dinar  
Symbol :DNR 

The `Dinar` contract extends the `ERC721A` contract and represents a collection of unique NFTs inspired by the Naruto series.

### Maximum Quantity of Tokens

```solidity
uint256 public maxLimit = 3;
```

The `maxLimit` variable sets the maximum number of NFTs that can be minted within this collection. In this contract, the maximum limit is set to 5 tokens.

### Base URL for NFTs (IPFS Base URL)

```solidity
string baseUrl = "https://bronze-wooden-aardvark-881.mypinata.cloud/ipfs/Qmf4MNSp6aJ3N1FPbLVms6vcsdjgUPJ9Wv71VT3qUs3RSn";
```

The `baseUrl` variable defines the base URL for the NFTs' metadata. This URL will be combined with the token ID to form the complete URL for accessing each NFT's metadata stored on the IPFS platform.

### Prompt Description

```solidity
string public prompt = "A Under-water world Portait, A Creative Futuristic World, A Majestic Peacock";
```
> Prompt can be anything based your Intrest 

### Deploy ERC721A Contract to Goerli Testnet

1. Create an `.env` file and set your Ethereum wallet private key.
2. Configure Hardhat network settings in `hardhat.config.js`.
3. Run the deployment script: `npx hardhat run scripts/DEPLOY.js --network amoy`

### Batch Mint NFTs

1. Edit the `MINT.js` script with required details.
2. Run the script: `npx hardhat run scripts/MINT.js --network amoy`

### Batch Transfer NFTs to Polygon Mumbai

1. Set up FxPortal Bridge for Ethereum to Polygon transfer.
2. Edit the `TransferTokens.js` script with necessary details.
3. Run the script: `npx hardhat run scripts/TransferTokens.js --network amoy`

### Check Balance 
1. Edit the `getBalance.js` script with required details.
2. Run the script: `npx hardhat run scripts/getBalance.js --network amoy`
## Explorer Used
- [Amoy Testnet Explorer](https://www.oklink.com/amoy)
- [Sepolia PoS Chain Testnet Explorer](https://sepolia.etherscan.io)
## Authors
Rajnish Kumar
