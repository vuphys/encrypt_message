# encrypt_message

Encryption/Decryption Tool

Overview

The Encryption/Decryption Tool is a simple and user-friendly application built using Python and Tkinter. This tool allows users to encrypt and decrypt short messages using symmetric encryption, specifically with the Fernet symmetric encryption method provided by the cryptography library. The application provides functionality for generating secure keys, encrypting messages, and decrypting them back to their original form.

Features

Generate Encryption Key: Easily generate a new encryption key (in Base64 format) that can be used to encrypt and decrypt messages.
Encrypt Messages: Input a message along with a valid key to encrypt it securely.
Decrypt Messages: Input a previously encrypted message along with the key to decode it back to its original text.
User-Friendly Interface: An intuitive graphical user interface (GUI) built with Tkinter for easy navigation and usability.
Prerequisites
Before running the application, ensure you have the following installed on your system:

Python (version 3.6 or later)
The cryptography library
You can install the cryptography library using pip:

 
pip install cryptography

Usage

Launch the Application: Run the script to open the Encryption/Decryption Tool.

Generate a Key:

Click the "Generate Key" button. The generated key will appear in the input field labeled "Key (Base64)".
Encrypt a Message:

Enter your encryption key (Base64) in the "Key" field.

Type the message you wish to encrypt into the "Message" field.

Click the "Encrypt" button. The encrypted message will be displayed in the "Result" field.
Decrypt a Message:

Input the same encryption key used for the message in the "Key" field.

Enter the encrypted message into the "Message" field.

Click the "Decrypt" button. The original message will appear in the "Result" field.
Example

Input Key: b'jB9L3WgNigM6OgFqyz62zF0h3gfg5N2hPFAHey3ASwI=' (example key generated)
Original Message: Hello World

Encrypted Message: gAAAAABgRk0re... (this will vary)

Decrypted Message: Hello World

Error Handling

The tool includes error handling mechanisms that display warning messages if:

Neither a key nor a message is provided when attempting to encrypt or decrypt.

The provided key or encrypted message is invalid.

License

This tool is open-source; you are free to use and modify it as needed. Please refer to the accompanying licenses for third-party libraries.

Conclusion

The Encryption/Decryption Tool serves as a convenient application for securely encrypting and decrypting short messages, with minimal user input and a straightforward interface. Whether you need to keep a message private or simply wish to learn more about encryption techniques, this application is a helpful resource.
