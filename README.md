# Microservices

This Document will describe how the different spring cloud components will be added in a project and how they work together. I will use different branches for the different spring cloud packages. The Master Branch has the whole project included. The documentation will have a focus on deploying the spring cloud environment in Cloud Foundry on the SAP Cloud Platform.

**Table of Contents**

* [Config Server (Distributed Configuration)](#config)
* [Eureka Server (Discovery Service)](#eureka)
* [Zuul (API Gateway / Intelligent Routing)](#zuul)
* [Feign](#feign)
* [Hystrix (Circuit Breaker)](#hystrix)
* [Sleuth](#sleuth)
* [Zipkin](#zipkin)
* [Spring Cloud Stream](#cloudstream)
* [Links](#links)

# Config Server (Distributed Configuration)<a name="config"></a>

The Config Server is the central source of all configuration files which are saved in an own  git repository. So its an distributed configuration to all connected microservices.

 ## 1. Generating Spring Boot Application

 ## 2. @EnableConfigServer in Applikation

 ## 2. Store Config in file system

 ## 2. Store Config in git


# Eureka Server (Discovery Service)<a name="eureka"></a>

 Eureka client and server


# Zuul (API Gateway / Intelligent Routing<a name="zuul"></a>
Feign / Ribbon ( Client-side Load Balancing)

# Hystrix (Circuit Breaker)<a name="hystrix"></a>

# Sleuth<a name="sleuth"></a>

# Zipkin<a name="zipkin"></a>

# Spring Cloud Stream<a name="cloudstream"></a>

# Links<a name="links"></a>
 - https://blog.novatec-gmbh.de/spring-cloud-sprint-a-fast-and-comprehensive-spring-cloud-services-tutorial/#flight-aggregation-frontend-impl
- https://github.com/joshlong/cloud-native-workshop
