# Encrypt AES Keys with LWE

## Overview

This project demonstrates a multi-level encryption approach for securing images by combining traditional cryptographic techniques with post-quantum encryption methods. The Python code provided implements the following steps:

1. **2D Discrete Wavelet Transform (DWT):** Decomposes the image into different frequency components.
2. **AES Encryption:** Encrypts the LL (approximation) coefficients from the DWT.
3. **LWE Encryption:** Applies post-quantum Learning with Errors (LWE) encryption to the AES ciphertext.

This multi-layered approach ensures enhanced security by leveraging both classical and quantum-resistant encryption techniques.

## Key Concepts

### 1. 2D Discrete Wavelet Transform (DWT)

- **Purpose:** Decomposes an image into different frequency components: LL (approximation) and LH, HL, HH (detail) coefficients.
- **LL Coefficients:** Represent the low-frequency, smooth aspects of the image.
- **LH, HL, HH Coefficients:** Capture high-frequency details, including edges and textures in various directions.

### 2. AES Encryption

- **Purpose:** Encrypts the LL coefficients to protect the primary information of the image.
- **Key Sizes:** Supports 128, 192, and 256 bits, offering different levels of security.
- **Operation:** Converts LL coefficients into ciphertext using the AES algorithm.

### 3. LWE Encryption

- **Purpose:** Adds a post-quantum layer of security by encrypting the AES ciphertext.
- **Rationale:** LWE encryption is resistant to quantum computing threats, providing future-proof security.
- **Parameters:** Includes `n` (dimension), `q` (modulus), and `sigma` (error distribution) for generating LWE keys and performing encryption.

## Why Encrypt AES Keys with LWE?

### Future-Proof Security
- **Quantum Resistance:** While AES encryption is robust, it is vulnerable to quantum attacks. LWE encryption is designed to be secure against such threats, ensuring that encryption remains effective even as quantum computing advances.

### Enhanced Security Model
- **Layered Security:** Encrypting AES keys with LWE adds an additional security layer. Even if the AES ciphertext is compromised, LWE encryption protects the AES keys, making unauthorized access significantly more difficult.

### Research and Development
- **Advancing Cryptographic Techniques:** Implementing LWE encryption helps in understanding its practicality and performance. This approach contributes to the development of advanced cryptographic methods and their real-world applications.

## Disclaimer
The Python code and repository contents are for research purpose only.
