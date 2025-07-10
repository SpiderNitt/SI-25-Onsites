# Set Up a Local Blockchain with Foundry

## Objective

The objective of this problem is to set up a local Ethereum-compatible blockchain development environment using **Foundry**. Foundry is a fast, portable, and modular toolkit for Ethereum application development, enabling smart contract compilation, deployment, testing, and interaction.

## Problem Statement

You are required to set up a full local blockchain development stack using Foundry. This includes installing the toolchain (`forge`, `cast`, `anvil`), initializing a Foundry project, running a local Ethereum node, writing and compiling smart contracts, deploying them to the local chain, and testing them with Solidity-based test scripts.

## Key Features to Implement

1. **Foundry Toolchain Setup**  
   Install and verify `forge`, `cast`, and `anvil` tools.

2. **Project Initialization**  
   Create a new Foundry project with a modular directory structure (`src/`, `script/`, `test/`).

3. **Local Blockchain with Anvil**  
   Run a local JSON-RPC server with pre-funded accounts to simulate an Ethereum environment.

4. **Contract Compilation & Deployment**  
   Write a simple smart contract, compile it, and deploy it using a deploy script.

5. **Smart Contract Testing**  
   Write unit tests in Solidity and execute them using `forge test`.

6. **(BONUS) Interact with Contracts via CLI**  
   Use `cast` to query or invoke smart contract functions directly from the command line.

---

**Deliverable:** A functioning local blockchain environment with a deployed smart contract and passing test cases, all within a structured Foundry project.

