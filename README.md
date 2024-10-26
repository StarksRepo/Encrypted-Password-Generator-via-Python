# Encrypted-Password-Generator-via-Python
## Description
This project is a Python-based tool that generates secure, randomized passwords using the secrets module, designed for cryptographic-grade randomness. Each generated password is then hashed with SHA-256, providing an irreversible, secure representation suitable for safe storage. The project illustrates principles of cybersecurity like secure password practices, hashing for data integrity, and cryptographic modules in Python.
## Tools Used
* Python
* Visual Studio Code
## Entire Encrypted Password Generator Code
* First I will post the entire code for you to see, afterwards I will be breaking it down section by section.
<img src="https://github.com/user-attachments/assets/9c833912-0d3b-4404-8f6d-9649ee886ce4" width=500>

## Modules Imported

<img src="https://github.com/user-attachments/assets/10538c8f-25ab-49e8-a999-7159f0891f12" width =400>

1. The *secrets* module is specifically designed for generating cryptographically secure random numbers, making it ideal for creating secure passwords and other sensitive data. It provides a higher level of randomness and security than the standard random module.
2. The *string* module provides constants for commonly used character sets, like all uppercase and lowercase letters (string.ascii_letters), digits (string.digits), and punctuation (string.punctuation). This allows you to easily create a pool of characters for generating diverse passwords.
3. The *hashlib* module provides access to secure hash functions, like SHA-256. These functions take an input and generate a fixed-length hash, useful for securely storing passwords by creating unique representations that can’t be reversed to reveal the original input.
