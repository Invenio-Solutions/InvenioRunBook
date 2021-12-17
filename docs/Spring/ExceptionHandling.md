# Spring Exception Handling

It is often noticed that exception handling with multiple try and catch blocks has an adverse impact on the readability of the code. Spring has an excellent features that enables us to avoid the duplications and hence improve code readability.

The best practices that must be adhered to with Exception Handling are summarized below:

## Use of Controller Advice

`@ControllerAdvice` constructor comes with special arguments, which scans only the related portion of the application and handle only those exceptions thrown by the respective classes mentioned in the constructor. By default, it will scan and handle all the classes in our application.

Below are some types which we can use to restrict only specific classes to handle exceptions.

**1. Annotations** - Controllers that are annotated with the mentioned annotations will be assisted by the `@ControllerAdvice` annotated class and are eligible for exception of those classes

```
`@ControllerAdvice(annotations = RestController.class)` - Here the exception helper annotated by `@ControllerAdvice` will catch all the exceptions thrown by the `@RestController` annotation classes.
```

**2. basePackages** - In this approach scanning and exception handling  for the specified packages are carried out.

```
 `@ControllerAdvice(basePackages = "org.example.controllers")` - This will only scan call the mentioned package and handle the exceptions for the same.
 ```

**3. assignableTypes** - This argument ensure to scan and handle the exceptions from the mentioned classes

```
`@ControllerAdvice(assignableTypes = {ControllerInterface.class, 
AbstractController.class})`
```

## Use of Exception Handler

The `@ExceptionHandler` annotation gives the flexibility in terms of handling exceptions. A method either in the controller itself or in a `@ControllerAdvice` class must be created and annotate it with `@ExceptionHandler`.

## Use HTTP Status Codes

Use of case appropriate HTTPSCode based response is the best practice while processing the web=request. This can be achieved by using the @ResponseStatus annotation. This has the support for all the HTTP status code.

## How to choose the Exception Handling Approach?

The rule of thumb fo choosing the handling pattern is as follows:

* For exceptions we write, consider adding `@ResponseStatus` to them.
* For all other exceptions implementing an `@ExceptionHandler` method on a `@ControllerAdvice` class is recommended.
* For Controller specific exception handling add `@ExceptionHandler` methods to your controller is recommended.


### Reference:
>>  [Exception Handling in Spring](https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc) has provided a detailed explaination and Best Practices for Spring Exception Handling.