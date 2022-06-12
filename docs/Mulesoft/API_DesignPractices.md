---
sidebar_position: 3
---

# API Design

### Introduction:

An API should be simple to understand and easy to use. An optimal API design enables application developers to easily recognize the purpose and functionality of the API. 

>> *InvenioLSI ensures the adoption of the best API design standards for designing a user-friendly API that persists. The following enlists the best practices incorporated by InvenioLSI while designing its API*

#### Planning of the API:

   * Understanding who our target audience is, and try to advocate to their needs is important.

   * Having clarity on the use-case, technologies that would interact and integrate with the API is imperative.

   * The API must be ptimized to fulfil a specific business request in a specific context.

   * Creating user stories that enlist and describes the entire set of actions/services that the API would provide would be benficial.

   * Following a layered architecture wherein, the API exposes the fine-grained services that users can access directly or according to the requirements and add coarse-grained services on top of them to support broader use cases. 

   * Envisioning sustainable API designing.

   * Versioning of an API only in cases like incompatible platform changes or major changes in the specifications to meet the requirement of the clients.


#### Focussing on the Specification:

   * The defining of the API structure should be carried out in an iterative manner with continous feedback on the usability and functionaluty of the API.

   * Mule provides API designer, which is an open-source design environment that leverage RAML. The API Designer tools has an interactive environment wherein drafting and testing of the API becomes easy.

   * API NoteBook must be leveraged to identify and eliminate the design related issue at the intial level.

   * Iterative feedbacks and changes is important untill the design flaws are reduced to a minimum and a strong foundation for API development is built.
  
#### Flexibility and Extendibility of API:

   * Naming of resources should be in Noun. This facilitates loose coupling of the resources enabling multi-tasks and several actions can be included at a time.

    ```
        users/id
        /user/address should be followed instead of
        /createusers/1

    ```
   * Resource Name essentially should be in lowercase.

   * Inclusion of description about the functionality is benficial.

   * For improved readability, reusablity and comprehensibilty, it is important that RAML fragments are created. [Improve Code Readability in RAML](https://blogs.mulesoft.com/dev-guides/restful-api-modeling-language-201/) beautifully documents the details on this.
 
   * Also, these fragments can be extended for use in other API Design accross the organization when shared over Exchange.T

   * To define the services the API is catering, CRUD and HTTP action verbs must be used.

   * Inclusion of  Content-Type header eases the understanding of the format of data the users is sending. Also, this increases the flexibilty by provisioning multiple file formats.

   * JSON can be opted whenever possible as JSON is compact and is widely supported 
   * Inclusion of different HTTP Status Codes to notify the clients of what response would the API give for a particular kind of request. Such codes are:

   ```
   200: OK
   201: Created 
   400: Bad Request
   404: Resource Not Found

   ```
   
  * To notify the developer of why a particular API call is giving an error status, it is important that a descriptive error body and possible measures to fix it should be included in a proper schema as follows:

  ```
  {
      "error" :{
          "code": 404,
          "message": Missing ID,
          "description": Please include the ID in int form,
          "link":
      } 

  }
  ```

#### API Management:

  * API Managers can be leveraged for securing and scaling the API.

  * Designing an API must ensure enabling of authentication.   

  * API Securing can be falicitated by providing unique API token to the users.
  
  * It is possible to set permissions and SLAs for users, depending on their individual needs. Also, addition of rate limiting and setting up SLA tiers in API can optimize the user experience.

#### Related Documentations:

There are many insteresting documents related to API Design Practices. 
   1. [Mulesoft Design Practices](https://www.mulesoft.com/lp/whitepaper/api/design-apis)
   2. [Undisturbed Rest](https://www.mulesoft.com/lp/ebook/api/restbook)
   3. The video [API Design Practices](https://www.youtube.com/watch?v=ntoYSsNo9Ww) comprehensively enlists the best practices related to API Design.




