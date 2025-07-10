# Problem Statement: TCP-Based Multi-Client Chat Server with Optional Encryption

## Objective

Develop a TCP-based chat server and client system in Python that supports real-time messaging between multiple clients. The system should provide two modes of communication:
1. **Unencrypted (Plaintext)** for testing and debugging.
2. **Encrypted** using basic symmetric key encryption (e.g., AES) for secure communication.

---

## Functional Requirements

### 1. Server Functionality

- Accept and manage multiple client connections concurrently.
- Broadcast messages from any client to all connected clients.
- Assign unique usernames or IDs to each client upon connection.
- Optionally support server-side logging of all messages.

### 2. Client Functionality

- Connect to the server using TCP sockets.
- Send and receive messages in real-time.
- Handle server disconnects or errors gracefully.
- Allow toggling between encrypted and unencrypted message modes.

### 3. Encryption Support (Optional Toggle)

- Use symmetric encryption (e.g., AES via `cryptography` or `pycryptodome`) for encrypted communication.
- The server and client must share a pre-shared key (PSK) for encryption.
- Encryption can be enabled/disabled via command-line argument or config flag.

---

## Non-Functional Requirements

- The solution should support concurrent clients using `threading` or `asyncio`.
- All code should be cross-platform (Windows, macOS, Linux).
- Encrypted messages must be decrypted correctly and efficiently without lag.

---

## Deliverables

- `server.py`: TCP chat server that accepts multiple clients.
- `client.py`: TCP chat client to send/receive messages.
- Support for:
  - Encrypted and unencrypted modes
  - Graceful error handling
  - Simultaneous multiple client support
- A sample pre-shared encryption key (for demo/testing)
- Logs or screenshots demonstrating encrypted and unencrypted communication

---

## Approach

### Server (`server.py`)

- Use the `socket` module to create a TCP server.
- Use `threading.Thread` to handle multiple client sockets.
- Implement a simple broadcast function to relay messages.
- Optionally wrap incoming/outgoing messages with encryption/decryption functions.

### Client (`client.py`)

- Connect to the server via TCP socket.
- Use two threads: one for receiving, one for sending messages.
- Read messages from user input and send to the server.
- Decrypt and display incoming messages if encryption is enabled.

### Encryption (Optional)

- Use a symmetric algorithm (e.g., AES in CBC or GCM mode).
- The encryption module will include:
  - `encrypt_message(message, key)`
  - `decrypt_message(ciphertext, key)`
- Base64 encoding may be used for safe socket transmission.