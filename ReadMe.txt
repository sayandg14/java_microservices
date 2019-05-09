cloud config server==>
spring-cloud-config-server
@EnableConfigServer
spring.cloud.config.server.git.uri=file://D:/work/downloaded projects/local_git_repository

config client==>
spring-cloud-starter-config
@ConfigurationProperties("limits-service")

eureka server==>
@EnableEurekaServer
spring-cloud-starter-netflix-eureka-server
spring-cloud-starter-config
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false

rest client==>
spring-cloud-starter-netflix-eureka-client
spring-cloud-starter-config
@EnableDiscoveryClient
@EnableFeignClients("com.in28minutes.microservices.currencyconversionservice")	
eureka.client.service-url.default-zone=http://localhost:8761/eureka

