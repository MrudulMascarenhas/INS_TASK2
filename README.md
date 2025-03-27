# Secure Key Management System

## Overview
The Secure Key Management System (SKMS) is a cryptographic solution designed to handle both symmetric and asymmetric encryption for secure communication and data protection. It supports AES-GCM for encryption and integrity verification, RSA for public key infrastructure (PKI), Diffie-Hellman for secure key exchange, and a key revocation mechanism to prevent unauthorized access to compromised keys.

## Features
- **AES-GCM Symmetric Encryption:** Secure data encryption with integrity verification.
- **RSA Public Key Infrastructure (PKI):** Asymmetric encryption for secure key distribution and authentication.
- **Diffie-Hellman Key Exchange:** Secure shared secret generation over an untrusted network.
- **Key Revocation System:** Revoke compromised keys to prevent unauthorized use.
- **Security Considerations:** Protection against man-in-the-middle (MITM) attacks, key compromise, and unauthorized access.

## Installation
### Prerequisites
- Python 3.x
- Required libraries:
  ```bash
  pip install cryptography
  ```
  
## Usage
Clone the Repository
```bash
git clone https://github.com/MrudulMascarenhas/INS_TASK2.git
```

### Available Functionalities
1. **AES-GCM Encryption & Decryption:**
   - Encrypts a user-provided message using AES-GCM with authentication tags.
   - Decrypts the encrypted data securely.

2. **RSA Key Pair Generation:**
   - Generates a public-private RSA key pair for secure communication.
   - Public keys can be shared for encryption, while private keys remain secure.

3. **Diffie-Hellman Key Exchange:**
   - Generates private-public key pairs for two parties.
   - Establishes a shared secret key securely over an untrusted network.

4. **Key Revocation System:**
   - Maintains a list of revoked keys.
   - Allows users to revoke keys manually and check key status before use.

5. **Exit:**
   - Terminates the program.

## System Architecture
The SKMS follows a modular architecture with the following components:
- `SymmetricKeyManager`: Manages AES-GCM encryption and decryption.
- `PKIManager`: Handles RSA key generation and authentication.
- `DiffieHellmanKeyExchange`: Enables secure shared key generation.
- `KeyRevocation`: Manages revoked keys and prevents unauthorized access.
- `main()`: Provides an interactive CLI for user interaction.

## Security Considerations
- **MITM Attack Prevention:**
  - Diffie-Hellman key exchange ensures secure shared key generation without exposure.
  - RSA encryption secures key transmission and authentication.
  - Digital signatures verify authenticity and prevent impersonation.

- **Key Compromise Mitigation:**
  - AES-GCM uses an Initialization Vector (IV) to prevent predictable encryption patterns.
  - Key revocation mechanism ensures compromised keys are invalidated.
  - Periodic key rotation limits the lifespan of keys, reducing attack exposure.

## Output Example
```
Secure Key Management System
1. Encrypt & Decrypt using AES-GCM
2. Generate RSA Keys
3. Perform Diffie-Hellman Key Exchange
4. Revoke & Check Key Status
5. Exit
OUTPUT:
Encryption & Decryption
Key ID: 65aa4e553e8d7a45
Encrypted Data: 0ba4e2f1093852ebb1e3eafa
Decrypted Message: attackatonce
RSA Key Generation
RSA Keys generated for User: key123
Key Revocation
Key 'key123' has been revoked.
```
### **Run the Code in Google Colab**
You can also execute the code using Google Colab:
[Secure Key Management System on Google Colab](https://colab.research.google.com/drive/1U61kd7kzSph7CEwnSTCn-VmhVSiG3lEU?usp=sharing)
## License
This project is licensed under the MIT License.



