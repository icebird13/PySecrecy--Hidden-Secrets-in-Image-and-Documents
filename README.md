How to use (for images section): 
1. Select an image, write your message and press the checkbox (full file encryption/decryption), it hides the image even in your computer so you can't view it. It will only open along with the message in the application.
2. To decrypt the whole encrypted image (if you selected the checkbox earlier), select it in the encrypted_images folder and press the checkbox again and then click "show message". it will decrypt and be available in decrypted_images folder.

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
-----------------------------------
File Encryption & Decryption
1. Encrypt File (AES Encryption)
Function: encrypt_file(input_file_path, key, algorithm="AES")

Purpose:
Securely lock any file (image or text) so that only someone with the correct key (password) can unlock it.
How it works:
Reads the content of the file you selected.
Converts the password into a secure encryption key using SHA-256.
Encrypts the file using AES encryption in CBC mode.
Adds a random IV (Initialization Vector) to make the encryption stronger.
Saves the encrypted file with a .enc extension.

Use Case: Useful when you want to protect a file before hiding it in an image or sending it securely.

2. Decrypt File (AES Decryption)
Function: decrypt_file(encrypted_file_path, key, algorithm="AES")
Purpose:
Unlocks the encrypted file and restores the original content using the correct key.
How it works:
Reads the locked file.
Extracts the IV and encrypted data.
Converts your password into a key (same method as encryption).
Decrypts the content using AES + CBC mode.
Saves the decrypted output file with a prefix decrypted_.
If the wrong key is given, it won’t work — ensuring security.

Image Quality Checker (After Steganography)
3. PSNR & SSIM Calculator
Function: calculate_psnr(original_image_path, stego_image_path)

Purpose:
Compares the original image and the image with the hidden message to check how much they differ in terms of quality.

Outputs:
PSNR (Peak Signal-to-Noise Ratio):
Measures if the image is still visually clear after hiding data.
Higher value = Better quality.

SSIM (Structural Similarity Index):
Checks if the image structure or patterns have changed.
Value near 1 = Almost identical.

This helps ensure that hiding a message doesn’t noticeably damage the image.

--------------------

