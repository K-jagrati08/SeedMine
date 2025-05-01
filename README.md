# SeedMine

> **Short Summary (<150 chars):**  
> A decentralized funding hub on Polkadot Asset Hub powering transparent, on-chain grants for Web3 projects.

## Full Description

**Problem Statement**  
Traditional grant programs and hackathon prizes suffer from opaque processes, off-chain coordination overhead, and high fees. Builders struggle to find transparent, low-friction funding.

**Solution Overview**  
SeedMine is an open-source, on-chain funding marketplace where project teams submit proposals and community members stake DOT to back them. All votes, funding flows, and vesting schedules are executed by custom smart contracts on Polkadot Asset Hub, ensuring trustless, automated disbursements and on-chain governance.

**Why Polkadot?**  
Polkadot Asset Hub’s shared-security, low-fee environment and on-chain governance pallets allow SeedMine’s custom funding logic to run seamlessly. XCM messaging ensures cross-chain compatibility for future expansions. 

## Technical Description:
1) Smart contracts in Solidity (PolkaVM) handle project creation, funding, vesting schedules, and milestone approvals.
2) Ethers.js scripts (compile.js, deploy.js, checkStorage.js) compile, deploy, and interact with the contract on Westend Asset Hub.	
3) React + Vite + Tailwind frontend at localhost:5173 drives wallet connections, UI, and real-time updates.	
4) Polkadot Asset Hub provides secure scaling, low fees, and native chain-level governance features.	

## Prerequisites

- Node.js v22.13.1 or later
- npm v6.13.4 or later
- A wallet with some test tokens on the Westend Asset Hub network

## Canva Presentation:
https://www.canva.com/design/DAGlzrqkodY/bMUl2x0WklenWYNuC734nw/edit?utm_content=DAGlzrqkodY&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
## Video Link: 
https://youtu.be/iA_-hSlSwzg
## Screenshots: 
# Project Screenshots

## Image 1
![Image 1](image1.png)

## Image 2
![Image 2](image2.png)

## Image 3
![Image 3](image3.png)



## Block explorer link for deployed smart contract on Asset Hub
https://assethub-westend.subscan.io/account/0x23b85081fd93a40608454d54a1088c328260cf02

## 📁 Repository Structure 


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
