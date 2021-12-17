# Testing
Java unit testing frameworks provide programmers with a standardized, sophisticated, and extensible means to build a web application or other softwares. It comprises a massive collection of packages that supply pre-written code. Java testing frameworks incorporate libraries, compilers, tools, and APIs. Java testing frameworks always deliver a secured application. They even offer built-in functions and modules to enable efficiency and speed for the developers and testers.

## Advantages Of Using Java Testing Frameworks

- Security: Frameworks offers top-notch security to the applications and also helps mitigate security problems at a speedy pace.
- Support: Frameworks offer broad community support wherein you can mitigate all your issues and doubts within a short span.
- Efficiency: Frameworks have pre-written tasks, thus makes he job simpler.
- Expense:  The cost of maintenance for Java frameworks is relatively low.

## Java Testing Frameworks
There are different Java Testing Frameworks available for QA testers. Some of the Testing Frameworks that we use in Invenio are:

- ### **JUnit**

    JUnit is one of the popular Java unit testing frameworks. The unit test is used in a path function or for testing a small piece of code. It plays a vital role in test-driven development and is a part of the collective unit test frameworks called xUnit.
    JUnit boosts the initiative of *“to begin with testing than coding”*. This technique is based on “test a little, code a little” technique.  It enhances the programmer’s productivity and program code’s stability, which in turn reduces the pressure on the programmer and minimizes the time spent on debugging.

    #### Features of JUnit
    - JUnit offers test runners to execute tests.
    - Enables to write enhanced tests at an expedited pace.
    - Offers annotations to simplify writing and maintaining of tests.
    - Offers assertions to test anticipated outcomes.
    - Less complicated and takes minimum time to execute.
    - Test suites can contain test cases as well as other test suites.

    #### Resources:

    ```
    1. 
    
    ```

- ### **Selenium**

     Selenium is an automated open-source testing framework, that is used for cross browser testing. It is to control and manage web browsers through the program. This reduces the effort involved in the maintenance of the code. Three kinds of framework by Selenium for the automation of manual test cases: Keyword Driven Tests, Data-Driven Tests, and Hybrid Tests.

     #### Features of Selenium:

     - Selenium Integrated Development Environment gives a record and playback trait for authoring tests and for creating Selenium scripts for future reference.
    - Selenium supports several programming languages, OSs, and browsers:
    - Operating Systems: iOS, Android, Windows, Mac, Solaris, Linux.
    - Browsers: Internet Explorer, Google Chrome, Edge, Mozilla Firefox, Safari, Opera, etc.
    - Programming Languages: Java, C#, PHP, Python, Ruby, JavaScript, etc.
    - Supports parallel test execution, which increases efficiency and reduces the test execution time.
    - It can be integrated with frameworks such as Ant, Maven, etc.

    #### Resources:
    
    ```
    1. 
    
    ```

- ### **TestNG**

    TestNG is open-source testing framework that is more robust framework compared to other test automation frameworks. It is inspired by JUnit and NUnit. Its features like grouping tests, annotations, parameterization, etc., helps in creating tests at a faster pace.
   
    #### Features of TestNG

     - Provides myriad kinds of after/ before annotations for support of distinct setup and cleanup choices.
    - Allows users to perform data-driven testing
    - Test suites in this framework are configured mainly utilizing XML files (i.e., testng.xml)
    - Supports testing integrated classes.
    - Provides flexible plugin API and flexible runtime configuration.
    - Supports dependent test methods, load test, parallel tests, and partial failure.
    - Support for multiple threaded testing.

    #### Resources

    ```
    1. 
    
    ```

- ### **Mockito**

    Mockito is an open-source testing framework that is primarily used for Java app unit testing. This framework generates mock objects by means of annotations. Mockito is used for writing behavioral-based development tests. This eases the test development by mocking exterior reliance and utilize it in the test implementation. Therefore, it gives a simplified test code that is understandable and easy to modify. 

    #### Features of Mockito
    - Mock objects reduce external reliance.
    - Easily create mock objects using annotations like @Mock.
    - It offers verification on the order of the method calls.
    - Safe refactoring: As mock objects are formed at runtime, renaming a method or interface does not impact the test code.

    #### Resources
    
    ```
    1. 
    
    ```

