# API Coding Standards

For an organized, comprehensible and a sustainable project, it is imperative that we follow certain coding standards. They are summarized as below:

- It is very important that sensitive data such as values, hosts, URLs etc are never hardcoded. Including these as its encrypted version is recommended.
- Payload logging should be avoided in order to ensure better performance and security of the appplication.
- Naming conventions should be followed in order to ease the identification process of the flow, sub-flows etc. The details related to naming conventions can be found [here](API_Implementation.md)
- To ensure consistency, incorporation of common logging and error handling frameworks is encouranged.
- Field Validations should be carried out at the initial stage of the Flow.
- Latest version of connectors must be included.
- To falicitate extendability and reusability and prevent duplicacy, sub-flows can be created.
- The third-party libraries should be included in the pom.xml
- Creating copies of the payload as variales is not encouraged.
- All possible runtime exceptions must be handled in mule. Detailed overview can be obtained in [here](Error Handlong.md)