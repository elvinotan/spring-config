# Spring-Config-Server
Spring Cloud Config adalah salah satu feature dari Netflix yang memungkinkan konfigurasi di atur oleh server ini. Konfigurasi yang di simpan di server ini bukan hanya untuk service ini, tp bisa juga untuk semua service yang ada.</br> 
Cara kerja dari Spring Config Server ini adalah pada saat server ini booting dia akan mencari bootstrap.yml yang memiliki property letak dari konfigurasi file

# Dependencies
Config Server

# How to
1. Tambahkan <code>@EnableConfigServer</code> pada SpringBootApplication class, dgn konfigursi ini menandakan bila server ini akan di gunakan sebagi config server, dan akan error bila property <code>spring.cloud.config.server.git.uri</code> tidak tersedia.
```
@EnableConfigServer
@SpringBootApplication
public class ServerApplication {
	
	public static void main(String[] args) {
		SpringApplication.run(ServerApplication.class, args);
	}
	
}
```
2. Buatlah bootstrap.yml sebagai pengganti application.properties. 
```
---
spring:
  cloud:
    config:
      server:
        git:
          uri: https://github.com/elvinotan/config

server:
  port: 9080
```
3. Untuk Setup sisi server selesai, next please refer to spring-config-client

# note
Contoh lain ```https://github.com/kennyk65/Microservices-With-Spring-Student-Files/tree/master/lab-3/server-solution```
