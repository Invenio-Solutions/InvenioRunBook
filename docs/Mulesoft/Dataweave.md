
## DataWeave:

Dataweave tools are primarily used for querying and transformation of data in Mule. The detailed information of Dataweave can be found [here](https://docs.mulesoft.com/mule-runtime/3.9/dataweave). The important things that must be considered in dataweave are as follows:
- The coding must be simple and clear.
- Dataweave libraries must be leveraged before creating our own functions.
- It is important that we provide sample data for testing the transformation.
- Use of inline scripts in dataweave is recommended.
- The input content type must be defined.
- Externalizing those scripts for reuse is preferrable.
- The directive indent can be set to false in dataweave while dealing with large payloads to reduce the response payload size.
