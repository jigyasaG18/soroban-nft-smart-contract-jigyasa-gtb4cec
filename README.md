```markdown
#### Decentralized NFT System Smart Contract

This project implements a decentralized Non-Fungible Token (NFT) system on the Stellar network using the Soroban SDK. NFTs are managed through smart contracts, ensuring uniqueness, transparency, and secure ownership transfers.

## Key Features

* **NFT Creation:** Users can mint new NFTs with unique identifiers and associated metadata.
* **Ownership Management:** Smart contracts handle ownership transfers and approvals, ensuring secure and transparent transactions.
* **Event Logging:** The system logs events such as transfers, minting, burning, and approvals for auditing purposes.
* **Metadata Management:** Metadata such as name, symbol, and URI associated with each NFT are stored securely on the blockchain.

## Prerequisites

* A Stellar Testnet account with some test XLM tokens.
* Basic understanding of Rust programming and the Stellar network.
* Soroban SDK installed ([https://soroban.stellar.org/install.sh](https://soroban.stellar.org/install.sh))

## Project Setup

1. Clone this repository.
2. Install dependencies:
   ```bash
   cargo install --locked
soroban build --target wasm32-unknown-unknown
   ```
```
