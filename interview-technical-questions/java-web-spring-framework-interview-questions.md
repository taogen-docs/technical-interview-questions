# Spring Framework Interview Questions

### Content

- Introduction
  - [x] [Q: What is Spring Framework?](#Q: What is Spring Framework?)
  - [x] [Q: What are the Benefits of Using Spring?](#Q: What are the Benefits of Using Spring?)
  - [x] [Q: What Spring Sub-Projects Do You Know?Describe Them Briefly.](#Q: What Spring Sub-Projects Do You Know?Describe Them Briefly.)
- [Core Technologies](#Core Technologies)
  - [IoC Container](#IoC Container)
    - [x] [Q: What are Dependency Injection (DI) and Inversion of Control (IoC)?](#Q: What are Dependency Injection (DI) and Inversion of Control (IoC)?)
    - [ ] [Q: How Can We Inject Beans in Spring?](#Q: How Can We Inject Beans in Spring?)
    - [ ] [Q: Which is the Best Way of Injecting Beans and Why?](#Q: Which is the Best Way of Injecting Beans and Why?)
    - [ ] [Q: What is the Difference between BeanFactory and ApplicationContext?](#Q: What is the Difference between BeanFactory and ApplicationContext?)
    - [ ] [Q: What is a Spring Bean?](#Q: What is a Spring Bean?)
    - [ ] [Q: What is Default Bean Scope in Spring Framework?](#Q: What is Default Bean Scope in Spring Framework?)
    - [ ] [Q: How to Define the Scope of a Bean?](#Q: How to Define the Scope of a Bean?)
    - [ ] [Q: Are Singleton Beans Thread-Safe?](#Q: Are Singleton Beans Thread-Safe?)
    - [ ] [Q: What Does the Spring Bean Lifecycle Look Like?](#Q: What Does the Spring Bean Lifecycle Look Like?)
    - [ ] [Q: What is the Spring Java-Based Configuration?](#Q: What is the Spring Java-Based Configuration?)
    - [ ] [Q: Can We Have Multiple Spring Configuration Files in One Project?](#Q: Can We Have Multiple Spring Configuration Files in One Project?)
    - [ ] [Q: How Does the Scope Prototype Work?](#Q: How Does the Scope Prototype Work?)
  - Resources
  - Validation, Data Binding, and Type Conversion
  - Spring Expression Language (SpEL)
  - Aspect Oriented Programing with Spring
    - [ ] Q: What is Aspect-Oriented Programming?
    - [ ] Q: What are Aspect, Advice, Pointcut, and JoinPoint in APO?
    - [ ] Q: What is Weaving?
- Testing
- Data Access
  - [ ] Q: What is Spring JdbcTemplate Class and How to Use It?
  - [ ] Q: How would you Enable Transactions in Spring and What Are Their Benefits?
  - [ ] Q: What is Spring Dao?
  - Transaction Management
  - DAO support
  - Data Access with JDBC
  - ORM Data Access
  - Marshalling XML
- The Web
  - Web MVC framework
    - [ ] Q: How to Get ServletContext and ServletConfig Objects in a Spring Bean?
    - [ ] Q: What is a Controller in Spring MVC?
    - [ ] Q: How Does the @RequestMapping Annotation Work?
  - View technologies
  - CORS Support
  - Integrating With Other Web Framework
  - WebSocKet Support
  - Web Reactive Framework
    - [ ] Q: What is Reactive Programming?
    - [ ] Q: What is Spring Webflux?
- Integration
- Others
  - [ ] Q: Name Some of the Design Patterns Used in the Spring Framework?
  - [ ] Q: What is Spring Boot?
  - [ ] Q: What is Spring Security?
- References



## Introduction

### Q: What is Spring Framework?

>The Spring Framework provides a comprehensive programming and configuration model for modern Java-based enterprise applications - on any kind of deployment platform.

> A key element of Spring is infrastructural support at the application level: Spring focuses on the "plumbing" of enterprise applications so that teams can focus on application-level business logic, without unnecessary ties to specific deployment environments.

> The Spring Framework is a Java platform that provides comprehensive infrastructure support for developing Java applications. Spring handles the infrastructure so you can focus on your application.

In my opinion, the Spring framework is **a infrastructure framework** or **a Java application infrastructure platform** that does a lot of infrastructure things to help you focus on your application business logic development. In addition, the Spring framework is non-intrusive, meaning that your domain logic code generally has no dependencies on the framework itself.

### Q: What are the Benefits of Using Spring?

Spring targets to make Jakarta EE development easier. Here are the advantages of using it:

- **Lightweight:** there is a slight overhead of using the framework in development
- **Inversion of Control (IoC):** Spring container takes care of wiring dependencies of various objects, instead of creating or looking for dependent objects
- **Aspect Oriented Programming (AOP):** Spring supports AOP to separate business logic from system services
- **IoC container:** it manages Spring Bean life cycle and project specific configurations
- **MVC framework:** that is used to create web applications or RESTful web services, capable of returning XML/JSON responses
- **Transaction management:** reduces the amount of boiler-plate code in JDBC operations, file uploading, etc., either by using Java annotations or by Spring Bean XML configuration file
- **Exception Handling:** Spring provides a convenient API for translating technology-specific exceptions into unchecked exceptions

### Q: What Spring Sub-Projects Do You Know?Describe Them Briefly.

- **Core** – a key module that provides fundamental parts of the framework, like IoC or DI
- **JDBC** – this module enables a JDBC-abstraction layer that removes the need to do JDBC coding for specific vendor databases
- **ORM integration** – provides integration layers for popular object-relational mapping APIs, such as JPA, JDO, and Hibernate
- **Web** – a web-oriented integration module, providing multipart file upload, Servlet listeners, and web-oriented application context functionalities
- **MVC framework** – a web module implementing the Model View Controller design pattern
- **AOP module** – aspect-oriented programming implementation allowing the definition of clean method-interceptors and pointcuts

## Core Technologies

### IoC Container

### Q: What are Dependency Injection (DI) and Inversion of Control (IoC)?

**Inversion of Control** (IoC) is also known as dependency injection (DI). It is a process whereby objects define their dependencies, that is, the other objects they work with, only through constructor arguments, arguments to a factory method, or properties that are set on the object instance after it is constructed or returned from a factory method. The container then injects those dependencies when it creates the bean. This process is fundamentally the inverse, hence the name Inversion of Control (IoC), of the bean itself controlling the instantiation or location of its dependencies by using direct construction of classes, or a mechanism such as the Service Locator pattern.

Inversion of Control is a principle in software engineering by which the control of objects or portions of a program is transferred to a container or framework. It's most often used in the context of object-oriented programming.

The advantages of this architecture are:

- decoupling the execution of a task from its implementation
- making it easier to switch between different implementations
- greater modularity of a program
- greater ease in testing a program by isolating a component or mocking its dependencies and allowing components to communicate through contracts

Inversion of Control can be achieved through various mechanisms such as: Strategy design pattern, Service Locator pattern, Factory pattern, and Dependency Injection (DI).

**Dependency Injection**, an aspect of Inversion of Control (IoC), is a general concept stating that you do not create your objects manually but instead describe how they should be created. An IoC container will instantiate required classes if needed.

### Q: How Can We Inject Beans in Spring?

Inject Beans Ways:

- Setter Injection
- Constructor Injection
- Field Injection

The configuration can be done using XML files or annotations.

### Resources

### Validation, Data Binding, and Type Conversion

### Spring Expression Language (SpEL)

### Aspect Oriented Programing with Spring

### Spring AOP APIs

## Testing

## Data Access

## The Web

### Web MVC framework

## Integration



## References

[1] [Spring Framework Reference 5.0.0](https://docs.spring.io/autorepo/docs/spring-framework/5.0.0.M1/spring-framework-reference/htmlsingle/)

[2] [Top Spring Framework Interview Questions](https://www.baeldung.com/spring-interview-questions)

[3] [Intro to Inversion of Control and Dependency Injection with Spring](https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring)