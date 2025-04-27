## Seedmine

This project demonstrates how to interact with the Polkadot Asset Hub using Ethers.js. It includes a simple Storage smart contract and scripts to compile, deploy, and interact with it. It Offers a decentralized Web3 project marketplace that helps founders list & fund Git-backed ideas while giving investors on-chain governance and verifiable milestones via Polkadot. 

## Description: 
Seedmine is a Polkadot-powered, on-chain project marketplace that brings founders and investors together. Founders connect their wallet, publish a GitHub-backed idea, and specify milestone-based funding tranches enforced by a Solidity smart contract on the Westend Asset Hub. Investors browse live projects, stake DOT or community tokens into funding pools, and receive NFT-based governance rights. Seedmine makes every step fully transparent, from code commits to fund releases, streamlining early-stage financing in Web3.

## Technical Description:
1) Smart contracts in Solidity (PolkaVM) handle project creation, funding, vesting schedules, and milestone approvals.
2) Ethers.js scripts (compile.js, deploy.js, checkStorage.js) compile, deploy, and interact with the contract on Westend Asset Hub.	
3) React + Vite + Tailwind frontend at localhost:5173 drives wallet connections, UI, and real-time updates.	
4) Polkadot Asset Hub provides secure scaling, low fees, and native chain-level governance features.	

## Prerequisites

- Node.js v22.13.1 or later
- npm v6.13.4 or later
- A wallet with some test tokens on the Westend Asset Hub network

## Screenshots: 
<p align="center">
  <img src="![Screenshot 2025-04-27 092323](https://github.com/user-attachments/assets/1e710d4b-993f-47bd-94ed-82a263471f69)
" alt="Mobile preview" width="300">
</p>


## Block explorer link for deployed smart contract on Asset Hub
https://assethub-westend.subscan.io/account/0x23b85081fd93a40608454d54a1088c328260cf02

## Project Structure

```
ethers-asset-hub/
├── contracts/
│   ├── Storage.sol
├── scripts/
│   ├── connectToProvider.js
│   ├── compile.js
│   ├── deploy.js
│   ├── checkStorage.js
├── abis/
│   ├── Storage.json
├── artifacts/
│   ├── Storage.polkavm
├── contract-address.json
├── package.json
└── README.md
```

## Installation

1. Clone the repository
2. Install dependencies:
```bash
npm install
```

## Usage

1. Compile the smart contract:
```bash
node scripts/compile.js
```

2. Deploy the contract:
   - Edit `scripts/deploy.js` and replace `INSERT_MNEMONIC` with your wallet's mnemonic
   - Run:
```bash
node scripts/deploy.js
```

3. Interact with the contract:
   - Edit `scripts/checkStorage.js` and replace:
     - `INSERT_MNEMONIC` with your wallet's mnemonic
     - `INSERT_CONTRACT_ADDRESS` with the deployed contract address
   - Run:
```bash
node scripts/checkStorage.js
```

## Configuration

The project is configured to connect to the Westend Asset Hub network with the following parameters:
- RPC URL: https://westend-asset-hub-eth-rpc.polkadot.io
- Chain ID: 420420421
- Chain Name: westend-asset-hub

## Security

Never commit your mnemonic or private keys to version control. Always use environment variables or secure key management solutions in production. 
