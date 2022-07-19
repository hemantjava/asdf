# spring-boot-flyway
 Spring Boot Database Migrations with Flyway
 Solution for jsonb type
 -----------------------
 Spring:
  datasource:
    url: jdbc:h2:mem:db;DB_CLOSE_DELAY=-1;INIT=RUNSCRIPT FROM 'classpath:init.sql'
    username: sa
    password:
    driver-class-name: org.h2.Driver
  jpa:
    database-platform: org.hibernate.dialect.PostgreSQL95Dialect
    hibernate:
      ddl-auto: create-drop
	  
----------------init.sql----------------
CREATE domain IF NOT EXISTS jsonb AS other;	  
