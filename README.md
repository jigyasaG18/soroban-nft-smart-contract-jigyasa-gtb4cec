
# 🚀 Stellar NFT Smart Contract System Overview 🚀

This project implements a decentralized Non-Fungible Token (NFT) system on the Stellar network using the Soroban SDK. NFTs are managed through smart contracts, ensuring uniqueness, transparency, and secure ownership transfers.

## Key Features

- **NFT Creation:** Users can mint new NFTs with unique identifiers and associated metadata.
- **Ownership Management:** Smart contracts handle ownership transfers and approvals, ensuring secure and transparent transactions.
- **Event Logging:** The system logs events such as transfers, minting, burning, and approvals for auditing purposes.
- **Metadata Management:** Metadata such as name, symbol, and URI associated with each NFT are stored securely on the blockchain.

## Prerequisites

- A Stellar Testnet account with some test XLM tokens.
- Basic understanding of Rust programming and the Stellar network.
- Soroban SDK installed ([https://soroban.stellar.org/install.sh](https://soroban.stellar.org/install.sh))

## Steps to compile the contract
- Setup soroban-cli following the steps mentioned on this page - https://soroban.stellar.org/docs/getting-started/setup
- If you are a Windows user that wants to leverage Linux, please refer to this video as a guide - https://www.youtube.com/watch?v=PQA5_7m3OjQ&t=2s
- After the setup and installation of soroban-cli, run the command soroban contract build.
- After the code compilation, you will see a newly created folder named ‘target’ which contains the wasm executable.

## Usage

- After successfully compiling the contract, you will find a newly created folder named **‘target’** containing the wasm executable.
- Deploy the compiled smart contract to the Stellar network using Soroban.
- Interact with the deployed contract using Stellar accounts to mint, transfer, and manage NFTs.
- Monitor contract events for auditing and transparency purposes.
