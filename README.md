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
3. If possible, it should send some location/path/uri to the next possible options/API along with the data either in the response header or using HATEOS tech.
4. Each API must return a common exception structure.
5. Whenever some classes needs to be shared among all the controller implementation, it needs to be annotated with @ControllerAdvice.
6. Each API should have ability to validate it's parameters.
7. Each API should have proper documentation based on openAPI specification.
8. Each service must expose specific actuator resources like health check and some visualization of API (using something like HAL explorer). 
9. API may have different versioning. Some of the examples of versioning are as follows,
   - **URI versioning** : Used by Twitter (different URI for different version)
   - **Custom Header versioning** : Used by Microsoft
   - **Request Param versioning** : Used by Amazon
   - **Aceept Header or Content Negotiation versioning** : Used by Github

10. Filtering can be added to filter out some of the fields from the beans returned in the response.
11. Each internal GET API should return  Optional<SomeBean>.
12. Make the best use of HTTP 
13. Always use plural in the resource naming and think about nown most of the cases.
 
## What is a Microservice?
1. Exposed using REST
2. Small code unit with proper boundary and which is easily deployable. 
3. Cloud Enabled 
 
### Challenges associated with microservice
1. Boundary identifications - Evaluationary process - Domain design
2. Configuration Management - Multiple environment with multiple instances - Spring Cloud Config Service
3. Dynamic Load handling - Scaling
4. Load Balancing - distribution 
   a. Naming or Discovery Service - Eureka
   b. Client Side Load Balancing - Ribbon
   c. REST Client with the naming service set up - Feign
5. Visibility of each service - Logging/Tracking of a request & Monitoring
   a. ZIPKIN Distributed Tracing mechanism
   b. Netflix API Zul Gateway.
6. CAP Principal 
7. Fault Tolearance - Hystrix
8. Security
9. Analytics 
 
## Advantages of microservice archiecture
1. Make the adaptation of new technology easy - Tech stack of microservices can be completely different
2. Dynamic Scaling
3. Faster Developement and Release cycle. 
4. Easy deployment. 
