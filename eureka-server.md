# Eureka Server (Discovery Service)<a name="eureka"></a>

Eureka Server is a discovery service ...

### 1. Generating Spring Boot Application
 Generate a Spring Boot application with the **Eureka Server** dependency

#### build.gradle
[buil.gradle]()TODOLINK in Github eureka-server branch
```gradle
compile('org.springframework.cloud:spring-cloud-starter-netflix-eureka-server')
```
<img src="./gifs/create-eureka-server.gif"/>

### 2. @EnableEurekaServer in *EurekaServerApplication*
[EurekaServerApplication]()TODO in Github
```kotlin
@SpringBootApplication
@EnableConfigServer
class ConfigServerApplication
fun main(args: Array<String>) {
runApplication<ConfigServerApplication>(*args)
}
```