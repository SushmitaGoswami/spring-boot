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

Each api is represented as an API. Following are some examples
1. GET user - /user/{id}
2. GET all posts of an user - /user/{id}/posts


## How does dispatcher servlet works?
Dispatcher servlet specifies the root of the application It maintains the mapping between resource and controller. It registers all the jars which it finds in the classpath.
Whenever, dispatcher servlet receives any request, it finds the controller mapping of the corresponding url and forwards the request based on that. Now, as @ResponseBody annotation is attached to the @RestController class, so when the response is returned to the client, it is converted into specific format dependending on the mapper class found in the classpath and registered.

## Some checkpoints of rest api
1. Each API should have proper return code.
2. Each API must have some fallback.
3. If possible, it should send some location/path/uri to the next API to be used in the response header.
4. Each API must return a common exception structure.
5. Whenever some classes needs to be shared among all the controller implementation, it needs to be annotated with @ControllerAdvice.
6. Each API should have ability to validate it's parameters.
7. Each API should have proper documentation based on openAPI specification.
8. Each service must expose specific actuator resources like health check and some visualization of API (using something like HAL explorer). 
