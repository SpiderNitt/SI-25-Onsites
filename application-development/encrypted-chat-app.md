# End-to-End Encrypted Chat App

## Objective

The goal is to build a secure messaging application that supports real-time chat between users with end-to-end encryption (E2EE). The platform ensures that messages are encrypted on the sender's side and can only be decrypted by the intended recipient. The system leverages ECDH (Elliptic-Curve Diffie-Hellman) for secure key exchange, ensuring that even the server cannot read the message contents.

## Key Features to Implement

### 1. User Authentication

**Functionality:**  
Allow users to log in or start a chat session either anonymously or with credentials.

**Requirements:**
- Support for username/password authentication.
- Option to join as an anonymous user using randomly generated ID.
- Session persistence (JWT or cookie-based sessions).
- Secure storage of user credentials with hashing (e.g., bcrypt or Argon2).
- Anonymous users should be identifiable only by their temporary IDs.

### 2. End-to-End Encryption via ECDH

**Functionality:**  
Enable secure key exchange and encrypted messaging using elliptic curve cryptography.

**Requirements:**
- Each client generates an ECDH key pair upon session start.
- Public keys are exchanged via the server at the beginning of a chat session.
- Shared secret is derived client-side using the received public key and the local private key.
- Messages are encrypted with a symmetric key derived from the shared secret (e.g., AES-GCM).
- Decryption happens only on the recipient’s device.

### 3. Real-Time Messaging

**Functionality:**  
Allow users to send and receive messages in real time.

**Requirements:**
- WebSocket-based communication for low-latency messaging.
- Text messages are encrypted on the sender's end before transmission.
- Decryption happens only after message receipt on the client-side.
- Support message delivery status (sent, delivered, seen).

### 4. Secure Key Handling

**Functionality:**  
Safeguard private keys and derived secrets from unauthorized access.

**Requirements:**
- Private keys are stored only in memory and never transmitted.
- Implement key rotation or regeneration on session expiration.
- Provide visual indicators or warnings when encryption is compromised (e.g., mismatched keys).

### 5. Anonymous Mode

**Functionality:**  
Allow users to chat without registration.

**Requirements:**
- Generate temporary anonymous IDs (e.g., UUIDs).
- Session is volatile and expires after a period of inactivity.
- Anonymous users should still benefit from full E2EE.

### 6. Optional Enhancements

**Functionality:**  
Add advanced features for usability and stronger privacy.

**Recommendations:**
- Forward secrecy via ephemeral keys.
- Encrypted chat history saved locally or via secure backup (optional).
- QR code or URL-based contact sharing for key exchange.
- Self-destructing messages and read receipts.
- Support for image/file encryption and transfer.
- Integration of biometric or PIN unlock for local decryption.

---

**References:**
- ECDH Key Exchange: [Wikipedia](https://en.wikipedia.org/wiki/Elliptic-curve_Diffie–Hellman)
- WebSocket Protocol: [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
