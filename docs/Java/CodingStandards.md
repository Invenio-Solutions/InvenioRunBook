# Coding Standards

## Introduction
Java being one of the evergreen programming languages has a strong presence in this high tech world for its speedy growth with trends and relevance. It is secure, fast, reliable and is designed to have less implementation dependencies.




>“Clean code is simple and direct. Clean code reads like well-written prose. Clean code never obscures the designer’s intent but rather is full of crisp abstractions and straightforward lines of control.” — Robert C. Martin

Writing clean code is matter of skill. A clean code must be focussed, simple, and testable so that it can **develop a software that is easy to change and maintain.**

Invenio uses this cross-platform object-oriented programming language that is concurrent and independent along with the best practices that enhances the coding standard to increase the performance and efficiency of the code.

We give utmost importance to improve code quality and to decrease the code entropy.
This includes all the clean coding principles which Invenio adopts to enhance the coding standards to keep the code readable and maintainable over time.

## General Practices 
- Logical grouping of the code are made using consistent whitespaces and blank lines to enhance the readability of the code.
- Well indented code to read and understand easily
- Avoids multiple parameter entry
- Increased reliability of code with less focused hardcoded values
- Uses code comments to understand the non-trivial aspects.
- We follow the principle DRY (Don’t Repeat Yourself) so that same piece of code is not driven across the software. It increases reusability and decreases the duplication of code.

## Proper Naming Convention
- Follow the java coding convention

    - Use camel case to define variable and method names
    - Start Class names with capital letters
    - Use all caps for constants in java
- Always preferred to take shorter names over longer one with clarity
- Always prefer to use descriptive names over short form and avoid similar names
- Avoids using non-ASCII characters
- Make good use of common verbs to improve code readability.




## Source file Structure
- 	Adhere to specified order of elements in a source file to improve code readability.
- Typical Ordering of elements in a source file will look like: -
    - Package statement
    - Import statements
    - One top level class that includes
        - Class variables
        - Instance variables
        - Constructors
        - Methods
          (Methods can also be grouped based on their functionality and scope)

## SOLID Principle
We strictly follow the five principles so named “SOLID” to increase the readability, reliability, flexibility, and efficiency of the code.
- **S**ingle Responsibility Principle:-  Interfaces, classes, and methods will be built only with one goal and purpose. This leads to increased number of smaller classes and easy testing.

- **O**pen-Closed Principle:- This helps the built-in code open for extensions but closed for further modification, though it allows changes through inheritance and composition.
  
- **L**iskov Substitution Principle:- It improves the reusability as every subclass or derived class can be substitutable for their parent or base class.
    
- **I**nterface Segregation Principle:- To define small and focused interfaces so that a class just need to implement the interface with specific behavior.

- **D**ependency Inversion Principle:- The classes are depended on abstractions and not on their concrete implementations. Thus, a class is not responsible for creating instances for their dependencies.








