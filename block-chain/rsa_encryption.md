# Implement RSA Encryption Algorithm

## Objective

The objective of this problem statement is to implement the RSA public-key cryptosystem from scratch using a programming language of your choice. This includes key generation, encryption, and decryption functionality without using any external cryptographic libraries.

## Problem Statement

You are required to write a full implementation of the RSA algorithm, covering:

- Generation of two large prime numbers
- Computation of public and private keys
- Message encryption using the public key
- Message decryption using the private key

The implementation should demonstrate a working example where a user can input a plaintext message, and your program returns the encrypted ciphertext and the decrypted original message.

## Key Features to Implement

1. **Prime Number Generation**
   - Use probabilistic methods (e.g., Miller-Rabin) or deterministic algorithms to generate large primes.

2. **Key Generation**
   - Compute modulus `n = p * q`
   - Compute Euler’s totient `φ(n) = (p-1)(q-1)`
   - Choose a public exponent `e` such that `1 < e < φ(n)` and `gcd(e, φ(n)) = 1`
   - Compute the private exponent `d` such that `d ≡ e⁻¹ mod φ(n)`

3. **Encryption**
   - Use the public key `(e, n)` to encrypt plaintext message `M` as:
     ```
     C = M^e mod n
     ```

4. **Decryption**
   - Use the private key `(d, n)` to decrypt ciphertext `C` as:
     ```
     M = C^d mod n
     ```

5. **(BONUS) String Encoding/Decoding**
   - Convert full strings to numerical format before encryption and back to readable text after decryption.

6. **(BONUS) UI or CLI Interface**
   - Provide an interface for users to enter messages and view the encrypted/decrypted results.

---

**Deliverables:**

- Full implementation of RSA key generation, encryption, and decryption.
- Sample input/output demonstrating correct encryption and decryption.
- (Optional) CLI or GUI interface for user interaction.

