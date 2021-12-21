
# Python Exception Handling


Exception Handling at all possible levels is important for creating a seamless application experience.Exception is the base class for all the exceptions in Python. The exception hierarchy of Python is given [here](https://docs.python.org/2/library/exceptions.html#exception-hierarchy).


## Why Do We Need Exception Handling?

1. Prevents program from crashing if an error occurs
2. Saves time debugging errors
3. Helps define requirements for the program

The following measures can be included as a part of Exception Handling Best Practices:


## Try and Except Statement 

Try and except statements are used to catch and handle exceptions in Python. Statements that can raise exceptions are kept inside the try clause and the statements that handle the exception are written inside except clause.

## Catching Specific Exception

A try statement can have more than one except clause, to specify handlers for different exceptions. However, it is to be noted that at most one handler will be executed.

## Try with Else Clause

We can also use the else clause on the try-except block which must be present after all the except clauses. The code enters the else block only if the try clause does not raise an exception.

## Finally Keyword

Python provides a keyword finally, which is always executed after the try and except blocks. The final block always executes after normal termination of try block or after try block terminates due to some exception.

## Raising Exception

The raise statement allows the programmer to force a specific exception to occur. The sole argument in raise indicates the exception to be raised. This must be either an exception instance or an exception class (a class that derives from Exception).

***
[Click here](https://wiki.python.org/moin/HandlingExceptions) for the detailed explanation of exception handling in python.


