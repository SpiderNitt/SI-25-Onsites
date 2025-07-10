# Real-Time Ethereum Block & Transaction Tracker

## Objective

The objective of this problem statement is to build a real-time monitoring tool that listens to the latest blocks and transactions on the Ethereum blockchain and displays the relevant data on a live dashboard.

## Problem Statement

You are required to create a script (Node.js, Python, or similar) that connects to the Ethereum network using a WebSocket provider (e.g., via Infura, Alchemy, or local node) and listens for new blocks and transactions as they are mined.

The script should extract key details such as:
- Block number
- Timestamp
- Miner address
- Number of transactions
- Gas used
- Selected transaction details (e.g., sender, recipient, value, gas)

This data should be presented on a simple web-based dashboard that updates in real time as new blocks are received.

## Key Features to Implement

1. **WebSocket Connection to Ethereum Network**
   - Subscribe to `newBlockHeaders` or `pendingTransactions` using Web3.js or ethers.js.
   - Retrieve full block and transaction data upon receipt.

2. **Block & Transaction Parsing**
   - Extract and format key data fields from blocks and transactions.
   - Optionally filter or limit the number of transactions shown.

3. **Live Dashboard**
   - Create a frontend (e.g., using React, Vue, or plain HTML/JS) to display data.
   - Use WebSockets or polling to reflect updates in real time.

4. **(BONUS) Persist Data**
   - Save block/transaction data to a lightweight database (e.g., SQLite, MongoDB).
   - Allow viewing recent block history.

5. **(BONUS) Filter Features**
   - Add filters to show only transactions with high value or specific addresses.

---

**Deliverables:**

- A script that listens to the Ethereum blockchain in real time.
- A responsive dashboard that displays updated block and transaction information.
- (Optional) Data persistence and filtering utilities.

