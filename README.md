# Microservices

<img src="./imgs/spring-cloud.png"/>

This Document will describe how the different spring cloud components will be added in a project and how they work together. I will use different branches for the different spring cloud packages. The Master Branch has the whole project included. The documentation will have a focus on deploying the spring cloud environment in Cloud Foundry on the SAP Cloud Platform.

**Table of Contents**

* [Create empty gradle project](#bootstrap)
* [Config Server (Distributed Configuration)](#config)
* [Eureka Server (Discovery Service)](#eureka)
* [Zuul (API Gateway / Intelligent Routing)](#zuul)
* [Feign](#feign)
* [Hystrix (Circuit Breaker)](#hystrix)
* [Sleuth](#sleuth)
* [Zipkin](#zipkin)
* [Spring Cloud Stream](#cloudstream)
* [Links](#links)

# Create empty gradle project<a name="bootstrap"></a>

First we need to create a core project for our whole spring cloud environment

<img src="./gifs/create-empty-gradle-project.gif"/>

The empty project should look like [this](https://github.com/arthurliebhardt/spring-cloud-setup-documentation/tree/empty-gradle-project) than.



# Eureka Server (Discovery Service)<a name="eureka"></a>

 Eureka client and server, Configuration, Health & High Availability, sDashboard

### 1. Generating Spring Boot Application
 Generate a Spring Boot application with the **Eureka server** dependency

# Zuul (API Gateway / Intelligent Routing<a name="zuul"></a>
Feign / Ribbon ( Client-side Load Balancing)

# Hystrix (Circuit Breaker)<a name="hystrix"></a>

# Sleuth<a name="sleuth"></a>

# Zipkin<a name="zipkin"></a>

# Spring Cloud Stream<a name="cloudstream"></a>

# Links<a name="links"></a>
 - https://blog.novatec-gmbh.de/spring-cloud-sprint-a-fast-and-comprehensive-spring-cloud-services-tutorial/#flight-aggregation-frontend-impl
- https://github.com/joshlong/cloud-native-workshop
- https://blogs.sap.com/2017/11/08/centralized-configuration-of-spring-boot-applications-using-sap-cloud-platform/
-https://www.youtube.com/watch?v=5q8B6lYhFvE - Cloud Native Java - Josh Long