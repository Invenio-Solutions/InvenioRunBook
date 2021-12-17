# Microservices Architecture:

Microservice architecture  encompasess several independent and autonoumous services together to build an application. It focusses on loose coupling of the services.

 The primary objective of the microservice architecture are:

* Scalability
* Decentralization
* Resilient Services
* Flexibilty
* Availability
* Continuous delivery through DevOps Integration
* Seamless API Integration and Continuous Monitoring
* Failure Isolation
* Auto -Provisioning

 Incorporating microservices architechture brings in with its own set of challenges. To overcome those, there are various design pattern proposed that will aid in creating the architecture seamlessly. These patterns can be broadly categorized as:
1. Decomposition Patterns
2. Integration Patterns
3. Database Pattern 
4. Observibility Pattern
5. Cross Cutting Concern Pattern

Here we will be having a brief elaboration of some of the patterns under these category:

### Integration Pattern:

* **Aggregator Pattern** : Several independent services are hosted by an application It is important to understand the behaviour of these services upon its collaboration and what reponse is returned to the clients. Here the aggregator pattern is a solution. An aggreagator will make a call to each of the services with a unique transaction ID and then collaborate and make necessary transform to their output before being sent as a response to the clients.

* **API Gateway Pattern** : The division of an application into smaller chunks brings in certain challenge in the form of requirement for multiple microservice calls from multiple channels, transformation of data according to the client's requirement, requirement of multiple protocols and conforming to the data requirement for different UI etc. This can be handled by API Gateway. API Gateway creates a client request specific fine grained API. This would be the entry point for all the services, wherein it will proxy the request to the concerned microservices. It is capable for handling protocol request and aggregation and has provision for authorization and authentication.

* **Chained Microservices Pattern** : This pattern is suitable for the service request calls, that has dependencies for other prevailing services in the application. These calls are HTTP request and responses. The calls to the services are in the form of chain structure, where one call to the service can invoke another service call. The client won't be able to receive each of the response of the chain calls. Instead, this pattern produces the amalgamated result of the service calls and returns the reponse to the client.

* **Asynchoronous Messaging Pattern** : This approach is a variation to the chained microservices pattern, wherein the service can request to multiple services simultaneously instead of having a chain of calls. These calls are then sent to a queue before being aggregated and returned to the client.

### Database Pattern:

* **Shared Data Pattern** : Shared database has the advantage of managing the transactions and redundancy of data. This approach where all the services in an application is sharing the same database, the data consistency and synchronization is present and it would not have adverse impact in synchronization of data if communication fails. However, shared database has its own share of challenges in terms of scalability, and independent development and deployment.

* **Database per Service Pattern** : This pattern addresses the scalabilty and importance of independent development and deployment. Each microservices has its own database with unique ID. This prevent other services to make changes in the data. Apart from being scalable this approach facilitates easy comprehension of the services and the data being affected. 

* **Event Sourcing Pattern** : Event sourcing aids in keeping track of the changes made to the data with the operations in  the microservices. The application sends a series of events based on the actions taken on the data and stored and published to event store for analysis and record.

### Decomposition Pattern:

* **Decomposition Design Pattern**: The primary objectives of microservices is loose coupling of the services provided by an application. However, these services must be created logically catering to a business responsibility. These decomposition of the services can be based on business capability, sub-domains or transactions. However, these appraoch for decomposition of services is not feasible for big applications as it would be quite challenging to identify how the domain is decomposed.

* **Strangler Pattern** : This approach for decomposition is suitable for big applications. It is a phased  approach for migrating a system with the existing functionalities with new services. The strangler pattern  creates two independent application with the same URI space. One of the applications consists of the services that were present previously, whereas the other application implements the new features of the services. With time the second application takes over the existing one. 

### Cross Cutting Concern Pattern:

* **Circuit Breaker Pattern** : For the services that are dependent on the responses of other downstream services might faces challenges whenever that service is down. This would have adverse affect on the performance as well as the user experience. As a preventive solution, circuit breaker approach can be used. Here, a remote service is used. This service has a threshold for failed request. If the threshold exceeds, it would go to a timeout period before taking any request.




