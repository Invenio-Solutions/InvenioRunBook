---
sidebar_position: 17
---
# XML Signature
XML signatures are useful in securing data and provide data integrity. W3C provides recommendations for governance of XML Signature. XML Signature is also used to secure data of any type.

## XML Signature in Java

Java API supports [generating and validating XML signatures](https://docs.oracle.com/javase/9/security/xml-digital-signature1.htm#JSSEC-GUID-6A9B51CC-8FAD-4627-AE58-7AA7C2E4436F) as per the recommended guidelines. Java XML Digital Signature API is encapsulated in the package “java.xml.crypto“.

The signature itself is just an XML document. There are three types of  XML signatures.
- **Detached**: This type of signature is over the data that is external to the Signature element.
- **Enveloping**: This type of signature is over the data that is internal to the Signature element.
- **Enveloped**: This type of signature is over the data that contains the Signature element itself.
Java supports creating and verifying of all the above mentioned types of XML Signatures.