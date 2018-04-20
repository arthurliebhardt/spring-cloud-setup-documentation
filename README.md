# Empty gradle Project

This is the "core" project where all other projects will be added. We can share dependencies for all Projects within the root gradle file.

 ## 1. Generating Spring Boot Application
 Generate a Spring Boot application with the **config server** dependency
 
 <img src='gifs/create-config-server.gif' />

 ## 2. @EnableConfigServer in *ConfigServerApplication*
 
 ```
 @SpringBootApplication
 @EnableConfigServer
 class ConfigServerApplication
 
 fun main(args: Array<String>) {
     runApplication<ConfigServerApplication>(*args)
 }
 ```
 

 ## 2. Store Config in file system
 
 ```
 @SpringBootApplication
 @EnableConfigServer
 class ConfigServerApplication
 
 fun main(args: Array<String>) {
     runApplication<ConfigServerApplication>(*args)
 }
 ```

 ## 2. Store Config in git
 
 create config folder and add an example property for example *hello-service.properties*
 
 
