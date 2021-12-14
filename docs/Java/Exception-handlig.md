# Exception Handling
Exception handling in java is used to handle the runtime errors that disrupts the normal flow of the program. This mechanism helps to maintain and improve the performances of program statement.

The root class of Java Exception hierarchy is jang.lang.Throwable. It is inherited by two subclasses. They are,
* Exception
* Error

## Hierarchy Of Java Exception Classes
![Java Error Handling Exception Hierarchy](https://lh3.googleusercontent.com/proxy/-cWUpJd2__37heAZgYr02jL-SMU0zd2TiPBdb47td4CAHXp0CxayJ277wIjsAu99qeWeilUHJnW8_q4ZGDoPOQ5AUrSXy5RNFR49shbyAqLyLPjRAGbhZGKVCR4x62tSY2IIHlyen8Tmnb0)

One branch is headed by exception and the onther by error. Exception class is used for exceptional conditions that user programs should catch. For example IOException,ArrayIndexOutOfBoundsException, etc.

JVM indicates error present in the run time environment. For example StackOverFlow etc.

## Types of Java Exception
There are three types of Java Exception.
* Checked Exception
* Unchecked Exception
* Error

![Types of JE](https://static.javatpoint.com/core/images/types-of-exception-handling.png)

* **Checked Exception**:- The classes that directly inherit the Throwable class except RuntimeException and Error are known as checked exceptions. For example, IOException, SQLException, etc. Checked exceptions are checked at compile-time.

* **Unchecked Exception**:- The classes that inherit the RuntimeException are known as unchecked exceptions. These exceptions are checked at runtime and not checked at compile-time.For example, ArithmeticException, NullPointerException, ArrayIndexOutOfBoundsException, etc. 

* **Error**:- It is irrecoverable that indicates a serious problem that an application should not try to catch. For example StackOverFlow, OutOfMemoryError, VirtualMachineError.

## Default Exception Handling
If an exception occurs inside a method, the method creates an Object known as Exception Object and hands it off to JVM(run-time system). This exception object contains a name, reason for the cause of exception and current state of the program where exception has occured.This creation of object and handling it ot run-time system is called throwing an exception.

[Default Exception Handling](https://www.geeksforgeeks.org/exceptions-in-java/)

## Customized Exception handling

 Java exceptions cover almost all the general type of exceptions that may occur in the programming.
 The customized exception handling is a technique to handle the exception according to our need. 

 Why Custom Exceptions?
 - To catch and provide specific treatment to a subset of existing Java exceptions.

- Business logic exceptions: These are the exceptions related to business logic and workflow. 
  It is useful for the application users or the     developers to understand the exact problem.

### Java Exception Keywords
There are five keywords specified in java to handle the exceptions.
- **try** : The "try" block is used to place the program statment or exception code that may raise an exception followed by either catch or finally block.

- **catch** : The "catch" block is used to handle the exception. It must be preceeded by try block and can be followed by finally block. It catches the exception that is raised by try block

- **finally** :  The "finally" block is used to excute a particular block of code even if the exception is handled or not.

- **throw** : The "throw" keyword is used to manually throw an exception.

- **throws** : The "throws" keyword is used to declare exceptions. It doesn't throw an exception but specifies that an exception may occur in the method.

For example : [Custom Exception](https://www.w3schools.com/java/java_try_catch.asp)
