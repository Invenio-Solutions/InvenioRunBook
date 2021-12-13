# Spring Coding Standards

## Application Structure:

It is always recommended to follow the below package structure while creating a spring based project

* src/main/java – Contains Java Source code packages and classes
* src/main/resources – Contains NON-Java Resources, such as property files and Spring configuration
* src/test/java – Contains Test Source code packages and classes
* src/test/resources – Contains NON-Java Resources, such as property files and Spring configuration
* Avoid using the default package.
* Make sure that everything lives in a well-named package. This is to avoid surprises related to wiring and component scan.

## Configuration:

### It is recomannded to use Auto-configuration in Spring Boot:

Auto-configuration is the part of Spring Boot that makes our code simply work. Auto-configuration attempts to automatically configure our Spring application based on the jar dependencies that we have added. For example, if H2 database is on the classpath, and we have not manually configured any database connection beans, then Spring Boot auto-configures an H2 in-memory database. We need to opt-in to auto-configuration by adding the `@EnableAutoConfiguration` or `@SpringBootApplication` annotations to one of our Configuration classes. It is generally recommended that we add one or the other annotation to our primary Configuration class only. Definitely take advantage of Spring Boot’s auto-configuration instead of manually injecting beans or intercepting any requests.

## Logging Rules:
* Never use System.out
* Never use System.err
* Always use SLF4J (annotate at class level with @Slf4j)
* Always use Logback (comes with Spring Boot)
* Don’t use Apache Commons Logging (JCL) aka Jakarta Commons Logging
* Don’t use Java Util Logging (JUL)

## Application Layer:

Application components (beans) should be separated into distinct layers, and categories.

Bean Layers
1. Controllers
2. Services
3. Repository

Other Bean Categories
* Data Transfer Objects
* System Functions

**1. Controller Beans:** The simplest way for creating a controller class to handle one or multiple requests is just by annotating a class with the `@Controller`

```
@Controller
public class HomeController {

@Autowired
private UserDAO userDAO;

@RequestMapping(value = "/visit" method = RequestMethod.POST)
public String visitHome(@RequestParam String username, @RequestParam String password) {
// do something before returning view name
return "home";
}
}
```

* Use `@RequestMapping` annotation for specifying URL mapping(requests) and the request type GET/POST

* Retrieve request parameters as regular parameters of the handler method by using the `@RequestParam` annotation

* After business logic is processed, a handler method should return a view which is then resolved by the Spring’s dispatcher servlet.

* Use the `@Autowired` annotation to let Spring automatically injects actual implementation of a business class to the controller

**2. Service Beans:** Service Beans are Problem Domain components. These are the MOST significant in the application. Service beans are the Fundamental component of SOA.

* Always defined from interfaces
* NEVER include infrastructure components
* NO import of Spring or utility libraries
* NO infrastructure annotations
* Always declare transaction boundaries by public functions
* Create implementation/concrete classes in a sub-package named internal.
* Prefer throwing runtime exceptions instead of checked exceptions from service layer
Spring annotations can be very useful for services, useful annotations are @Service and @Transactional.

To abstract away the infrastructure from the business services, create a project specific meta annotation.

**3. Repository Beans:** Repository beans are in the System Domain.
* DO NOT contain business logic
* Do use Spring and JPA annotations
* Should be considered disposable.
* Manage transactions only in the dao layer
* Mark transactions as readOnly=true when methods only contain queries
* Use SessionFactory and EntityManager directly in your DAO beans

## **General Best Practices for Spring:**

### 1. Configuration
* Avoid using XML based Configuration for your Spring Boot project.
* Use Java Class as Configuration with @Configuration Annotation
* Divide your large configuration files into multiple config files then Import them into main file (ex. DatabaseConfig)

### 2. Use Spring Initializr for starting new projects

### 3. Spring Bean Naming Conventions:
* Bean names shoud start with a lowercase letter and are camel-cased from then on. (ex. accountService)