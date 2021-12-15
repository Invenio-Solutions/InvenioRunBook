# Spring Exception Handling

Whenever we think of handling exceptions at any level of our code, we fall under writing everywhere try catch block in our code, and then after some days, we find most of the code is filled with handling exceptions. This degrades readability of code. Here, we will learn all the best practice to handle exceptions with powerful feature provided by Spring Boot to avoid these duplications and improve the readability of code while handling exceptions in our application.

## Use Controller Advice

`@ControllerAdvice` constructor comes with some special arguments, which allows you to scan only the related portion of your application and handle only those exceptions thrown by the respective classes mentioned in the constructor. By default, it will scan and handle all the classes in our application.

Below are some types which we can use to restrict only specific classes to handle exceptions.

**1. Annotations** - Controllers that are annotated with the mentioned annotations will be assisted by the `@ControllerAdvice` annotated class and are eligible for exception of those classes

>Example: `@ControllerAdvice(annotations = RestController.class)` - Here the exception helper annotated by `@ControllerAdvice` will catch all the exceptions thrown by the `@RestController` annotation classes.

**2. basePackages** - By Specifying the packages that we want to scan and handling exceptions for the same.

>Example: `@ControllerAdvice(basePackages = "org.example.controllers")` - This will only scan call the mentioned package and handle the exceptions for the same.

**3. assignableTypes** - This argument will make sure to scan and handle the exceptions from the mentioned classes

>Example: `@ControllerAdvice(assignableTypes = {ControllerInterface.class, 
AbstractController.class})`

## Use Exception Handler

The `@ExceptionHandler` annotation gives us a lot of flexibility in terms of handling exceptions. For starters, to use it, we simply need to create a method either in the controller itself or in a `@ControllerAdvice` class and annotate it with `@ExceptionHandler`.

## Use HTTP Status Codes

Normally any unhandled exception thrown when processing a web-request causes the server to return an HTTP 500 response. However, any exception that you write yourself can be annotated with the `@ResponseStatus` annotation (which supports all the HTTP status codes defined by the HTTP specification). When an annotated exception is thrown from a controller method, and not handled elsewhere, it will automatically cause the appropriate HTTP response to be returned with the specified status-code.

## What to Use When?
As usual, Spring likes to offer you choice, so what should you do? Here are some rules of thumb.

* For exceptions you write, consider adding `@ResponseStatus` to them.
* For all other exceptions implement an `@ExceptionHandler` method on a `@ControllerAdvice` class.
* For Controller specific exception handling add `@ExceptionHandler` methods to your controller.


Refer to [Exception Handling in Spring](https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc) documentation for detailed explaination and Best Practices for Spring Exception Handling.