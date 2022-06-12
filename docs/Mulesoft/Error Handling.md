---
sidebar_position: 3
---
# Error Handling

Error Handling forms an innate part of a seamless microservices architechture. Invenio ensures that it leverages the provisions mule has provided for error handling. Mule has categorized errors as:

* System Errors : These flows covers the deplyment and code related issues.

* Messaging Errors: This error encompasses the errors in the processing of an event in a mule flow. This error type creates an error object upon occurence which consist of the following components:

         1. Description

         2. Type

         3. Cause

         4. Message

         5. Child Errors

These errors in a mule application can be handled in three different scopes:

1. On Error Propagate

2. On Error Continue

3. Try and Catch Scope

### Best Practices in Error Handling:

*  Error Handling of all the errors encountered at a single place is prefferable.

*  Provision for creating custom error types such as validations should be leveraged. 

*  Creation of a generic message schema is important at the design level of the API. This step will ensure that the API Kit Router too follows the same for error response.

* Error encountered via HTTP must include retry mechanisms.

### Documentation
There are several documentation on how to efficiently enable error handling in a mule application. Some of these are:

1. [This documentation](https://docs.mulesoft.com/mule-runtime/4.4/error-handling) explains the configuration for the error handlers in mule.

2.  A detailed four series blog on Error Handling in a mule application is [here](https://blogs.mulesoft.com/dev-guides/how-to-tutorials/mule4-error-handling/)

3. A video tutorial on the same is also available [here](https://videos.mulesoft.com/watch/97pfQvqqAYPubhLTcP4jRH)

