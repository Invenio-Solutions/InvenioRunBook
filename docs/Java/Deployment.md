---
sidebar_position: 3
---
# Deployment

The deployment of Java applications can be a cubersome and tedious process. To reach an optimal deploement, it is always encouraged to adopt the best practices to improve the deployment process to mitigate deployment risk. Invenio always follows the best practices to deliver a highly efficient product within the specified time. Some of them are:

- **Do a Reality Testing**

    It is always good to test deployment in a pre-production/staging environment. Typically, functional, regression as well as performance tests are conducted to ensure that the application still meets the requirements (functional & non-functional) once deployed in production.

- **Use an Artifact Repository**

    Artifact repositories manages multilevel dependencies.  This dependency management is critical in reducing errors and ensuring that the right components are included with each build/deployment/release. For Mavenized Java projects, we specify application version and declare dependencies in a pom.xml file, file, specifying the source of your artifact repository and voila, your application.

- **Have a Rollback Strategy**

    Rollingback of the application to  aknowm version of the application. One simple strategy is to keep a backup of the production application and initiate the rollback, then undeploy the defected Java application and deploy the backup application.  Artifact repository helps to simply redeploy a previous version of your application back to production.

- **Documentation**

    Developed codes are documented using code comment, highlighting the purpose and intent of the code. Before production deployment, a detailed and accurate document is created that lists the stakeholders of the projects, the features, and bug fixes introduced in your Java applications release, the backup plan, deployment plan, rollback plan, a maintenance plan, and communication plans & training plan.  Documentation can be to retrace the steps and reproduce the deployment process they created.

- **Automate Deployment Process**

    Manual deployment may introduce unintended errors. Thus its better to go with automate deployment. There are various tools that allows to do an automated deployment. Factors thar are considered while choosing a deployment tool include:
    - **Automated Build tool**: Build tool identifies the dependencies between files and package them for distribution. For Eg:-  [Apache Ant](https://ant.apache.org/), [Apache Maven](https://maven.apache.org/)

    - **Load Testing and Performance Testing**: These tools can be easily integrated into CI tools such as Apache Jenkins and/or Atlassian Bamboo. Tools like  [Apache JMeter](https://jmeter.apache.org/), [SmartMeter.io](https://www.smartmeter.io/) are suited for this purpose.

    - **Automatic deployment**:  Makes sure that the tool can deploy and install the application to the target environment.

## Steps to follow



    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum