# PKI Support in Java
Java platform has APIs to [facilitate the creation, storage, and validation of digital certificates:](https://docs.oracle.com/javase/9/security/java-pki-programmers-guide.htm#JSSEC-GUID-650D0D53-B617-4055-AFD3-AF5C2629CBBF)
- **KeyStore** : Java provides the KeyStore class for persistent storage of cryptographic keys and trusted certificates. KeyStore can represent both key-store and trust-store files. These files have similar content but vary in their usage.

-  **CertStore** : Java has the CertStore class, which represents a public repository of potentially untrusted certificates and revocation lists. We need to retrieve certificates and revocation lists for certificate path building amongst other usages.

Java have **cacerts** (built-in-trust=store) that contains certificates for well known CAs.

## Java Tools for PKI 
Java has some tools to facilitate trusted communication:
- There is a built-in tool called “keytool” to create and manage key-store and trust-store
- There is also another tool “jarsigner” that we can use to sign and verify JAR files

## Working with Certificates in Java

To establish a secure connection using SSL in Java we need specified certificates.

**Present Certificate** — We need to present a valid certificate to another party. For this, key-store file should be loaded, where we must have our public keys:

**Verify Certificate** — We also need to verify the certificate presented by another party in the communication. For this we need to load the trust-store, where we must have previously trusted certificates from other parties: