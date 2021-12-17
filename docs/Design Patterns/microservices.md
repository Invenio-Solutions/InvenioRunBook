# Microservices Pattern:

Microservice architecture facilitates loose coupling of the services by encompassing several independent and autonoumous services together to build an application. [7 Microservices Benefits and How they Impact Development](https://www.capitalone.com/tech/software-engineering/10-microservices-best-practices/) details on the importance of the microservice architecture.The primary objective of the microservice architecture are:

* Scalability
* Decentralization
* Resilient Services
* Flexibilty
* Availability
* Continuous delivery through DevOps Integration
* Seamless API Integration and Continuous Monitoring
* Failure Isolation
* Auto -Provisioning

Incorporating microservices architechture brings in with its own set of challenges. To overcome those, there are various design patterns proposed that will aid in creating the architecture seamlessly. These patterns can be broadly categorized as:

1. Decomposition Patterns
2. Integration Patterns
3. Database Pattern 
4. Observibility Pattern
5. Cross Cutting Concern Pattern

A brief elaboration of some of the patterns under these categories is provided here:

## Integration Pattern:

* **Aggregator Pattern** : Several independent services are hosted by an application. Hnece, it is important to understand the behaviour of these services upon its collaboration and the reponse it is returning to the clients. For this, the aggregator pattern is used. An aggreagator makes a call to each of the services requested with a unique transaction ID and then collaborate and make necessary transforms to their output before being sent as a response to the clients.

* **API Gateway Pattern** : The division of an application into smaller service chunks brings the requirement to handle multiple microservice calls from multiple channels, transformation of data according to the client's requirement, and conforming to the data requirement for different UI etc. API Gateway is a solution to this. API Gateway creates a client request specific fine grained API. This would be the entry point for all the services, wherein it will proxy the request to the concerned microservices. It is capable for handling protocol request, aggregation and has provision for authorization and authentication.

* **Chained Microservices Pattern** : This pattern is suitable for the service request calls, that has dependencies for other prevailing services in the application. These calls are HTTP request and responses. The calls to the services are in the form of chain structure, where one call to the service can invoke another service call. The client won't be able to receive each of the response of the chain calls. Instead, this pattern produces the amalgamated result of the service calls and returns a single reponse to the client.

* **Asynchoronous Messaging Pattern** : This approach is a variation to the chained microservices pattern, wherein, request to multiple services can be sent simultaneously instead of having a chain of calls. These calls are then sent to a queue before being aggregated and returned to the client.

## Database Pattern:

* **Shared Data Pattern** : Shared database has the advantage of managing the transactions and redundancy of data. Since, all the services in an application is sharing the same database, the data consistency and synchronization is present and it would not have adverse impact in synchronization of data if communication fails. However, shared database has its own share of challenges in terms of scalability, and independent development and deployment which is the core of the microservice architecture.

* **Database per Service Pattern** : This pattern addresses the scalabilty and importance of independent development and deployment. Each microservices has its own database with unique ID. This prevent other services to have any impact on the other service's data. Apart from being scalable, this approach facilitates easy comprehension of the database the service is impacting on. 

* **Event Sourcing Pattern** : Event sourcing aids in keeping track of the changes made to the data with the CRUD operations in  the microservices. The application sends a series of events based on the actions taken on the data which are stored and published to the event store for analysis and record.

## Decomposition Pattern:

* **Decomposition Design Pattern**: The primary objectives of microservices is loose coupling of the services provided by an application. However, these services must be created logically catering to a business responsibility. These decomposition of the services can be based on business capability, sub-domains or transactions. However, these appraoch for decomposition of services is not feasible for big applications as it would be quite challenging to identify how the domain is decomposed.

* **Strangler Pattern** : This approach for decomposition is suitable for big applications. It is a phased  approach for migrating a system with the existing functionalities with new services. The strangler pattern  creates two independent application with the same URI space. One of the applications consists of the services that were present previously, whereas the other application implements the new features of the services. With time the second application takes over the existing one. 

## Cross Cutting Concern Pattern:

* **Circuit Breaker Pattern** : For the services that are dependent on the responses of other downstream services might faces challenges whenever that dependent service is down. This would have adverse affect on the performance as well as the user experience. As a preventive solution, circuit breaker approach can be used. Here, a remote service is used which has a threshold for failed request. If the threshold exceeds, it would go to a timeout period before taking any further request.

The following provides a detailed information on these patterns:
1. [Applying Microservice Architecture Pattern Language. ](https://microservices.io/articles/applying.html) 
2. [Microservice Architecture and its 10 Most Important Design Patterns.](https://towardsdatascience.com/microservice-architecture-and-its-10-most-important-design-patterns-824952d7fa41)
3. [10 Microservices Best Practices](https://www.devteam.space/blog/10-best-practices-for-building-a-microservice-architecture/)
4. [Microservices Best Practices](https://www.capitalone.com/tech/software-engineering/10-microservices-best-practices/)




