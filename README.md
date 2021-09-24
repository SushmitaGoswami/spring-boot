# Spring Boot

## What is a webservice?
 Webservice is a distributable package made out of business and data layer of a solution. Following are 3 properties each webservice must possesses...
 - Web services must be able to communicate over the network.
 - Implementation and Interfaces must be platform independent.
 - It should allow machine to machine communication, not application to application communication.


## How can a service be platform independent?
Request and response of a service must follow a standard format. It is defined by Service Definitions. 

**Service definitions**
1. Request/Response format
2. Request structure
3. Response structure
4. Endpoint

## Types of webservice
1. SOAP
2. REST

## What is SOAP?
SOAP possess a restriction on the request and response structure of a webservice. The format each webservice implementing SOAP model, must follow is as follows
a. SOAP Request Format - 
    - SOAP envelope 
      - SOAP Request
      - SOAP Response
      
b. Request/Response - SOAP XML Request/Response
c. Transport - HTTP/MQ
d. Service Definition - WSDL (Web Service Definition Language)

## What is REST?
Representational state transfer - It is an architectural style which guides the design and development of the architecture for the World Wide Web.
1. Request/Response - JSON/XML/Any standard
2. Transport - HTTP
3. Service Definition - Nothing fixed, but Swagger/WADL is used for this purpose.
