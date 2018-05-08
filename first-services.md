# First Service (Microservice)<a name="first-service"></a>
In this chapter we will create a simple microservices via an Spring Boot Application.

### 1. Generating Spring Boot Application
Generate a Spring Boot application with and `Config Client`, `Eureka Discovery` and `Web` dependency

##### build.gradle [GitHub]()
```gradle
compile('org.springframework.boot:spring-boot-starter-web')
compile('org.springframework.cloud:spring-cloud-starter-config')
compile('org.springframework.cloud:spring-cloud-starter-netflix-eureka-client')
```
//TODO Create GIF
<img src="./gifs/create-first-service.gif"/>


### 2. Implement `FirstServiceApplication`
Our `Eureka Server` will be able to find our first service with the help of the `@EnableEurekaClient` annotation. Furthermore we implement an simple Restcontroller which responds on a GET Request at `/hello`

##### FirstServiceApplication [GitHub]() 

```kotlin
@EnableEurekaClient
@RestController
@RequestMapping("/hello")
@SpringBootApplication
class FirstServiceApplication {

    @GetMapping
    fun sayHello(): String = "hello from our first service!"
}

fun main(args: Array<String>) {
    runApplication<FirstServiceApplication>(*args)
}
```

### 3. Delete `application.properties` and add a `bootstrap.properties`

##### bootstrap.properties [GitHub]()
```ini
spring.application.name=first-service
spring.cloud.config.uri=${vcap.services.config-server.credentials.uri:http://localhost:8888}
```
### 4. Create `eureka-server.properties` config in config repository
**IMPORTANT**: The config name should be the same as the `spring.application.name`. In our case `first-service.properties`.

##### first-service.properties [GitHub Config Server]()

```ini
server.port=${PORT:8081}
```