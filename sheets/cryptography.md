# Cryptography Cheat Sheet

## 1. **Types of Cryptography** <br>
- **Symmetric Key Cryptography**: Uses the same key for both encryption and decryption <br>
  - Examples: AES, DES, 3DES <br>
- **Asymmetric Key Cryptography**: Uses a public key for encryption and a private key for decryption. <br>
  - Examples: RSA, ECC, DSA <br>

## 2. **Common Algorithms** <br>

### Symmetric Key Algorithms: <br>
| Algorithm | Key Size | Block Size | Use Case        |
| --------- | -------- | ---------- | --------------- |
| AES       | 128, 192, 256 bits | 128 bits | Data Encryption |
| DES       | 56 bits  | 64 bits    | Legacy systems  |
| 3DES      | 168 bits | 64 bits    | Financial industry (now deprecated) |

### Asymmetric Key Algorithms: <br>
| Algorithm | Key Size | Security Level  | Use Case              |
| --------- | -------- | --------------- | --------------------- |
| RSA       | 1024, 2048, 4096 bits | Strong security for large key sizes | Digital Signatures, Encryption |
| ECC       | 160, 224, 256 bits    | Same security as RSA with smaller keys | Secure messaging, SSL/TLS |

## 3. **Cryptographic Hash Functions** <br>
- **Purpose**: Generate a fixed-size hash from variable-size input, ensuring data integrity. <br>
  - **MD5**: 128-bit hash, insecure due to vulnerabilities. <br>
  - **SHA-1**: 160-bit hash, deprecated due to collision attacks. <br>
  - **SHA-256**: 256-bit hash, widely used in blockchain and digital certificates. <br>

## 4. **Encryption Modes** <br>
- **ECB (Electronic Codebook)**: Simplest mode, but vulnerable to pattern attacks. <br>
- **CBC (Cipher Block Chaining)**: More secure than ECB by introducing an initialization vector (IV). <br>
- **GCM (Galois/Counter Mode)**: Provides both encryption and message integrity. <br>

## 5. **Digital Signatures** <br>
- **Purpose**: Provide message authentication, integrity, and non-repudiation. <br>
- **How it works**: <br>
  - Hash the message. <br>
  - Encrypt the hash with the sender's private key. <br>
  - Receiver decrypts with sender's public key and compares hashes. <br>

## 6. **Key Exchange Protocols** <br>
- **Diffie-Hellman**: Allows two parties to exchange keys securely over an insecure channel. <br>
- **Elliptic Curve Diffie-Hellman (ECDH)**: Uses ECC for smaller, faster key exchanges. <br>

## 7. **Best Practices** <br>
- Use **AES-256** for symmetric encryption. <br>
- Use **RSA-2048** or **ECC** for public-key cryptography. <br>
- Avoid **MD5** and **SHA-1**; use **SHA-256** or better. <br>
- Always use **salting** with passwords before hashing. <br>
- Use authenticated encryption modes like **GCM** to ensure data integrity. <br>

## 8. **Public Key Infrastructure (PKI)** <br>
- **Components**:
  - **Certificate Authority (CA)**: Issues digital certificates. <br>
  - **Registration Authority (RA)**: Verifies user identities before issuing certificates. <br>
  - **Digital Certificate**: Contains public key and identity info, signed by a CA. <br>
  - **Certificate Revocation List (CRL)**: List of revoked certificates. <br>

## 9. **Common Attacks** <br>
- **Brute Force Attack**: Attempts to guess the key by trying all possibilities. <br>
- **Man-in-the-Middle Attack**: Intercepting communication between two parties. <br>
- **Replay Attack**: Reusing captured messages to fool the system. <br>
- **Side-Channel Attack**: Gaining information from the physical implementation of a cryptosystem. <br>

---

## 10. **Resources** <br>
- [Cryptography Concepts](https://en.wikipedia.org/wiki/Cryptography) <br>
- [AES Algorithm](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) <br>
- [RSA Algorithm](https://en.wikipedia.org/wiki/RSA_(cryptosystem)) <br>
