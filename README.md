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

<img src="https://github.com/user-attachments/assets/10538c8f-25ab-49e8-a999-7159f0891f12" width=400>

1. The *secrets* module is specifically designed for generating cryptographically secure random numbers, making it ideal for creating secure passwords and other sensitive data. It provides a higher level of randomness and security than the standard random module.
2. The *string* module provides constants for commonly used character sets, like all uppercase and lowercase letters (string.ascii_letters), digits (string.digits), and punctuation (string.punctuation). This allows you to easily create a pool of characters for generating diverse passwords.
3. The *hashlib* module provides access to secure hash functions, like SHA-256. These functions take an input and generate a fixed-length hash, useful for securely storing passwords by creating unique representations that can’t be reversed to reveal the original input.

## Password Generator Function

<img src="https://github.com/user-attachments/assets/18908f6f-18d3-4ce2-a31f-ab57b2b036f4" width=600>

1. We create a string *characters* containing all possible characters for our password.
2. We use *secrets.choice()* which will randomly select characters from this string. It's more secure than using *random.choice()* because it uses the operating system’s cryptographically secure random number generator.
3. Joining all selected characters into a single string with *''.join(...)*, resulting in our password.

## Hashing Password Function 

<img src="https://github.com/user-attachments/assets/23b7ab8b-8d6a-4b17-8646-12618e1e8819" width=500>

The *hash_password* function hashes a password using SHA-256, providing a secure, unique representation.
1. password.encode(): Converts the password to bytes since SHA-256 requires byte input.
2. hashlib.sha256(...).hexdigest():
- hashlib.sha256(...) computes the SHA-256 hash of the password.
- .hexdigest() converts the hash to a readable hexadecimal string.
3. Finally, return sha_signature will output a hashed, hexadecimal representation when ran.

## Password Output Function

<img src="https://github.com/user-attachments/assets/22b7ebe4-8bb7-4cc2-bb28-a1e74d5edab0" width=500>

This lets you see the password created by the generator.

<img src="https://github.com/user-attachments/assets/9b95660a-31e0-4e10-a0f3-04a75480e840" width=500>

This hash is a secure, irreversible representation of the password, ideal for storage. Make sure to keep it safe!
