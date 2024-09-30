# Spring Boot Interview Questions

### Content

- [Introduction](#Introduction)
  - [x] [Q: What is Spring Boot?](#Q: What is Spring Boot?)
  - [x] [Q: Spring vs Spring Boot?](#Q: Spring vs Spring Boot?)
  - [x] [Q: What is Spring Boot and mention the need for it?](#Q: What is Spring Boot and mention the need for it?)
  - [x] [Q: Mention the Advantages of Spring Boot?](#Q: Mention the Advantages of Spring Boot?) (What are the advantages of Spring Boot?)
  - [x] [Q: Mention the Disadvantages of Spring Boot?](#Q: Mention the Disadvantages of Spring Boot?)
  - [x] [Q: Mention a few features of Spring Boot?](#Q: Mention a few features of Spring Boot?)
- [Using Spring Boot](#Using Spring Boot)
  - [Build Systems, Dependency Management, Starters](#Build Systems, Dependency Management, Starters)
    - [x] [Q: Mention the minimum requirements for a Spring boot System?](#Q: Mention the minimum requirements for a Spring boot System?)
    - [x] [Q: Explain How to create Spring Boot application using Maven?](#Q: Explain how to create Spring Boot application using Maven?)
    - [x] [Q: Mention the steps to create a Spring Boot project using Spring  Initializr?](#Q: Mention the steps to create a Spring Boot project using Spring  Initializr?)
    - [x] [Q: How to create Spring Boot Project using boot CLI?](#Q: How to create Spring Boot Project using boot CLI?)
    - [x] [Q: How to create Spring Boot application using Spring Starter Project Wizard?](#Q: How to create Spring Boot application using Spring Starter Project Wizard?)
    - [x] [Q: Can we create a non-web application in Spring Boot?](#Q: Can we create a non-web application in Spring Boot?)
    - [x] [Q: Do you think, you can use jetty instead of tomcat in spring-boot-starter-web?](#Q: Do you think, you can use jetty instead of tomcat in spring-boot-starter-web?)
    - [x] [Q: What are the Spring Boot starters and what are available the starters?](#Q: What are the Spring Boot starters and what are available the starters?)
    - [x] [Q: What is Spring Boot dependency management?](#Q: What is Spring Boot dependency management?)
  - [Structuring Your Code, Main Application Class](#Structuring Your Code, Main Application Class)
    - [x] [Q: What are the differences between @SpringBootApplication and @EnableAutoConfiguration annotation?](#Q: What are the differences between @SpringBootApplication and @EnableAutoConfiguration annotation?)
  - [Configuration Classes](#Configuration Classes)
    - [x] [Q: What are the Spring Boot properties?](#Q: What are the Spring Boot properties?)
    - [x] [Q: Can we change the port of the embedded Tomcat server in Spring boot?](#Q: Can we change the port of the embedded Tomcat server in Spring boot?)
    - [x] [Q: What is the best way to expose custom application configuration with Spring Boot?](#Q: What is the best way to expose custom application configuration with Spring Boot?)
    - [x] [Q: Mention the advantages of the YAML file than Properties file and the different ways to load YAML file in Spring boot?](#Q: Mention the advantages of the YAML file than Properties file and the different ways to load YAML file in Spring boot?)
  - [Auto Configuration](#Auto Configuration)
    - [x] [Q: What do you understand by auto-configuration in Spring Boot and how to disable the auto-configuration?](#Q: What do you understand by auto-configuration in Spring Boot and how to disable the  auto-configuration?)
    - [x] [Q: Explain how to register a custom auto-configuration?](#Q: Explain how to register a custom auto-configuration?)
    - [x] [Q: How to instruct an auto-configuration to back off when a bean exists?](#Q: How to instruct an auto-configuration to back off when a bean exists?)
  - [Spring Beans and Dependency Injection](#Spring Beans and Dependency Injection)
    - [x] [Q: What is the difference between RequestMapping and GetMapping?](#Q: What is the difference between RequestMapping and GetMapping?)
  - [Developer Tools](#Developer Tools)
    - [x] [Q: What is the need for Spring Boot DevTools?](#Q: What is the need for Spring Boot DevTools?)
  - [Packaging Application for Production](#Packaging Application for Production)
    - [x] [Q: What are the steps to deploy Spring Boot web applications as JAR and WAR files?](#Q: What are the steps to deploy Spring Boot web applications as JAR and WAR files?)
    - [x] [Q: Mention the differences between WAR and embedded containers?](#Q: Mention the differences between WAR and embedded containers?)
- [Spring Boot Features](#Spring Boot Features)
  - [SpringApplication, Externalized Configuration, Profiles, Logging](#SpringApplication, Externalized Configuration, Profiles, Logging)
    - [x] [Q: Can you explain what happens in the background when a Spring Boot Application is “Run as Java Application”?](#Q: Can you explain what happens in the background when a Spring Boot Application is "Run as Java Application"?)
    - [x] [Q: Mention the possible sources of external configuration?](#Q: Mention the possible sources of external configuration?)
    - [x] [Q: What do you think is the need for Profiles?](#Q: What do you think is the need for Profiles?)
    - [x] [Q: How do you Configure Log4j for logging?](#Q: How do you Configure Log4j for logging?)
    - [x] [Q: What is the way to use profiles to configure the environment-specific configuration with Spring Boot?](#Q: What is the way to use profiles to configure the environment-specific configuration with Spring Boot?)
    - [x] [Q: What do you understand by Spring Boot supports relaxed binding?](#Q: What do you understand by Spring Boot supports relaxed binding?)
  - [Working with Databases, Caching](#Working with Databases, Caching)
    - [x] [Q: Mention the differences between JPA and Hibernate?](#Q: Mention the differences between JPA and Hibernate?)
    - [x] [Q: Mention the steps to connect Spring Boot application to a database using JDBC?](#Q: Mention the steps to connect Spring Boot application to a database using JDBC?)
    - [x] [Q: Explain Spring Data?](#Q: Explain Spring Data?)
    - [x] [Q: How is Hibernate chosen as the default implementation for JPA without any configuration?](#Q: How is Hibernate chosen as the default implementation for JPA without any configuration?)
    - [ ] [Q: What do you understand by Spring Data REST?](#Q: What do you understand by Spring Data REST?)
    - [ ] [Q: How does path=”sample”, collectionResourceRel=”sample” work with Spring Data Rest?](#Q: How does path="sample", collectionResourceRel="sample" work with Spring Data Rest?)
    - [x] [Q: Why is Spring Data REST not recommended in real-world applications?](#Q: Why is Spring Data REST not recommended in real-world applications?)
    - [x] [Q: Mention the dependencies needed to start up a JPA Application and connect to in-memory database H2 with Spring Boot?](#Q: Mention the dependencies needed to start up a JPA Application and connect to in-memory database H2 with Spring Boot?)
    - [x] [Q: Where is the database connection information specified and how does it automatically connect to H2?](#Q: Where is the database connection information specified and how does it automatically connect to H2?)
    - [x] [Q: What is the name of the default H2 database configured by Spring Boot?](#Q: What is the name of the default H2 database configured by Spring Boot?)
  - [REST Services](#REST Services ) 
  - [Other Features](#Other Features)
    - [x] [Q: How to enable HTTP/2 support in Spring Boot?](#Q: How to enable HTTP/2 support in Spring Boot?)
- [Spring Boot Actuator](#Spring Boot Actuator)
  - [x] [Q: What is Spring Boot Actuator?](#Q: What is Spring Boot Actuator?)
  - [x] [Q: Explain Spring Actuator and its advantages?](#Q: Explain Spring Actuator and its advantages?)
  - [x] [Q: How can we create a custom endpoint in Spring Boot Actuator?](#Q: How can we create a custom endpoint in Spring Boot Actuator?)
- [Deploying Spring Boot Applications](#Deploying Spring Boot Applications)
- [Spring Boot CLI](#Spring Boot CLI)
  - [x] [Q: What is Spring Boot CLI and how to execute the Spring Boot project using boot CLI?](#Q: What is Spring Boot CLI and how to execute the Spring Boot project using boot CLI?)
- [Build Tool Plugins](#Build Tool Plugins)
- [References](#References)

## Introduction

### Q: What is Spring Boot?

Spring Boot is a Spring module which provides RAD (Rapid Application Development) feature to Spring framework.

It is used to create stand alone spring based application that you can just run because it needs very little spring configuration.

### Q: Spring vs Spring Boot?

Spring is a web application framework based on Java. It provides tools and libraries to create a complete cutomized web application.

Spring Boot is a spring module which is used to create spring application project that can just run.

| **Spring**                                                   | **Spring** Boot                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| A web application framework based on Java                    | A module of Spring                                           |
| Provides tools and libraries to create customized web applications | Used to create a Spring application project which can just run/ execute |
| Spring is more complex than Spring Boot                      | Spring Boot is less complex than the Spring framework        |
| Takes an unopinionated view                                  | Takes an opinionated view of a platform                      |

### Q: What is Spring Boot and mention the need for it?

Spring Boot is a Spring module which aims to simplify the use of the Spring framework for Java development. It is used to a create stand-alone Spring-based applications which you can just run. So, it basically removes a lot of configurations and dependencies. Aiming at the Rapid Application Development, Spring Boot framework comes with the auto-dependency resolution, embedded HTTP servers, auto-configuration, management endpoints, and Spring Boot CLI.

So, if you ask me why should anybody use Spring Boot, then I would say, Spring Boot not only improves productivity but also provides a lot of conveniences to write your own business logic.

### Q: Mention the Advantages of Spring Boot?

The advantages of Spring Boot are as follows:

- Provides auto-configuration to load a set of default configuration for a quick start of the application
- Creates stand-alone applications with a range of non-functional features that are common to large classes of projects
- It comes with embedded tomcat, servlet containers jetty to avoid the usage of WAR files
- Spring Boot provides an opinionated view to reduce the developer effort and simplify maven configurations
- Provides CLI tool to develop and test applications
- Comes with Spring Boot starters to ensure dependency management and also provides various security metrics
- Consists of a wide range of APIs for monitoring and managing applications in dev and prod.
- Integrates with Spring Ecosystem like Spring JDBC, Spring ORM, Spring Data, Spring Security easily by avoiding boilerplate code.

Other Answer

1. Simplified & version conflict free dependency management through the starter POMs.
2. We can quickly setup and run standalone, web applications and micro services at very less time.
3. You can just assemble the jar artifact which comes with an embedded Tomact, Jetty or Undertow application server and you are ready to go.
4. Spring Boot provides HTTP endpoints to access application internals like detailed metrics, application inner working, health status, etc.
5. No XML based configurations at all. Very much simplified properties. The beans are initialized, configured and wired automatically.
6. The Spring Initializer provides a project generator to make you productive with the certain technology stack from the beginning. You can create a skeleton project with web, data access (relational and NoSQL datastores), cloud, or messaging support.

Other Answer 2

- Create stand-alone Spring applications that can be started using java -jar.
- Embed Tomcat, Jetty or Undertow directly. You don't need to deploy WAR files.
- It provides opinionated 'starter' POMs to simplify your Maven configuration.
- It automatically configure Spring whenever possible.

### Q: Mention the Disadvantages of Spring Boot?

- The biggest challenge many developers face when using Spring Boot is the lack of control. The opinionated style installs **many additional dependencies (that often go unused) which increases the deployment file size**.
- Spring Boot works well with microservices. The Spring Boot artifacts can be deployed directly into Docker containers. However, some developers **don’t recommend the framework for building large and monolithic apps**.
- If you have never worked with Spring before and want to learn about proxies, dependency injection, and AOP programming, it is not recommended to start with Spring Boot because it doesn’t cover most of these details.
- If you are not familiar with other projects of the Spring ecosystem like Spring Security, Spring AMQP, Spring Integration, etc), using them with Spring Boot will make you miss many concepts that you would grasp if you had started using them independently.

### Q: Mention a few features of Spring Boot?

Few important features of Spring Boot are as follows:

1. Spring CLI – Spring Boot CLI allows you to Groovy for writing Spring boot application and avoids boilerplate code.
2. Starter Dependency – With the help of this feature, Spring Boot aggregates common dependencies together and eventually improves productivity
3. Spring Initializer – This is basically a web application, which can create an internal project structure for you. So, you do not have to manually set up the structure of the project, instead, you can use this feature.
4. Auto-Configuration – The auto-configuration feature of Spring Boot helps in loading the default configurations according to the project you are working on. In this way, you can avoid any unnecessary WAR files.
5. Spring Actuator – This feature provides help while running Spring Boot applications.
6. Logging and Security – The logging and security feature of Spring Boot, ensures that all the applications made using Spring Boot are properly secured without any hassle.

Other Answer

- Web Development
- SpringApplication
- Application events and listeners
- Admin features

## Using Spring Boot

### Build Systems, Dependency Management, Starters

### Q: Mention the minimum requirements for a Spring boot System?

Spring Boot 2.1.7.RELEASE requires

- Java 8 +
- Spring Framework 5.1.9 +

Explicit build support

- Maven 3.3+
- Gradle 4.4+

Servlet Container Support

- Tomcat 9.0 – Servlet Version 4.0
- Jetty 9.4 – Servlet Version 3.1
- Undertow 2.0 – Servlet Version 4.0

### Q: Explain how to create Spring Boot application using Maven?

Well, there are various approaches to create a Spring Boot application using maven, but if I have to name a few, then following are the ways to create a Spring Boot project/ application using maven:

- Spring Boot CLI
- Spring Starter Project Wizard
- Spring Initializr
- Spring Maven Project

### Q: Mention the steps to create a Spring Boot project using Spring  Initializr?

Spring Initializr is a web tool provided by Spring. With the help of this tool, you can create Spring Boot projects by just providing project details. The following steps need to be followed to create a Spring Boot project using Spring Initializr:

- Choose the maven project and the required dependencies. Then, fill the other required details like Group, Artifact, and then click on Generate Project.
- Once the project is downloaded, extract the project onto your system
- Next, you have to import this project using the import option on the Spring Tool Suite IDE
  - While importing the project, remember that you have to choose the project type to be Maven and the source project should contain the pom.xml file.

Once, all the above steps are followed you will see that the Spring Boot project is created with all the required dependencies.

### Q: How to create Spring Boot Project using boot CLI?

It is a tool which you can download from the official site of Spring Framework. Here, we are explaining steps.

Download the CLI tool from official site and For more information [click here.](https://www.javatpoint.com/spring-boot-cli)

### Q: How to create Spring Boot application using Spring Starter Project Wizard?

There is one more way to create Spring Boot project in STS (Spring Tool Suite). Creating project by using IDE is always a convenient way. Follow the following steps in order to create a Spring Boot Application by using this wizard.

For more information [click here.](https://www.javatpoint.com/spring-starter-project-wizard)

### Q: Can we create a non-web application in Spring Boot?

Yes, we can create a non-web application by removing the web dependencies from the classpath along with changing the way Spring Boot creates the application context.

### Q: Do you think, you can use jetty instead of tomcat in spring-boot-starter-web?

Yes, we can use jetty instead of tomcat in spring-boot-starter-web, by removing the existing dependency and including the following:

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
    <exclusions>
        <exclusion>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-tomcat</artifactId>
        </exclusion>
    </exclusions>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-jetty</artifactId>
</dependency>
```



### Q: What are the Spring Boot starters and what are available the starters?

Spring Boot starters are a set of convenient dependency management providers which can be used in the application to enable dependencies. These starters, make development easy and rapid. All the available starters come under the org.springframework.boot group. Few of the popular starters are as follows:

- *spring-boot-starter: –* This is the core starter and includes logging, auto-configuration support, and YAML.
- *spring-boot-starter-jdbc –* This starter is used for HikariCP connection pool with JDBC
- *spring-boot-starter-web –* Is the starter for building web applications, including RESTful, applications using Spring MVC
- *spring-boot-starter-data-jpa –* Is the starter to use Spring Data JPA with Hibernate
- *spring-boot-starter-security –* Is the starter used for Spring Security
- *spring-boot-starter-aop:* This starter is used for aspect-oriented programming with AspectJ and Spring AOP
- *spring-boot-starter-test:* Is the starter for testing Spring Boot applications

### Q: What is Spring Boot dependency management?

Spring Boot dependency management is basically used to manage dependencies and configuration automatically without you specifying the version for any of that dependencies.

### Structuring Your Code, Main Application Class

### Q: What are the differences between @SpringBootApplication and @EnableAutoConfiguration annotation?

| **@SpringBootApplication**                                   | **@EnableAutoConfiguration**                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Used in the main class or bootstrap class                    | Used to enable auto-configuration and component scanning in your project |
| It is a combination of @Configuration, @ComponentScan and @EnableAutoConfiguration annotations. | It is a combination of @Configuration and @ComponentScan annotations |



### Configuration Classes

### Q: What are the Spring Boot properties?

Spring Boot provides various properties which can be specified inside our project's **application.properties** file. These properties have default values and you can set that inside the properties file. Properties are used to set values like: server-port number, database connection configuration etc.

### Q: Can we change the port of the embedded Tomcat server in Spring boot?

Yes, we can change the port of the embedded tomcat server by using the application properties file. In this file, you have to add a property of “server.port” and assign it to any port you wish to. For example, if you want to assign it to 8081, then you have to mention server.port=8081. Once you mention the port number, the application properties file will be automatically loaded by Spring Boot and the required configurations will be applied on to the application.

### Q: What is the best way to expose custom application configuration with Spring Boot?

One way to expose the custom application configuration in Spring Boot is by using the **@Value annotation**. But, the only problem with this annotation is that all the configuration values will be distributed throughout the application. Instead, you can use a centralized approach.

By centralized approach, I mean that you can define a configuration component using the @ConfigurationProperties as follows:

```
@Component
@ConfigurationProperties("example")
public class SampleConfiguration {
    private int number;
    private boolean value;
    private String message;
}
```

According to the above snippet, the values configured in application.properties will be as follows:

```
example.number: 100
example.value: true
example.message: Dynamic Message
```

### Q: Mention the advantages of the YAML file than Properties file and the different ways to load YAML file in Spring boot?

The advantages of the YAML file than a properties file is that the data is stored in a hierarchical format. So, it becomes very easy for the developers to debug if there is an issue. The SpringApplication class supports the YAML file as an alternative to properties whenever you use the SnakeYAML library on your classpath. The different ways to load a YAML file in Spring Boot is as follows:

- Use YamlMapFactoryBean to load YAML as a Map
- Use YamlPropertiesFactoryBean to load YAML as Properties



### Auto Configuration



### Q: What do you understand by auto-configuration in Spring Boot and how to disable the  auto-configuration?

Auto-configuration is used to automatically configure the required configuration for the application. For example, if you have a data source bean present in the classpath of the application, then it automatically configures the JDBC template. With the help of auto-configuration, you can create a Java application in an easy way, as it automatically configures the required beans, controllers, etc. 

To disable the auto-configuration property, you have to exclude attribute of @EnableAutoConfiguration, in the scenario where you do not want it to be applied.

```
@EnableAutoConfiguration(exclude={DataSourceAutoConfiguration.class})
```

If the class is not on the classpath, then to exclude the auto-configuration, you have to mention the following code:

```
@EnableAutoConfiguration(excludeName={Sample.class})
```

Apart from this, Spring Boot also provides the facility to exclude list of auto-configuration classes by using the `spring.autoconfigure.exclude` property. You can go forward, and add it either in the application.properties or add multiple classes with comma-separated.

### Q: Explain how to register a custom auto-configuration?

In order to register an auto-configuration class, you have to mention the fully-qualified name under the @EnableAutoConfiguration key META-INF/spring. factories file. Also, if we build the with maven, then this file should be placed in the resources/META-INT directory. 

### Q: How to instruct an auto-configuration to back off when a bean exists?

To instruct an auto-configuration class to back off when a bean exists, you have to use the @ConditionalOnMissingBean annotation. The attributes of this annotation are as follows:

- **value:** This attribute stores the type of beans to be checked
- **name:** This attribute stores the name of beans to be checked



### Spring Beans and Dependency Injection



### Q: What is the difference between RequestMapping and GetMapping?

The @GetMapping is a composed annotation that acts as a shortcut for @RequestMapping(method = RequestMethod.GET). 

### Developer Tools

### Q: What is the need for Spring Boot DevTools?

Spring Boot Dev Tools are an elaborated set of tools and aims to make the process of developing an application easier. If the application runs in the production, then this module is automatically disabled, repackaging of archives are also excluded by default. So, the Spring Boot Developer Tools applies properties to the respective development environments. To include the DevTools, you just have to add the following dependency into the pom.xml file:

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
</dependency>
```



### Packaging Application for Production

### Q: What are the steps to deploy Spring Boot web applications as JAR and WAR files?

To deploy a Spring Boot web application, you just have to add the following plugin in the pom.xml file:

```
<plugin>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-maven-plugin</artifactId>
</plugin>
```

By using the above plugin, you will get a JAR executing the package phase. This JAR will contain all the necessary libraries and dependencies required. It will also contain an embedded server. So, you can basically run the application like an ordinary JAR file.
**Note:** The packaging element in the pom.xml file must be set to **jar** to build a JAR file as below:

```
<packaging>jar</packaging>
```

Similarly, if you want to build a WAR file, then you will mention

```
<packaging>war</packaging>
```

### Q: Mention the differences between WAR and embedded containers?

| WAR                                                  | Embedded Containers                                          |
| ---------------------------------------------------- | ------------------------------------------------------------ |
| WAR benefits a considerable measure from Spring Boot | Only one component of Spring Boot and is utilized during improvements |

## Spring Boot Features

### SpringApplication, Externalized Configuration, Profiles, Logging

### Q: Can you explain what happens in the background when a Spring Boot Application is “Run as Java Application”?

When a Spring Boot application is executed as “Run as Java application”, then it automatically launches up the tomcat server as soon as it sees, that you are developing a web application.

### Q: Mention the possible sources of external configuration?

There is no doubt in the fact that Spring Boot allows the developers to run the same application in different environments. Well, this is done with the support it provides for external configuration. It uses environment variables, properties files, command-line arguments, YAML files, and system properties to mention the required configuration properties. Also, the @value annotation is used to gain access to the properties. So, the most possible sources of external configuration are as follows:

- **Application Properties –** By default, Spring Boot searches for the application properties file or its YAML file in the current directory, classpath root or config directory to load the properties.
- **Command-line properties –** Spring Boot provides command-line arguments and converts these arguments to properties. Then it adds them to the set of environment properties.
- **Profile-specific properties –** These properties are loaded from the application-{profile}.properties file or its YAML file. This file resides in the same location as that of the non-specific property files and the{profile} placeholder refers to an active profile.

### Q: What do you think is the need for Profiles?

Profiles are used to provide a way to segregate the different parts of the application configuration and make it available for various environments. So, basically, any @Component or a @Configuration can be marked with a @Profile to limit as it is loaded. Consider you have multiple environments,

- Dev
- QA
- Stage
- Production

Now, let’s say, you want to have different application configuration in each of the environments, you can use profiles to have different application configurations for different environments. So, basically, Spring and Spring Boot provide features through which you can specify:

- The active profile for a specific environment
- The configuration of various environments for various profiles.

### Q: How do you Configure Log4j for logging?

Since Spring Boot supports Log4j2 for logging a configuration, you have to exclude Logback and include Log4j2 for logging. This can be only done if you are using the starters project.

### Q: What is the way to use profiles to configure the environment-specific configuration with Spring Boot?

Once you are done with the profile-specific configuration, you have to set the active profile in an environment. To do that, either you can

- Use `-Dspring.profiles.active=prod` in arguments
- Use `spring.profiles.active=prod` in application.properties file

### Q: What do you understand by Spring Boot supports relaxed binding?

Relaxed binding, is a way in which, the property name does not need to match the key of the environment property. In Spring Boot, relaxed binding is applicable to the type-safe binding of the configuration properties. For example, if a property in a bean class with the @ConfigurationPropertie annotation is used sampleProp, then it can be bounded to any of the following environment properties:

- sampleProp
- sample-Prop
- sample_Prop
- SAMPLE_PROP

### Working with Databases, Caching

### Q: Mention the differences between JPA and Hibernate?

| **JPA**                                                      | **Hibernate**                                                |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| JPA is a Data Access Abstraction used to reduce the amount of boilerplate code | Hibernate is an implementation of Java Persistence API and offers benefits of loose coupling |

### Q: Mention the steps to connect Spring Boot application to a database using JDBC?

Once the project is created, you have to configure the database into application properties

```
spring.datasource.url=jdbc:mysql://localhost:3306/example
spring.datasource.username=root  
spring.datasource.password=edureka  
spring.jpa.hibernate.ddl-auto=create-drop 
```

The main application.java class should have the following code:

```java
@SpringBootApplication  
public class SampleApplication {  
    public static void main(String[] args) {  
        SpringApplication.run(SampleApplication.class, args);  
    }  
} 
```

Next, you have to create a controller to handle the HTTP requests, by mentioning the following code:

```java
@RestController
public class JdbcController {
    @Autowired
    JdbcTemplate jdbc;
    
    @RequestMapping("/insert")
    public String index(){
    	jdbc.execute("insert into customers(name)values('Aryya')");
    	return "Data Entry Successful";
    }
}
```

Finally, execute this project as a Java application.

Next, open the URL (localhost:8080/insert), and you will see the output as Data Entry Successful. You can also go forward and check if the data is entered into the table.

### Q: Explain Spring Data?

Spring Data aims to make it easy for the developers to use relational and non-relational databases, cloud-based data services, and other data access technologies. So, basically, it makes it easy for data access and still retains the underlying data.

### Q: How is Hibernate chosen as the default implementation for JPA without any configuration?

When we use the Spring Boot Auto Configuration, automatically the spring**-boot-starter-data-jpa** dependency gets added to the pom.xml file. Now, since this dependency has a transitive dependency on JPA and Hibernate, Spring Boot automatically auto-configures Hibernate as the default implementation for JPA, whenever it sees Hibernate in the classpath. 

### Q: What do you understand by Spring Data REST?

TODO

### Q: How does path=”sample”, collectionResourceRel=”sample” work with Spring Data Rest?

TODO

### Q: Why is Spring Data REST not recommended in real-world applications?

Spring Data REST is not recommended in real-world applications as you are exposing your database entities directly as REST Services. While designing RESTful services, the two most important things that we consider is the domain model and the consumers. But, while using Spring Data REST, none of these parameters are considered. The entities are directly exposed. So, I would just say, you can use Spring Data REST, for the initial evolution of the project.

### Q: Mention the dependencies needed to start up a JPA Application and connect to in-memory database H2 with Spring Boot?

The dependencies are needed to start up a JPA Application and connect to in-memory database H2 with Spring Boot

- web starter

- h2

- data JPA starter

- To include the dependencies refer to the following code:

  ```
  <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
  </dependency>
  <dependency>
      <groupId>com.h2database</groupId>
      <artifactId>h2</artifactId>
      <scope>runtime</scope>
  </dependency>
  <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-data-jpa</artifactId>
  </dependency>
  ```

  

### Q: Where is the database connection information specified and how does it automatically connect to H2?

Well, the answer to this question is very simple. It is because of the Spring Boot auto-configuration that, configures the dependencies of the application. So, the database connection information, and automatically connecting the database to H2 is done by the auto-configuration property.

### Q: What is the name of the default H2 database configured by Spring Boot?

The name of the default H2 database is **testdb. Refer below:**

```
spring.datasource.name=testdb # Name of the datasource.
```

**Note:** Just incase if you are using H2 in-memory database, then exactly that is the name of Spring Boot which is used to setup your H2 database.

### REST Services 

### Other Features

### Q: How to enable HTTP/2 support in Spring Boot?

You can enable the HTTP/2 support in Spring Boot by: `server.http2.enabled=true`

## Spring Boot Actuator

### Q: What is Spring Boot Actuator?

**Spring** Boot **Actuator** is a sub-project of the **Spring** Boot Framework. It includes a number of additional features that help us to monitor and manage the **Spring** Boot application. It contains the **actuator** endpoints (the place where the resources live). We can use **HTTP** and **JMX** endpoints to manage and monitor the Spring Boot application. If we want to get production-ready features in an application, we should use the **Spring Boot actuator**.

There are **three** main features of Spring Boot Actuator:

- **Endpoints**
- **Metrics**
- **Audit**

**Endpoint:** The actuator endpoints allows us to monitor and interact with the application. Spring Boot provides a number of built-in endpoints. We can also create our own endpoint. We can enable and disable each endpoint individually. Most of the application choose **HTTP**, where the Id of the endpoint, along with the prefix of **/actuator,** is mapped to a URL.

For example, the **/health** endpoint provides the basic health information of an application. The actuator, by default, mapped it to **/actuator/health**.  

**Metrics:** Spring Boot Actuator provides dimensional metrics by integrating with the **micrometer**. The micrometer is integrated into Spring Boot. It is the instrumentation library powering the delivery of application metrics from Spring. It provides vendor-neutral interfaces for **timers, gauges, counters, distribution summaries,** and **long task timers** with a dimensional data model.

**Audit:** Spring Boot provides a flexible audit framework that publishes events to an **AuditEventRepository.** It automatically publishes the authentication events if spring-security is in execution.

### Q: Explain Spring Actuator and its advantages?

Spring Actuator is a cool feature of Spring Boot with the help of which you can see what is happening inside a running application. So, whenever you want to debug your application, and need to analyze the logs you need to understand what is happening in the application right? In such a scenario, the Spring Actuator provides easy access to features such as identifying beans, CPU usage, etc. The Spring Actuator provides a very easy way to access the production-ready REST points and fetch all kinds of information from the web. These points are secured using Spring Security’s content negotiation strategy.

### Q: How can we create a custom endpoint in Spring Boot Actuator?

To create a custom endpoint in Spring Boot 2.x, you can use the @Endpoint annotation. Spring Boot also exposes endpoints using @WebEndpointor, @WebEndpointExtension over HTTP with the help of Spring MVC, Jersey, etc.

## Deploying Spring Boot Applications

## Spring Boot CLI

### Q: What is Spring Boot CLI and how to execute the Spring Boot project using boot CLI?

Spring Boot CLI is a tool supported by the official Spring Framework. The steps to execute a Spring Boot project are as follows:

- Download the CLI tool from the official site and extract the zip file. The bin folder present in the Spring setup is used to execute the Spring Boot application.

- Since Spring Boot CLI executes groovy files, you need to create a groovy file for Spring Boot application. So, to do that, open terminal and change the current directory to the bin folder. Now, open a groovy file (for example Sample.groovy)

- In this file create a controller as follows:

  ```
  @RestController   public class Sample {   
   @RequestMapping("/example")   
   String index(){   
  <h1>"Welcome"</h1>;  
  }   }
  ```

- Then execute the groovy file by mentioning:

  ```
  ./spring run Sample.groovy;
  ```

- Once, the project is executed go to the URL(localhost:8080:/example) and you will see the output as

  ```
  Welcome
  ```

  

## Build Tool Plugins

## References

- [Top 50 Spring Boot Interview Questions That Are A Must](https://www.edureka.co/blog/interview-questions/spring-boot-interview-questions/)
- [Pros and Cons of Using Spring Boot](https://scand.com/company/blog/pros-and-cons-of-using-spring-boot)
- [Spring Boot Interview Questions - Javatpoint](https://www.javatpoint.com/spring-boot-interview-questions)

