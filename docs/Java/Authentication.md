---
sidebar_position: 3
---
# Authentication
Authentication carries out the verification of the identity of a user or machine based on additional data like password, token, or a variety of other credentials available.
##  Authentication in Java
Java APIs uses **pluggable login modules** to provide different and often multiple authentication mechanisms to applications. LoginContext provides this abstraction, which in turn refers to configuration and loads an appropriate LoginModule.
Default Java login modules:
- **Krb5LoginModule** - Kerberos-based authentication
- **JndiLoginModule** - username and password-based authentication backed by an LDAP store
- **KeyStoreLoginModule** - cryptographic key-based authentication