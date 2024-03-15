# PFAF-Encryption

PFAF Encryption is a novel encryption technique that combines the principles of fractal mathematics and cryptography to enhance the security of token embeddings in artificial intelligence (AI) systems. This project provides an implementation of the PFAF encryption algorithm in Python.

Overview
The PFAF encryption algorithm leverages fractal activation functions to generate unique and complex embeddings for input tokens. These fractal embeddings are then encrypted using the Advanced Encryption Standard (AES) in Cipher Block Chaining (CBC) mode. The resulting encrypted tokens provide an additional layer of security, making it difficult for unauthorized parties to access or manipulate the underlying data.

Features
Fractal embedding generation using the Julia fractal activation function
Encryption of fractal embeddings using AES-CBC
Decryption of encrypted tokens to retrieve the original fractal embeddings
Nearest neighbor search for approximate inverse transformation
Customizable embedding size and maximum iterations for fractal computation

Installation

Clone the repository

Install the required dependencies:

pip install numpy pycryptodome

Usage

Import the necessary functions:

from pfaf_encryption import apply_pfaf, encrypt_pfaf_embedding, decrypt_pfaf_embedding, generate_encrypted_token, decrypt_token, pfaf_dict

Generate fractal embeddings for tokens:

token = "Hello, World!"
pfaf_embedding = apply_pfaf(token)

Encrypt the fractal embedding:

encryption_key = get_random_bytes(32)
encrypted_token = encrypt_pfaf_embedding(pfaf_embedding, encryption_key)

Decrypt the encrypted token:

decryption_key = encryption_key
decrypted_embedding = decrypt_pfaf_embedding(encrypted_token, decryption_key)

Generate encrypted tokens for a dictionary of tokens:

token_dict = {"apple": 0, "banana": 1, "cherry": 2}
pfaf_embeddings = pfaf_dict(token_dict)

For detailed usage examples and function descriptions, please refer to the documentation.

Contributing
Contributions are welcome! If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request.

License
This project is currently only available for individual licensing.

Acknowledgements

The PFAF encryption algorithm is based on the research involving Calculus based PFAF Fractals by Richard Aragon.
The AES encryption implementation utilizes the PyCryptodome library.

1. Initialization:
   - Define a set of fractal activation functions (P-FAF) for embedding: {f₁, f₂, ..., fₙ}.
   - Generate or obtain the encryption key and decryption key.
   - Initialize the AI model with P-FAF embedding layers.

2. Token Generation with P-FAF Embedding:
   - For each input token x:
     - Apply the P-FAF functions to generate the fractal embedding f(x).
     - Convert the fractal embedding f(x) to a byte string.
     - Pad the byte string to a multiple of the AES block size (16 bytes) using a standard padding scheme (e.g., PKCS7).
     - Generate a random initialization vector (IV) of the same size as the AES block size.
     - Create a new AES cipher object with the encryption key and IV.
     - Encrypt the padded byte string using the AES cipher in CBC mode.
     - Prepend the IV to the encrypted bytes to form the final encrypted token.

3. Model Training:
   - Train the AI model using the encrypted tokens as input.
   - The model learns to process and generate encrypted tokens.

4. Decryption Process for Authorized Receivers:
   - Upon receiving an encrypted token, extract the IV from the beginning of the token.
   - Create a new AES cipher object with the decryption key and the extracted IV.
   - Decrypt the encrypted token using the AES cipher in CBC mode.
   - Remove the padding from the decrypted bytes using the standard padding scheme.
   - Convert the decrypted bytes back to the fractal embedding array.
   - Apply the inverse of the P-FAF functions to obtain the original token or its semantic representation.

5. Error Handling:
   - Implement error handling mechanisms to detect and handle decryption errors gracefully.
   - If the decryption process encounters an error (e.g., incorrect padding), raise an appropriate exception to indicate the failure.

6. Integration with the AI Model:
   - Modify the AI model's input and output processing to handle encrypted tokens seamlessly.
   - Ensure that the model can process and generate encrypted tokens without disrupting its functionality.

7. Security Considerations:
   - Implement secure key management practices to protect the encryption and decryption keys.
   - Use secure random number generation for IV creation to ensure randomness and uniqueness.
   - Adhere to established cryptographic standards and best practices for AES encryption and padding.
   - Regularly update and patch any dependencies or libraries used in the implementation to address potential security vulnerabilities.

8. Testing and Validation:
   - Conduct thorough testing to verify the correctness and security of the encryption and decryption processes.
   - Validate that the model can successfully train and generate encrypted tokens.
   - Perform security assessments and audits to identify and mitigate any potential vulnerabilities.

9. Deployment and Monitoring:
   - Deploy the AI model with the integrated P-FAF encryption algorithm in a secure environment.
   - Implement monitoring and logging mechanisms to detect and respond to any suspicious activities or anomalies.
   - Regularly review and update the system to ensure ongoing security and reliability.

This breakdown provides a comprehensive overview of the P-FAF encryption algorithm, covering the key steps from token generation and encryption to model training, decryption, and security considerations. It's important to note that implementing a secure encryption scheme requires careful design, testing, and adherence to established cryptographic principles and best practices. Collaboration with cryptography experts and thorough security audits are recommended to ensure the robustness and reliability of the system.
