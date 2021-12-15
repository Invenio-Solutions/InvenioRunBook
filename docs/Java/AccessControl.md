# Access Control
Access Control protects sensitive resources like a filesystem or codebase from unwarranted access. This is achieved by restricting access to such resources.

## Access Control in Java
[Access Control](https://docs.oracle.com/en/java/javase/11/security/java-authentication-and-authorization-service-jaas-reference-guide.html) acheived in Java using classes Policy and Permission mediated through the SecurityManager class.

[SecurityManager](https://docs.oracle.com/javase/7/docs/api/java/lang/SecurityManager.html) is part of the “java.lang” package and is responsible for enforcing access control checks in Java.
When the class gets loaded in runtime using class loader, it grants some default permissions to the class that is encapsulated in the Permission Object. Beside these default permissions, we can also grant some security policies to this class. They are called class Policy.

During code execution, if the runtime encounters a request for a protected resource, **SecurityManager verifies the requested Permission against the installed Policy** through the call stack. It may also grant permission or throws *SecurityException*.

## Java Tools for Policy
Java has a default implementation of Policy that reads authorization data from the properties file. However, the policy entries in these policy files have to be in a specific format.

Java ships with “policytool”, a graphical utility to compose policy files.
