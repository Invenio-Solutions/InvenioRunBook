# MULE APPLICATION BEST PRACTICES

It is important that we bring about consistency while creating our Mule Application so that these applications are easily comprehendable within the organization as well as the clients. Hence, it is important that certain standards are considered while creating the application. The areas that would be covered are:
1. AnyPoint Studio
2. Mule Project 
3. Naming Conventions
4. API Kit
5. Dataweave
6. API URL
7. Mule Flow

### AnyPoint Studio:
- It is important to keep the Anypoint Studio Updated.
- The projects must be upgraded to the  latest patch version.
- The Mule Runtime version  must be coherent within the SDLC.

### Mule Project:
- Use of Maven for creating Mule Projects is recommended. 
- Seperate XML file must be created for proper readalbility. The segregation can be based on:
     - Global Elements
     - Use case or resource implementation 
     - Common structures or logic 
- Seperate packages for resources such as DataWeave, WSDLs should be created.
- Formatting and Indentation of the XML files must be checked.
- The global elements must be included in a configuration file
- Also, seperate application.properties file must be created to efficiently manage different environment for the mule application.

### Naming Convention:
It is preferred to have the following in a mule application.
- Mule Project name should follow kebab- case.
- Flows and Sub flows should use camelCase
- XML files should be of lowercase kebab-case.
- Global Elements should be of kebab-case.
- JSON files should be camel cased
- REST related components should have Capitalized first letter with space between words.

### APIKit:
- Mule has the provision for APIKIT, which enables creating of the flows automatically based on the RAML file.
- The APIKit Strategy can be leveraged to catch the connector related exception
- The APIKit console must be disabled to avoid security related threats.

### DataWeave:
Dataweave tools are primarily used for querying and transformation of data in Mule. The detailed information of Dataweave can be found [here](https://docs.mulesoft.com/mule-runtime/3.9/dataweave). The important things that must be considered in dataweave are as follows:
- The coding must be simple and clear.
- Dataweave libraries must be leveraged before creating our own functions.
- It is important that we provide sample data for testing the transformation.
- Use of inline scripts in dataweave is recommended.
- The input content type must be defined.
- Externalizing those scripts for reuse is preferrable.
- The directive indent can be set to false in dataweave while dealing with large payloads to reduce the response payload size.

### Mule Flows:
- Mule flows must be simple and clear. 
- It is preffered that a Mule flow is kept short focussing on a single work. This appraoch can help in acheiving a great **test coverage**. Read more about testing in mule [here.](Testing.md)
- Only the variables required for the flow must be defined.
- External Component calls must be equipped with exception handling
- To advocate reusablity and individualizing of logics, flow references must be used.

### API URL:
API URL plays an important role in organizing and categorizing the APIs. An optimal API URLs should map to the business domains and process they are catering to. The following should be considered while designing the API URL.
- **Environment** the API belongs to.
- Specify which **Organization** the API belongs to.
- API **Layer** it belongs
- It should specify the **Version** of the API
- It should specify the **Business Unit** if applicable.
- It should specify the **Business Process** this API belongs to.




