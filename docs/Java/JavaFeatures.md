# Java Features

Java is the most popular object oriented programming  and platform independent language, that offers different varities of salient features as preffered by developers.
Java comes with its own unique set of security aspects that makes it more realiable, secure and acceptable.

## Why java is secure?

Security in java begins at its language feature level. This helps us to write secure code and get benefit from many implicit security features:

- **Access Modifiers** : Java uses public and private access modifiers to control access to fields, methods, and classes.

- **Automatic Memory Management** : Java has garbage-collection based memory management. Thus it relieves the developers from managing it manually.

- **Bytecode Verification** : Java converts code into platform agnostic bytecode,and runtime verifies every bytecode it loads by checking the code fragments for illegal code that can violate access right to object.
- **JVM** : Java Virtual Machine plays a major role in verifyng the bytecode. JVM ensures that program do not take any unsafe operations. It helps to minimize the memory safety flaws.

- **Security API's**
Java class libraries provide several API that ensures security.These APIs contain cryptographic algorithms and authentication protocols that lead to secure communication.

- **Security Manager**
All the properties and permissions of the classes are checked and verified by security manager. It controls socket connections and monitors the system resources accessed by the authorized classes.

- **No Concept of Pointers**
Java does not support pointer concept as the use of pointers leads to unauthorized read or write operations. It is the *main feature of Java*. Thus user cannot point to any memory locations. 

- **Static Data** : Java is a statically typed language. It reduces the possibilities of run-time detection of type-related errors.

- **Compile-time Checking**
It prevents system crash. For example, JVM gives compile-time error when an unauthorized method tries to access the private variable.

- **Cryptographic Security**
Java provides a class named java.secrurity.SourceCode that also provides security. The class maintains the source information and provides guarantees to keep a digital signature and cryptographic security.

- **Java Sandbox**
Java Sandbox ia a restricted area where applets are run. Java does not provide system resources without check if an applet is to be run.

- **Exception Handling**
This adds more scurity to java. It reports the error to the programmer during the runtime. The code will not run until it is rectified.

- **Java ClassLoader**
It provides and maintains namespaces for specific classes. The advantage of the ClassLoader is that the untrusted classes would not behave like a trusted one.



