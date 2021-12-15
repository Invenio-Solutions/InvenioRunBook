# Cryptography
Cryptography is the cornerstone of security features in Java. This refers to tools and techniques for secure communication in the presence of adversaries.
## Cryptography in Java
The Java Cryptographic Architecture (JCA) provides a framework to access and implement cryptographic functionalities in Java, including:

- Digital signatures
- Message digests
- Symmetric and asymmetric ciphers
- Message authentication codes
- Key generators and key factories

Java makes the best use of **Provider-based implementations** for cryptographic functions and includes built-in providers for cryptographic algorithms like RSA, DSA, AND AES. These alogithms can be used to add more security to data in resr, in use or in motion. It is used to store user passwords and later used by authentication process. But the plain text of password will compromise the security. To overcome this challenge, *SHA1 algorithm* is used to scramble the password and then store it. This process is reffered to as *cryptographic hash function*.