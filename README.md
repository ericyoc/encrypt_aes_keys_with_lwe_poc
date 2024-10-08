# Encrypt AES Keys with LWE

## Overview

This project demonstrates a multi-level encryption approach for securing images by combining traditional cryptographic techniques with post-quantum encryption methods. 

## Motivating Articles

Budroni, A., & Mårtensson, E. (2024). Further improvements of the estimation of key enumeration with applications to solving LWE. Cryptography and Communications, 1-20. https://link.springer.com/article/10.1007/s12095-024-00722-1

Verchyk, D., & Sepúlveda, J. (2023). A practical study of post-quantum enhanced identity-based encryption. Microprocessors and Microsystems, 99, 104828. https://doi.org/10.1016/j.micpro.2023.104828

Rawal, B. S., & Biswas, A. (2024). A comprehensive survey of post-quantum cryptography and its implications. Engineering Science & Technology, 256-269. https://ojs.wiserpub.com/index.php/EST/article/view/4169


## Results
![](https://github.com/ericyoc/encrypt_aes_keys_with_lwe_poc/blob/main/results_table.jpg)

### The Python code provided implements the following steps:

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

## License
Copyright 2024 Eric Yocam

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
