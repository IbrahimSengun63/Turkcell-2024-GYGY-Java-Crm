# 🟡 Turkcell Crm Project - GYGY 3.0 - İbrahim şengün


This project was carried out within the scope of Turkcell Youth Investment Software for the Future 3.0 Java programme. With the 120-hour course, it was decided to do the project in groups. I took part in the development process of CustomerService from start to finish in the group I was in. 

We carried out our work by creating a common organisation on GitHub. At the same time, we used it as a configuration server by creating a repository in our common github organisation. You can access the project's configuration server from  [this link](https://github.com/IbrahimSengun63/Turkcell-2024-GYGY-Java-Crm-Configurations) in my repository. In addition, we used it effectively by creating a common page on Figma to analyse the project and determine the requirements and follow the development. Each group member was responsible for the service/server that fell on him.



## Hi, I'm İbrahim! 👋 I have a little more information for you:

In this project I was involved in the development of the Micro service setup and configurations with docker and without docker(local) from start to finish. Here are the main topics I covered during the development process:
- Creation of microservices
- Git branch strategy and settings for the group project within the organization
- Docker settings and network configurations for Docker Compose
- Microservice separations and folder structures
- Microservices POM XML configurations for both local build and Docker build
- Container and image setup and configurations for Docker
- Configuring the database with code-first using JPA Hibernate
- Establishment of DTOs (Data Transfer Objects)
- Config server setup
- Eureka configurations and setup
- Auth server security and user development
- Base server for security and package management
- Creation of managers and implementation of services
- Creation of controllers
- Performing validations
- Creation of business rules
- Ensuring global exception handling
- Testing via Docker
🚀 I am happy to have completed the auth server, base server (core), and microservices setup and configurations development after a very instructive and developing process. It has been a very useful experience for me. I spent productive time both analyzing and coding the project, as well as during the testing phase.

🙏 At the end of the day, I would like to thank Turkcell and all those who contributed to this process. My Linkedin address if you want to take a look:

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ibrahim-sengun63/)
## Endpoints

The following table lists the end points that authserver and coreserver has. The table includes the endpoint URL, http status, request and response return values. Under the [DTOs](#dtos) heading, the contents of the request and response values are shown.

| Endpoint                                 | HTTP  | Parameters                          | Response        | Returns                                             | Explanation                                                         | Error                    |
|------------------------------------------|-------|-------------------------------------|-----------------|-----------------------------------------------------|---------------------------------------------------------------------|--------------------------|
| **api/v1/auth/user/customer/register**   | POST  | Email: Unique<br>Password: String   | 200 OK          | User_id: int<br>Email: String<br>Role: String       | If successful, it will create a customer.                           | Duplicate Email          |
| **api/v1/auth/user/admin/register**      | POST  | Email: Unique<br>Password: String   | 200 OK          | User_id: int<br>Email: String<br>Role: String       | Restricted to users with admin authority. If successful, it will create an admin. | Duplicate Email          |
| **api/v1/auth/user/customer/login**      | POST  | Email: String<br>Password: String   | 200 OK          | User_id: int<br>Email: String<br>Role: String<br>Token: String | If successful, it will log in the user.                            | Bad Credentials          |
| **api/v1/auth/user/admin/login**         | POST  | Email: String<br>Password: String   | 200 OK          | User_id: int<br>Email: String<br>Role: String<br>Token: String | If successful, it will log in the admin.                            | Bad Credentials          |
| **api/v1/auth/token**                    | POST  | Token: String                       | 200 OK          | User_id: int<br>Email: String<br>Role: String       | If successful, it will extract user credentials from the token.     | Bad token<br>Token Expired |




## Sample Screenshots

![Customer register](https://github.com/IbrahimSengun63/Turkcell-2024-GYGY-Java-Crm/assets/67779798/bdeef811-1173-4adf-bf5c-30067a02bee2)
![Customer login](https://github.com/IbrahimSengun63/Turkcell-2024-GYGY-Java-Crm/assets/67779798/41a688b3-a7fc-4bff-88d9-052d421552f7)
![Customer login bad request](https://github.com/IbrahimSengun63/Turkcell-2024-GYGY-Java-Crm/assets/67779798/13bd0170-f9f0-4e70-b103-519867708432)
![Customer register email validation check](https://github.com/IbrahimSengun63/Turkcell-2024-GYGY-Java-Crm/assets/67779798/9a93d349-be70-4f60-a7e2-24e13cca77f5)
![Customer email duplicate check](https://github.com/IbrahimSengun63/Turkcell-2024-GYGY-Java-Crm/assets/67779798/85e58d08-5960-4ae3-a861-ecea9710c209)
![Token extraction](https://github.com/IbrahimSengun63/Turkcell-2024-GYGY-Java-Crm/assets/67779798/cca02cd2-c087-4f73-84e0-e044d5119b8f)



## DTOs

#### RequestLoginUser 

```java 
    private String email;
    private String password;
```

#### RequestRegisterUser

```java
    private String email;
    private String password;
    private String role;
```

#### RequestUserFromToken

```java
    private String token;
```

#### ResponseLoginUser

```java
    private int id;
    private String email;
    private String role;
    private String token;
```

#### ResponseRegisterUser

```java
    private int id;
    private String email;
    private String role;
```
#### ResponseUserFromToken

```java
    private int id;
    private String email;
    private String role;
```


## Learned

In this project and 120 hours of learning:
- JPA Hibernate
- N-tier Architecture
- Docker setup and configurations
- Micro service setup and configurations
- Config server setup and configurations
- Discovery server setup and configurations
- Gateway server setup and configurations
- Core package management and devolopment
- Java and docker build configurations
- Spring Boot
- PostgreSQL
- Lombok
- Maven

and many more important things for backend developer so for me 😄

It was a process in which I learned and started to apply what I learned. I will continue to use what I have learned and increase my knowledge. Keep moving 🚀
