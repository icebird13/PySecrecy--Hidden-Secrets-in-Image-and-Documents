# PySecrecy--Hidden-Secrets-in-Image-and-Documents
This application allows users to securely hide and reveal messages within images or text documents using steganography and AES encryption.

Key Features:
1. AES Encryption:
Messages are encrypted using AES (Advanced Encryption Standard) in CBC (Cipher Block Chaining) mode for enhanced security.
A secure key is derived using SHA-256 hashing of a password.
Encrypted messages include the Initialization Vector (IV) and ciphertext to ensure proper decryption.

2. Steganography:
Encrypted messages can be hidden within image files (PNG, JPG) using LSB (Least Significant Bit) steganography.
Text documents store encrypted messages in an alternate data stream (ADS) for added security.

3. File Management:
Load, display, and manage images or text documents.
Save modified files with hidden messages or decrypted content.

4. Timer and Performance Metrics:
Tracks and displays message size, encryption time, and decryption time for efficiency monitoring.

5. User-Friendly Interface:
Built with Tkinter for a visually intuitive GUI.
Allows users to easily load files, hide/reveal messages, and save results.

