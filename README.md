Problem-1: Symmetric Encryption Service Objective
Write a program that allows users to encrypt and decrypt files using asymmetric encryption algorithm (AES). The program should generate asecure key dynamically and provide options for the user to specify the 
encryption mode.
Key Concepts: AES, key management, encryption modes.

Solution:
Certainly! Here's a breakdown of the code in text format:

1. **Importing Libraries**: 
    - The code imports the necessary modules from the `cryptography` library. Specifically, it imports `Fernet`, which is a symmetric encryption algorithm provided by the library, and `os` for interacting with the operating system.

2. **SymmetricEncryptionService Class**:
    - This class encapsulates all the functionality related to symmetric encryption.
  
3. **Constructor Method (\_\_init\_\_)**:
    - Initializes the `key` attribute as `None`.

4. **generate_key Method**:
    - Generates a new encryption key using the `Fernet.generate_key()` function and assigns it to the `key` attribute.

5. **save_key_to_file Method**:
    - Saves the encryption key to a file specified by the `key_file` parameter using the `open()` function with write binary mode (`"wb"`). It then writes the key to the file.

6. **load_key_from_file Method**:
    - Loads the encryption key from a file specified by the `key_file` parameter using the `open()` function with read binary mode (`"rb"`). It then reads the key from the file and assigns it to the `key` attribute.

7. **encrypt_file Method**:
    - Encrypts the contents of the file specified by the `input_file` parameter using the encryption key. It reads the contents of the input file, encrypts them using `Fernet.encrypt()` method, and writes the encrypted data to the file specified by the `output_file` parameter.

8. **decrypt_file Method**:
    - Decrypts the contents of the file specified by the `input_file` parameter using the encryption key. It reads the encrypted contents from the input file, decrypts them using `Fernet.decrypt()` method, and writes the decrypted data to the file specified by the `output_file` parameter.

9. **Example Usage Section**:
    - Instantiates the `SymmetricEncryptionService` class.
    - Generates a new encryption key using `generate_key()` method.
    - Saves the encryption key to a file named "encryption_key.key" using `save_key_to_file()` method.
    - Encrypts a file named "plaintext.txt" and saves the encrypted data to a file named "encrypted_file.txt".
    - Decrypts the encrypted file "encrypted_file.txt" and saves the decrypted data to a file named "decrypted_file.txt".

This code provides a basic framework for symmetric encryption using AES algorithm, allowing users to encrypt and decrypt files securely.


Problem 3: Caesar Cipher Tool
Objective: Implement a Caesar cipher tool with a user-friendly interface that allows users to encrypt and decrypt text. Include options for shifting and wrap￾around handling.
Key Concepts: Caesar cipher, modular arithmetic.

Solution:
Caesar Cipher Overview:
The Caesar cipher is a substitution cipher where each letter in the plaintext is shifted a certain number of places down or up the alphabet. For example, with a shift of 3, 'A' would be replaced by 'D', 'B' would become 'E', and so on.

Modular Arithmetic:
Modular arithmetic is used to handle wrap-around when shifting characters. In Python, you can use the modulus operator % to ensure that the shifted index wraps around within the range of the alphabet.

User Interface:
You can create a simple command-line interface (CLI) where users can interact with the Caesar cipher tool. 

Here are some features you might include:
  1.Option to choose between encryption and decryption.
  2.Prompt for the text to be encrypted or decrypted.
  3.Prompt for the shift value.
  4.Option to handle wrap-around by choosing whether to wrap around or not.
  
Implementation Steps:
Prompt the user to choose between encryption and decryption.
If encryption is chosen:
    1.Prompt the user to enter the text to be encrypted.
    2.Prompt the user to enter the shift value.
    3.Prompt the user to choose whether to handle wrap-around or not.
    4.Encrypt the text using the Caesar cipher algorithm.
    5.Display the encrypted text.
If decryption is chosen:
    1.Prompt the user to enter the text to be decrypted.
    2.Prompt the user to enter the shift value used for encryption.
    3.Prompt the user to choose whether to handle wrap-around or not.
    4.Decrypt the text using the Caesar cipher algorithm.
    5.Display the decrypted text.
    
Wrap-around Handling:
When shifting characters, ensure that the index wraps around within the range of the alphabet. 
For example, if the shift value is 3 and the character is 'Z', it should wrap around to 'C'.
