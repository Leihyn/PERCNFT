# ERC-721 Token Creation Project

This project demonstrates how to create and deploy a private ERC721 (non-fungible token) smart contract using Hardhat, a popular Solidity development framework. The project is deployed on the Swisstronik network.

## Overview

The ERC721 standard is widely used for creating unique digital assets (NFTs). This project sets up a basic private ERC721 token with customizable metadata and deployment scripts. You can use this as a starting point for creating your own private NFTs or expanding the functionality to suit more complex use cases.

## Features

- ERC721 Standard: Implements the ERC721 standard with minting functionality.
- Custom Metadata: Supports setting token URIs for metadata.
- Deployment: Scripts for deploying the contract to the Swisstronik network.
- Testing: Basic tests for the ERC721 functionality using Hardhat.

## Prerequisites

- Node.js: Ensure you have Node.js installed (>= 14.x).
- npm or yarn: Package manager for installing dependencies.
- Hardhat: A development environment for Ethereum smart contracts.
- Swisstronik Network: Access to the Swisstronik network for deployment.

## Getting Started

Here is the main guide: [Swisstronik Contract Deployment with Hardhat](https://swisstronik.gitbook.io/swisstronik-docs/development/guides/contract-deployment-hardhat/)

### 1. Clone the Repository

```bash
git clone https://github.com/Leihyn/swissERC721.git 
cd erc721-token-swisstronik
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Configure the Network

In the `hardhat.config.js` file, configure the Swisstronik network settings:

USE A DEMO ACCOUNT; an account you can afford to lose**

```javascript
module.exports = {
  solidity: "0.8.19",
  networks: {
    swisstronik: {
      url: "(use swisstronik rpc)",  // Replace with the correct RPC URL from the Gitbook
      accounts: ["YOUR_PRIVATE_KEY"],  // Replace with your Swisstronik network private key
    },
  },
};
```

### 4. Compile the Contract

```bash
npx hardhat compile
```

### 5. Deploy the Contract

```bash
npx hardhat run scripts/deploy.js --network swisstronik
```

### 6. Run Tests

```bash
npx hardhat test
```

## Project Structure

- `contracts/`: Contains the ERC721 smart contract.
- `scripts/`: Deployment scripts.
- `test/`: Test files for the ERC721 contract.
- `hardhat.config.js`: Hardhat configuration file.

## Customization

- Token Name and Symbol: Modify the name and symbol of the token in the ERC721 contract.

## Deployment

After configuring the network and writing your contract, you can deploy it using the deployment script. The script will push the contract to the Swisstronik network, and you'll receive a contract address upon success.

---

This version emphasizes that the ERC-721 token is private, with the necessary details for setting up, deploying, and customizing the contract on the Swisstronik network.
