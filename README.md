# SpringCloud

Spring Cloud try to solve.

1. Configuration maintainability



Configuration maintainability:

In microservice environment, the microservices can be multiple, it can have multiple instances in each environment, maintaining these information/configuration will be challaging. To resolve the issue, these configurations can be stored in centralized repository, for example, git and SpringCloudConfigServer can be used to read it and share with the all the microservices.


Dynamic scale up & down:

Eureka - Naming server.  -> all microservices will need to register in Eureka. It will provide current instances details to the calling service
Ribbon - Client side load balancing.  It help to trace log in multiple components. It distribute the load into underlying service instances
But in new version, Ribbon has been replaced by Spring cloud loadbalancer.
Feign - REST client
Zuul - dynamic routing but in latest version, it has been replaced by Spring cloud gateway


Visibility & Monitoring

1. Zipkin distributed tracing - It will add unique tracable id to the underlying services. 
2. Netflix API gateway

Fault tolerance:

Hystrix.  - In latest version, it has been replaced by Resilience4j as circuit breaker
