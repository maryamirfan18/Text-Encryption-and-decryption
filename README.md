# Text-Encryption-and-Decryption
This code is a simple implementation of **Caesar Cipher**, a basic encryption technique where each letter in the message is shifted by a certain number of positions (defined by the key) in the alphabet. The process is reversible by shifting in the opposite direction to decrypt the message.

### Code Overview

1. **Encryption (`encrypt(message, key)`)**:
   - The function takes two inputs: "message" (the plain text to encrypt) and "key"(the number of positions to shift the letters).
   - It loops through each character of the message. If the character is a letter:
     - It checks if it's lowercase or uppercase.
     - For lowercase letters, it shifts within the lowercase range ('a' to 'z`), and for uppercase, it shifts within the uppercase range ('A' to 'Z').
     - Non-alphabetic characters are left unchanged.
   - The encrypted message is returned.

   **Key point**: Shifting is done using the ASCII values (ord()) of characters and then converting them back using chr(). The shift is controlled by the key, and % 26 ensures that the shift wraps around the alphabet.

2. **Decryption (`decrypt(encrypted_message, key)`)**:
   - The decryption process mirrors encryption but shifts letters backward (by subtracting the key).
   - Like encryption, it handles both lowercase and uppercase letters, and non-alphabetic characters are returned unchanged.
   - After looping through each character and reversing the shift, the original message is restored.

3. **Main Function (`main()`)**:
   - This is the entry point of the program where:
     - The user is prompted to enter a message and a key (0-25).
     - The message is passed to the `encrypt()` function to get the encrypted message.
     - The encrypted message is then passed to the `decrypt()` function to retrieve the original message.
   - The encrypted and decrypted messages are displayed.

### Example:
- If you input `"Hello World"` with a key of `3`, the encryption will shift each letter by 3 positions:
  - `"H"` becomes `"K"`, `"e"` becomes `"h"`, etc.
  - The encrypted message might be `"Khoor Zruog"`.
- Decrypting it with the same key shifts the letters back, restoring the original message: `"Hello World"`.

### Conclusion:
This Caesar Cipher implementation is a simple and elegant way to illustrate basic encryption and decryption concepts. It demonstrates how messages can be hidden (encrypted) and later revealed (decrypted) using a shared secret (the key).
