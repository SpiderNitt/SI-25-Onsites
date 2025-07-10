# Create and Deploy ERC20/721 Tokens using OpenZeppelin

## Objective

The objective of this problem is to create custom ERC20 and ERC721 tokens using OpenZeppelin’s secure and audited smart contract library. You will implement, test, and deploy these tokens on a local or testnet blockchain, ensuring proper functionality and standard compliance.

## Problem Statement

You are required to use the OpenZeppelin Contracts library to create and deploy both of the following:

- **ERC20 Token**: A fungible token with standard features like transfer, approval, and balance tracking.
- **ERC721 Token**: A non-fungible token (NFT) with unique identifiers and metadata support.

## Key Features to Implement

1. **Token Implementation**
   - Use OpenZeppelin Contracts to create ERC20 or ERC721 token contracts.
   - Customize token details: name, symbol, initial supply (for ERC20), and metadata URI (for ERC721).

2. **Deployment Script**
   - Write deployment scripts using your preferred framework (e.g., Hardhat, Foundry, or Truffle).
   - Ensure deploy scripts are configurable (e.g., via `.env` for private keys and RPC URLs).

3. **Token Interaction**
   - Allow token transfers, minting, and (for NFTs) metadata retrieval.
   - Validate behavior through test scripts or CLI interaction (e.g., using `cast`, `ethers.js`, etc.).

4. **(BONUS) Web Interface**
   - Build a basic frontend to interact with the deployed tokens (optional).
   - Display balances, allow transfers, and minting for both token types.

---

**Deliverables:**

- A working smart contract using OpenZeppelin.
- A deployment script with configurable parameters.
