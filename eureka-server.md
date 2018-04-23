# Eureka Server (Discovery Service)<a name="eureka"></a>

Eureka Server is a discovery service ...

### 1. Generating Spring Boot Application
 Generate a Spring Boot application with the **Eureka Server** and **Config Client** dependency

#### build.gradle
[buil.gradle]()TODOLINK in Github eureka-server branch
```gradle
compile('org.springframework.cloud:spring-cloud-starter-config')
compile('org.springframework.cloud:spring-cloud-starter-netflix-eureka-server')
```
<img src="./gifs/create-eureka-server.gif"/>

### 2. @EnableEurekaServer in *EurekaServerApplication*
[EurekaServerApplication]()TODO in Github
```kotlin
@EnableEurekaServer
@SpringBootApplication
class EurekaServerApplication
fun main(args: Array<String>) {
    runApplication<EurekaServerApplication>(*args)
}
```

### 3. delete application.properties and add a bootstrap.properties

##### bootstrap.properties
```ini
spring.application.name=eureka-server
spring.cloud.config.uri=${vcap.services.config-server.credentials.uri:http://localhost:8888}
```

## 4. Create eureka-server config in config repository
**IMPORTANT**: The config name should be the same as the spring.application.name eureka-server.properties

##### eureka-server.properties 
[eurea-server.properties example](https://github.com/arthurliebhardt/spring-cloud-configs-example/blob/master/eureka-server.properties)
```ini
server.port=${PORT:8761}

eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
```

## 3. Test it locally
For testing it locally you need to start first the config-server and then the eureka-server. IntelliJ IDEA provides and Spring Run dashboard where you can start, debug, stop multiple Spring Boot Applications.

IntelliJ IDEA detects two spring boot applications and shows an Run Dashboard popup:

<img src="./imgs/run-dashboard-popup.png"/>

After opening the Run Dashboard it shoud look like this:

<img src="./imgs/run-dashboard.png"/>
