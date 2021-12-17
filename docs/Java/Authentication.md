# Authentication
Authentication carries out the verification of the identity of a user or machine based on additional data like password, token etc. The Java Authentication and Authorization Services (JAAS) API can be leveraged for the authentication and the authorization process.

##  Authentication in Java

The JAAS APIs uses **pluggable login modules** to provide different and often multiple authentication mechanisms to applications. LoginContext provides this abstraction, which in turn refers to configuration and loads an appropriate LoginModule such as

- **Krb5LoginModule** - Kerberos-based authentication
- **JndiLoginModule** - username and password-based authentication backed by an LDAP store
- **KeyStoreLoginModule** - cryptographic key-based authentication