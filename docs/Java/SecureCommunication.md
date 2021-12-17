# Secure Communication

Java provides APIs to [secure network communication](https://docs.oracle.com/javase/9/security/java-secure-socket-extension-jsse-reference-guide.htm#JSSEC-GUID-93DEEE16-0B70-40E5-BBE7-55C3FD432345) with encryption, message integrity, and client-server authentication:
- **SSL/TLS**: SSL/TSL, provide security through data encryption and public-key infrastructure over untrusted network communication. Java provides support of SSL/TLS through SSLSocket defined in the package “java.security.ssl“.
- **SASL**: Simple Authentication and Security Layer (SASL) is a standard for authentication between client and server. Java supports SASL as part of the package “java.security.sasl“.
- **GGS-API/Kerberos**: Generic Security Service API (GSS-API) offers uniform access to security services over a variety of security mechanisms like Kerberos v5. Java supports GSS-API as part of the package “java.security.jgss“.