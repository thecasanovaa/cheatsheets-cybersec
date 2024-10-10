# Cryptography Cheat Sheet

## 1. **Types of Cryptography**
- **Symmetric Key Cryptography**: Uses the same key for both encryption and decryption.
  - Examples: AES, DES, 3DES
- **Asymmetric Key Cryptography**: Uses a public key for encryption and a private key for decryption.
  - Examples: RSA, ECC, DSA

## 2. **Common Algorithms**

### Symmetric Key Algorithms:
| Algorithm | Key Size | Block Size | Use Case        |
| --------- | -------- | ---------- | --------------- |
| AES       | 128, 192, 256 bits | 128 bits | Data Encryption |
| DES       | 56 bits  | 64 bits    | Legacy systems  |
| 3DES      | 168 bits | 64 bits    | Financial industry (now deprecated) |

### Asymmetric Key Algorithms:
| Algorithm | Key Size | Security Level  | Use Case              |
| --------- | -------- | --------------- | --------------------- |
| RSA       | 1024, 2048, 4096 bits | Strong security for large key sizes | Digital Signatures, Encryption |
| ECC       | 160, 224, 256 bits    | Same security as RSA with smaller keys | Secure messaging, SSL/TLS |

## 3. **Cryptographic Hash Functions**
- **Purpose**: Generate a fixed-size hash from variable-size input, ensuring data integrity.
  - **MD5**: 128-bit hash, insecure due to vulnerabilities.
  - **SHA-1**: 160-bit hash, deprecated due to collision attacks.
  - **SHA-256**: 256-bit hash, widely used in blockchain and digital certificates.

## 4. **Encryption Modes**
- **ECB (Electronic Codebook)**: Simplest mode, but vulnerable to pattern attacks.
- **CBC (Cipher Block Chaining)**: More secure than ECB by introducing an initialization vector (IV).
- **GCM (Galois/Counter Mode)**: Provides both encryption and message integrity.

## 5. **Digital Signatures**
- **Purpose**: Provide message authentication, integrity, and non-repudiation.
- **How it works**:
  - Hash the message.
  - Encrypt the hash with the sender's private key.
  - Receiver decrypts with sender's public key and compares hashes.

## 6. **Key Exchange Protocols**
- **Diffie-Hellman**: Allows two parties to exchange keys securely over an insecure channel.
- **Elliptic Curve Diffie-Hellman (ECDH)**: Uses ECC for smaller, faster key exchanges.

## 7. **Best Practices**
- Use **AES-256** for symmetric encryption.
- Use **RSA-2048** or **ECC** for public-key cryptography.
- Avoid **MD5** and **SHA-1**; use **SHA-256** or better.
- Always use **salting** with passwords before hashing.
- Use authenticated encryption modes like **GCM** to ensure data integrity.

## 8. **Public Key Infrastructure (PKI)**
- **Components**:
  - **Certificate Authority (CA)**: Issues digital certificates.
  - **Registration Authority (RA)**: Verifies user identities before issuing certificates.
  - **Digital Certificate**: Contains public key and identity info, signed by a CA.
  - **Certificate Revocation List (CRL)**: List of revoked certificates.

## 9. **Common Attacks**
- **Brute Force Attack**: Attempts to guess the key by trying all possibilities.
- **Man-in-the-Middle Attack**: Intercepting communication between two parties.
- **Replay Attack**: Reusing captured messages to fool the system.
- **Side-Channel Attack**: Gaining information from the physical implementation of a cryptosystem.

---

## 10. **Resources**
- [Cryptography Concepts](https://en.wikipedia.org/wiki/Cryptography)
- [AES Algorithm](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard)
- [RSA Algorithm](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