- ### **JBehave**

    JBehave framework is a Behaviour-Driven Development (BDD) framework. It is primarily used with Selenium WebDriver for Java testing.

    #### Features of JBehave

    - Pure Java execution that plays well with Java-based enterprises or when interfacing to any environment that exposes a Java API.
    - Stories can be executed at the same time, stating the number of concurrent threads.
    - Shallow learning curve as user stories is written in Gherkin or JBehave syntax.
    - Steps class specifications and annotation-based configuration.
    - Groovy scripting for writing configuration and Steps instances.
    - Dependency Injection supports enabling both configuration and stage instances composed through your favorite container (PicoContainer, Needle, Guice, Spring, Weld).
    - Extensible story reports: outputs stories executed in varied human-readable file-based formats (TXT, HTML, XML). Fully style-able view.
    - Ant integration- permits stories to be run through an Ant task.
    - Maven integration: permits stories to be carried out via Maven plugin at specified build stage.

    #### Resources

    ```
    1. 
    
    ```

- ### **Serenity**

    Serenity is an open-source library designed for Behavior-Driven Development (BDD). It expands the WebDriver and JUnit attributes. This framework helps to write well-structured tests. Serenity can also integrate with existing BDD frameworks such as JBehave. It supports a number of automated acceptance test solutions.

    #### Features of Serenity
    - Helps in writing cleaner and maintainable automation & regression tests.
    - Obtain Business-readable reports for every test.
    - It can be used for automated web testing with Selenium.
    - It can be integrated with other popular BDD tools like JBehave, Cucumber, as well as test automation frameworks like JUnit.
    - Can be integrated with necessities stored in an external source (like JIRA or other test case management tools).

    #### Resources

    ```
    1. 
    
    ```

- ### **HTTPUnit**

    HTTPunit testing framework is based on JUnit. It imitates browser behavior like Page redirection, Form Submission, cookie management, and JS Validation, to name a few. It is used to test the website without the requirement of web browser. The framework also supports automatic page redirection, HTTP basic access authentication, HTML form submission, JavaScript, and cookies. This permits Java test code to process restored pages like XML Document Object Model (DOM), text, or containers of tables, forms, links, etc.

    #### Features of HTTPUnit

    - Used to test websites without any web browser.
    - Support for cookies.
    - Support for the HTTPS as well as HTTP  protocols, along with support for HTML responses.
    - It enables the test of web applications, and due to this, it also assists in regression tests.
    - HTTPUnit is faster than other frameworks such as Selenium as you do not require a web browser for the tests.
    - Better JavaScript support enables imitating the actions of the configured browser (Internet Explorer or Firefox).
    - Proxy server support as well as great JavaScript support.
   
    #### Resources

    ```
    1. 
    
    ```

- ### **Gauge**
    Gauge is a Behavior Driven Java testing framework. This framework helps to develope automated frameworks and speed up the software development procedure. This open-source framework for Java takes the stress out of acceptance tests with minimum involvement of code.

    #### Features of Gauge:

    - An extensive range of templates is accessible in the language of your choice.
    - Command-Line support eases the integration with popular CI/CD tools.
    - Easily create your plugin using the open-source Gauge API.
    - Rapidly identify anomalies through screenshots of event failures.
    - Enables you to generate scalable tests through parallel execution and provides integrations with cloud-based solutions such as LambdaTest to address the objectives of rapid cross browser testing.

    #### Resources

    ```
    1. 
    
    ```

- ### **Geb**
    Geb is also an open-source test framework. Geb brings together the grace of jQuery content selection and the capabilities offered by WebDriver, Page Object Modelling (POM), and clarity offered by the Groovy language. Geb can be integrated with popular test automation frameworks like TestNG, Cucumber, Spock, and JUnit. It supports Page Object Model design pattern

    ### Features of Geb

    - It lets you execute the tests at a faster pace.
    - Compatible with browsers such as Firefox, Chrome, IE, and HTMLUnit.
    - Well-suited for running regression tests.
    - While using Geb for automated tests, minimal test code modifications are needed if there are any UI changes in the app (or website). This minimizes the duplication of code.

    #### Resources
    ```
    1. 

    ```





