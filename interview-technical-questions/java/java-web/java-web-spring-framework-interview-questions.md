# Spring Framework Interview Questions

### Content

- [Introduction](#Introduction)
  - [x] [Q: What is Spring Framework?](#Q: What is Spring Framework?)
  - [x] [Q: What are the Benefits of Using Spring?](#Q: What are the Benefits of Using Spring?)
  - [x] [Q: What Spring Sub-Projects Do You Know?Describe Them Briefly.](#Q: What Spring Sub-Projects Do You Know?Describe Them Briefly.)
- [Core Technologies](#Core Technologies)
  - [IoC Container](#IoC Container)
    - [x] [Q: What are Dependency Injection (DI) and Inversion of Control (IoC)?](#Q: What are Dependency Injection (DI) and Inversion of Control (IoC)?)
    - [x] [Q: How Can We Inject Beans in Spring?](#Q: How Can We Inject Beans in Spring?)
    - [x] [Q: Which is the Best Way of Injecting Beans and Why?](#Q: Which is the Best Way of Injecting Beans and Why?)
    - [x] [Q: What is the Difference between BeanFactory and ApplicationContext?](#Q: What is the Difference between BeanFactory and ApplicationContext?)
    - [x] [Q: What is a Spring Bean?](#Q: What is a Spring Bean?)
    - [x] [Q: What is Default Bean Scope in Spring Framework?](#Q: What is Default Bean Scope in Spring Framework?)
    - [x] [Q: How to Define the Scope of a Bean?](#Q: How to Define the Scope of a Bean?)
    - [x] [Q: Are Singleton Beans Thread-Safe?](#Q: Are Singleton Beans Thread-Safe?)
    - [x] [Q: What Does the Spring Bean Lifecycle Look Like?](#Q: What Does the Spring Bean Lifecycle Look Like?)
    - [x] [Q: What is the Spring Java-Based Configuration?](#Q: What is the Spring Java-Based Configuration?)
    - [x] [Q: Can We Have Multiple Spring Configuration Files in One Project?](#Q: Can We Have Multiple Spring Configuration Files in One Project?)
    - [x] [Q: How Does the Scope Prototype Work?](#Q: How Does the Scope Prototype Work?)
  - Resources
  - Validation, Data Binding, and Type Conversion
  - Spring Expression Language (SpEL)
  - [Aspect Oriented Programing (AOP) with Spring](#Aspect Oriented Programing (AOP) with Spring)
    - [x] [Q: What is Aspect-Oriented Programming?](#Q: What is Aspect-Oriented Programming?)
    - [x] [Q: What are Aspect, Advice, Pointcut, and JoinPoint in APO?](#Q: What are Aspect, Advice, Pointcut, and JoinPoint in APO?)
    - [ ] Q: What is Weaving?
- [Testing](#Testing)
- [Data Access](#Data Access)
  - Transaction Management
    - [x] [Q: How would you Enable Transactions in Spring and What Are Their Benefits?](#Q: How would you Enable Transactions in Spring and What Are Their Benefits?)
  - DAO support
    - [x] [Q: What is Spring Dao?](#Q: What is Spring Dao?)
  - Data Access with JDBC
    - [x] [Q: What is Spring JdbcTemplate Class and How to Use It?](#Q: What is Spring JdbcTemplate Class and How to Use It?)
  - ORM Data Access
  - Marshalling XML
- [The Web](#The Web)
  - [Web MVC framework](#Web MVC framework)
    - [ ] [Q: Why Should We Use Spring MVC?](#Q: Why Should We Use Spring MVC?)
    - [x] [Q: How to Get ServletContext and ServletConfig Objects in a Spring Bean?](#Q: How to Get ServletContext and ServletConfig Objects in a Spring Bean?)
    - [x] [Q: What is a Controller in Spring MVC?](#Q: What is a Controller in Spring MVC?)
    - [x] [Q: How Does the @RequestMapping Annotation Work?](#Q: How Does the @RequestMapping Annotation Work?)
    - [x] [Q: Explain a Model Attribute?](#Q: Explain a Model Attribute?)
    - [x] [Q: Explain the Difference Between @Controller and @RestController?](#Q: Explain the Difference Between @Controller and @RestController?)
    - [x] [Q: Validation Using Spring MVC?](#Q: Validation Using Spring MVC?)
    - [x] [Q: What are the @RequestBody and the @ResponseBody?](#Q: What are the @RequestBody and the @ResponseBody?)
    - [x] [Q: @ModelAttribute vs @RequestBody in Spring Data Binding?](#Q: @ModelAttribute vs @RequestBody in Spring Data Binding?)
    - [x] [Q: Explain Model, ModelMap and ModelAndView?](#Q: Explain Model, ModelMap and ModelAndView?)
    - [x] [Q: Explain SessionAttributes and SessionAttribute?](#Q: Explain SessionAttributes and SessionAttribute?)
    - [x] [Q: What is the Purpose of @EnableWebMVC?](#Q: What is the Purpose of @EnableWebMVC?)
    - [x] [Q: What Is ViewResolver in Spring?](#Q: What Is ViewResolver in Spring?)
    - [x] [Q: What is the BindingResult?](#Q: What is the BindingResult?)
    - [x] [Q: What Is the Role of the @Qualifier Annotation?](#Q: What Is the Role of the @Qualifier Annotation?)
    - [x] [Q: What Is the Role of the @Required Annotation?](#Q: What Is the Role of the @Required Annotation?)
  - View technologies
  - CORS Support
  - Integrating With Other Web Framework
  - WebSocKet Support
  - [Web Reactive Framework](#Web Reactive Framework)
    - [x] Q: What is Reactive Programming?
    - [x] Q: What is Spring Webflux?
- [Integration](#Integration)
- [Others](#Others)
  - [x] [Q: Name Some of the Design Patterns Used in the Spring Framework?](#Q: Name Some of the Design Patterns Used in the Spring Framework?)
  - [x] [Q: What is Spring Boot?](#Q: What is Spring Boot?)
  - [x] [Q: What is Spring Security?](#Q: What is Spring Security?)
- [References](#References)



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

**Setter Injection**

For setter-based DI, the container will call setter methods of our class, after invoking a no-argument constructor or no-argument static factory method to instantiate the bean. Let's create this configuration using annotations:

```java
@Bean
public Store store() {
    Store store = new Store();
    store.setItem(item1());
    return store;
}
```

We can also use XML for the same configuration of beans:

```xml
<bean id="store" class="org.baeldung.store.Store">
    <property name="item" ref="item1" />
</bean>
```

Constructor-based and setter-based types of injection can be combined for the same bean. The Spring documentation recommends using constructor-based injection for mandatory dependencies, and setter-based injection for optional ones.

**Constructor Injection**

In the case of constructor-based dependency injection, the container will invoke a constructor with arguments each representing a dependency we want to set.

```java
@Configuration
public class AppConfig {
    @Bean
    public Store store() {
        return new Store(item1());
    }
}
```

Another way to create the configuration of the beans is through XML configuration:

```xml
<bean id="store" class="org.baeldung.store.Store"> 
    <constructor-arg type="ItemImpl1" index="0" name="item" ref="item1" /> 
</bean>
```


**Field Injection**

In case of Field-Based DI, we can inject the dependencies by marking them with an *@Autowired* annotation:

```java
public class Store {
    @Autowired
    private Item item; 
}
```

While constructing the *Store* object, if there's no constructor or setter method to inject the *Item* bean, the container will use reflection to inject *Item* into *Store*.

The configuration can be done using XML files or annotations.

```xml
<bean 
  id="indexService" 
  class="com.baeldung.di.spring.IndexService" />
     
<bean 
  id="indexApp" 
  class="com.baeldung.di.spring.IndexApp" >
    <property name="service" ref="indexService" />
</bean> 
```

This approach might look simpler and cleaner but is not recommended to use because it has a few drawbacks such as:

- This method uses reflection to inject the dependencies, which is costlier than constructor-based or setter-based injection
- It's really easy to keep adding multiple dependencies using this approach. If you were using constructor injection having multiple arguments would have made us think that the class does more than one thing which can violate the Single Responsibility Principle.

### Q: Which is the Best Way of Injecting Beans and Why?

The recommended approach is to use constructor arguments for mandatory dependencies and setters for optional ones. Constructor injection allows injecting values to immutable fields and makes testing easier.

### Q: What is the Difference between BeanFactory and ApplicationContext?

*BeanFactory* is an interface representing a container that provides and manages bean instances. The default implementation instantiates beans lazily when *getBean()* is called.

*ApplicationContext* is an interface representing a container holding all information, metadata, and beans in the application. It also extends the *BeanFactory* interface but the default implementation instantiates beans eagerly when the application starts. This behavior can be overridden for individual beans.

In short, the `BeanFactory` provides the configuration framework and basic functionality, and the `ApplicationContext` adds more enterprise-specific functionality. The `ApplicationContext` is a complete superset of the `BeanFactory`.

### Q: What is a Spring Bean?

The Spring Beans are Java Objects that are initialized by the Spring IoC container.

> In Spring, the objects that form the backbone of your application and that are managed by the Spring IoC container are called beans. A bean is an object that is instantiated, assembled, and otherwise managed by a Spring IoC container. Otherwise, a bean is simply one of many objects in your application. Beans, and the dependencies among them, are reflected in the configuration metadata used by a container.
>
> -- [1]<cite>[Introduction to the Spring IoC container and beans][1]</cite>

### Q: What is Default Bean Scope in Spring Framework?

By default, a Spring Bean is initialized as a *singleton*.

### Q: How to Define the Scope of a Bean?

To set Spring Bean's scope:

- Use *@Scope* annotation
- Set “scope” attribute in XML configuration files. 

There are five supported scopes:

- **singleton**
- **prototype**
- **request**
- **session**
- **global-session**

| Scope                                                        | Description                                                  |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [singleton](https://docs.spring.io/spring/docs/current/spring-framework-reference/core.html#beans-factory-scopes-singleton) | (Default) Scopes a single bean definition to a single object instance for each Spring IoC container. |
| [prototype](https://docs.spring.io/spring/docs/current/spring-framework-reference/core.html#beans-factory-scopes-prototype) | Scopes a single bean definition to any number of object instances. |
| [request](https://docs.spring.io/spring/docs/current/spring-framework-reference/core.html#beans-factory-scopes-request) | Scopes a single bean definition to the lifecycle of a single HTTP request. That is, each HTTP request has its own instance of a bean created off the back of a single bean definition. Only valid in the context of a web-aware Spring `ApplicationContext`. |
| [session](https://docs.spring.io/spring/docs/current/spring-framework-reference/core.html#beans-factory-scopes-session) | Scopes a single bean definition to the lifecycle of an HTTP `Session`. Only valid in the context of a web-aware Spring `ApplicationContext`. |
| [application](https://docs.spring.io/spring/docs/current/spring-framework-reference/core.html#beans-factory-scopes-application) | Scopes a single bean definition to the lifecycle of a `ServletContext`. Only valid in the context of a web-aware Spring `ApplicationContext`. |
| [websocket](https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html#websocket-stomp-websocket-scope) | Scopes a single bean definition to the lifecycle of a `WebSocket`. Only valid in the context of a web-aware Spring `ApplicationContext`. |

### Q: Are Singleton Beans Thread-Safe?

No, singleton beans are not thread-safe, as thread safety is about execution, whereas the singleton is a design pattern focusing on creation. Thread safety depends only on the bean implementation itself.

### Q: What Does the Spring Bean Lifecycle Look Like?

First, a Spring bean needs to be instantiated, based on Java or XML bean definition. It may also be required to perform some initialization to get it into a usable state. After that, when the bean is no longer required, it will be removed from the IoC container.

The whole cycle with all initialization methods is shown on the image.

![](images/java-web-spring-bean-life-cycle.jpg)

### Q: What is the Spring Java-Based Configuration?

It's one of the ways of configuring Spring-based applications in a type-safe manner. It's an alternative to the XML-based configuration.

### Q: Can We Have Multiple Spring Configuration Files in One Project?

Yes, in large projects, having multiple Spring configurations is recommended to increase maintainability and modularity.

You can load multiple Java-based configuration files:

```java
@Configuration
@Import({MainConfig.class, SchedulerConfig.class})
public class AppConfig {
```

Or load one XML file that will contain all other configs:

```java
ApplicationContext context = new ClassPathXmlApplicationContext("spring-all.xml");
```

And inside this XML file you'll have:

```xml
<import resource="main.xml"/>
<import resource="scheduler.xml"/>
```

### Q: How Does the Scope Prototype Work?

Scope *prototype* means that every time you call for an instance of the Bean, Spring will create a new instance and return it. This differs from the default *singleton* scope, where a single object instance is instantiated once per Spring IoC container.

### Resources

### Validation, Data Binding, and Type Conversion

### Spring Expression Language (SpEL)

### Aspect Oriented Programing (AOP) with Spring

### Q: What is Aspect-Oriented Programming?

1

*Aspects* enable the modularization of cross-cutting concerns such as transaction management that span multiple types and objects by adding extra behavior to already existing code without modifying affected classes.

2

Aspect-Oriented Programming (AOP) complements Object-Oriented Programming (OOP) by providing another way of thinking about program structure. The key unit of modularity in OOP is the class, whereas in AOP the unit of modularity is the aspect. Aspects enable the modularization of concerns such as transaction management that cut across multiple types and objects.

One of the key components of Spring is the AOP framework. While the Spring IoC container does not depend on AOP, the AOP complements Spring IoC to provide a very capable middleware solution.

### Q: What are Aspect, Advice, Pointcut, and JoinPoint in APO?

- ***Aspect***: a class that implements cross-cutting concerns, such as transaction management
- ***Advice\***: the methods that get executed when a specific *JoinPoint* with matching *Pointcut* is reached in the application
- ***Pointcut***: a set of regular expressions that are matched with *JoinPoint* to determine whether *Advice* needs to be executed or not
- ***JoinPoint***: a point during the execution of a program, such as the execution of a method or the handling of an exception

### Q: What is Weaving?



### Spring AOP APIs

## Testing

## Data Access

### Transaction Management

### Q: How would you Enable Transactions in Spring and What Are Their Benefits?

There are two distinct ways to configure *Transactions* – with annotations or by using Aspect Oriented Programming (AOP) – each with their advantages.

The benefits of using Spring Transactions, according to the [official docs](https://docs.spring.io/spring/docs/current/spring-framework-reference/html/transaction.html), are:

- Provide a consistent programming model across different transaction APIs such as JTA, JDBC, Hibernate, JPA, and JDO
- Support declarative transaction management
- Provide a simpler API for programmatic transaction management than some complex transaction APIs such as JTA
- Integrate very well with Spring's various data access abstractions

### DAO support

### Q: What is Spring Dao?

Spring Data Access Object is Spring's support provided to work with data access technologies like JDBC, Hibernate, and JPA in a consistent and easy way.

### Data Access with JDBC

### Q: What is Spring JdbcTemplate Class and How to Use It?

The Spring JDBC template is the primary API through which we can access database operations logic that we’re interested in:

- creation and closing of connections
- executing statements and stored procedure calls
- iterating over the *ResultSet* and returning results

To use it, we'll need to define the simple configuration of *DataSource*:

```java
@Configuration
@ComponentScan("org.baeldung.jdbc")
public class SpringJdbcConfig {
    @Bean
    public DataSource mysqlDataSource() {
        DriverManagerDataSource dataSource = new DriverManagerDataSource();
        dataSource.setDriverClassName("com.mysql.jdbc.Driver");
        dataSource.setUrl("jdbc:mysql://localhost:3306/springjdbc");
        dataSource.setUsername("guest_user");
        dataSource.setPassword("guest_password");
 
        return dataSource;
    }
}
```

### **Basic Queries**

```java
int result = jdbcTemplate.queryForObject(
    "SELECT COUNT(*) FROM EMPLOYEE", Integer.class);
```

```java
public int addEmplyee(int id) {
    return jdbcTemplate.update(
      "INSERT INTO EMPLOYEE VALUES (?, ?, ?, ?)", id, "Bill", "Gates", "USA");
}
```

### **Queries With Named Parameters**

```java
public int addEmplyee(int id) {
    return jdbcTemplate.update(
      "INSERT INTO EMPLOYEE VALUES (?, ?, ?, ?)", id, "Bill", "Gates", "USA");
}
```

### **Mapping Query Results to Java Object**

```java
public class EmployeeRowMapper implements RowMapper<Employee> {
    @Override
    public Employee mapRow(ResultSet rs, int rowNum) throws SQLException {
        Employee employee = new Employee();
 
        employee.setId(rs.getInt("ID"));
        employee.setFirstName(rs.getString("FIRST_NAME"));
        employee.setLastName(rs.getString("LAST_NAME"));
        employee.setAddress(rs.getString("ADDRESS"));
 
        return employee;
    }
}
```

```java
String query = "SELECT * FROM EMPLOYEE WHERE ID = ?";
List<Employee> employees = jdbcTemplate.queryForObject(
  query, new Object[] { id }, new EmployeeRowMapper());
```

**JDBC Operations Using SimpleJdbc Classes**

```java
SimpleJdbcInsert simpleJdbcInsert = 
  new SimpleJdbcInsert(dataSource).withTableName("EMPLOYEE");
```

```java
public int addEmplyee(Employee emp) {
    Map<String, Object> parameters = new HashMap<String, Object>();
    parameters.put("ID", emp.getId());
    parameters.put("FIRST_NAME", emp.getFirstName());
    parameters.put("LAST_NAME", emp.getLastName());
    parameters.put("ADDRESS", emp.getAddress());
    return simpleJdbcInsert.execute(parameters);
}
```



### ORM Data Access

### Marshalling XML

## The Web

### Web MVC framework

### Q: Why Should We Use Spring MVC?

**Spring MVC implements a clear separation of concerns that allows us to develop and unit test our applications easily**.

The concepts like:

- Dispatcher Servlet
- Controllers
- View Resolvers
- Views, Models
- *ModelAndView*
- Model and Session Attributes

are completely independent of each other, and they are responsible for one thing only.

Therefore, **MVC gives us quite big flexibility**. It's based on interfaces (with provided implementation classes), and we can configure every part of the framework by using custom interfaces.

**Another important thing is that we aren't tied to a specific view technology (for example, JSP), but we have the option to choose from the ones we like the most**.

Also, **we don't use Spring MVC only in web applications development but in the creation of RESTful web services as well**.

### Q: How to Get ServletContext and ServletConfig Objects in a Spring Bean?

You can do either by:

1. Implementing Spring-aware interfaces. The complete list is available [here](http://www.buggybread.com/2015/03/spring-framework-list-of-aware.html).

More aware interfaces reference <cite>[Aware interfaces][2]</cite>. 

A example of  `ServletContextAware`:

```java
public class ServletContextAwareBean implements ServletContextAware {

	private ServletContext servletContext;

	public void setServletContext(ServletContext servletContext) {
		this.servletContext = servletContext;
	}

	public ServletContext getServletContext() {
		return servletContext;
	}
}
```

2. Using *@Autowired* annotation on those beans:

```java
@Autowired
ServletContext servletContext;
 
@Autowired
ServletConfig servletConfig;
```





### Q: What is a Controller in Spring MVC?

Simply put, all the requests processed by the *DispatcherServlet* are directed to classes annotated with *@Controller*. Each controller class maps one or more requests to methods that process and execute the requests with provided inputs.



### Q: How Does the @RequestMapping Annotation Work?

The *@RequestMapping* annotation is used to map web requests to Spring Controller methods. In addition to simple use cases, we can use it for mapping of HTTP headers, binding parts of the URI with *@PathVariable,* and working with URI parameters and the *@RequestParam* annotation.

### Q: Explain a Model Attribute?

One of the most important Spring-MVC annotations is the @ModelAttribute annotation.

The @ModelAttribute is an annotation that binds a method parameter or method return value to a named model attribute and then exposes it to a web view.

As the introductory paragraph revealed, @ModelAttribute can be used

- At the method level
- As a method parameter

**At the Method Level**

If we use it at the method level, it indicates the purpose of that method is to add one or more model attributes.

```java
@ModelAttribute
public void addAttributes(Model model) {
    model.addAttribute("msg", "Welcome to the Netherlands!");
}
```

In the example, we show a method that adds an attribute named msg to all models defined in the controller class.

In general, Spring-MVC will always make a call first to that method, before it calls any request handler methods. That is, @ModelAttribute methods are invoked before the controller methods annotated with @RequestMapping are invoked. The logic behind the sequence is that, the model object has to be created before any processing starts inside the controller methods.

It is also important that you annotate the respective class as @ControllerAdvice. Thus, you can add values in Model which will be identified as global. This actually means that for every request a default value exists, for every method in the response part.

**As a Method Argument**

When used as a method argument, it indicates the argument should be retrieved from the model. When not present, it should be first instantiated and then added to the model and once present in the model, the arguments fields should be populated from all request parameters that have matching names.

View

```html
<form:form method="POST" action="/spring-mvc-basics/addEmployee" 
  modelAttribute="employee">
    <form:label path="name">Name</form:label>
    <form:input path="name" />
    <form:label path="id">Id</form:label>
    <form:input path="id" />
    <input type="submit" value="Submit" />
</form:form>
```

Controller

```java
@RequestMapping(value = "/addEmployee", method = RequestMethod.POST)
public String submit(@ModelAttribute("employee") Employee employee) {
    // Code that uses the employee object

    return "employeeView";
}
```

### Q: Explain the Difference Between @Controller and @RestController?

The main difference between the *@Controller* and *@RestController* annotations is that **the \*@ResponseBody\* annotation is automatically included in the \*@RestController\***. This means that we don't need to annotate our handler methods with the *@ResponseBody*. We need to do this in a *@Controller* class if we want to write response type directly to the HTTP response body.

### Q: Validation Using Spring MVC?

**Spring MVC supports JSR-303 specifications by default. We need to add JSR-303 and its implementation dependencies to our Spring MVC application**. Hibernate Validator, for example, is one of the JSR-303 implementations at our disposal.

JSR-303 is a specification of the Java API for bean validation, part of Jakarta EE and JavaSE, which ensures that properties of a bean meet specific criteria, using annotations such as *@NotNull*, *@Min*, and *@Max*. More about validation is available in the [Java Bean Validation Basics](https://www.baeldung.com/javax-validation) article.

**Spring offers the \*@Validator\* annotation and the \*BindingResult\* class**. The *Validator* implementation will raise errors in the controller request handler method when we have invalid data. Then we may use the *BindingResult* class to get those errors.

Besides using the existing implementations, we can make our own. To do so, we create an annotation that conforms to the JSR-303 specifications first. Then, we implement the *Validator* class. Another way would be to implement Spring's *[Validator](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/validation/Validator.html)* interface and set it as the validator via *@InitBinder* annotation in *Controller* class.

To check out how to implement and use your own validations, please see the tutorial regarding [Custom Validation in Spring MVC](https://www.baeldung.com/spring-mvc-custom-validator).

### Q: What are the @RequestBody and the @ResponseBody?

The @RequestBody annotation, used as a handler method parameter, binds the HTTP Request body to a transfer or a domain object. Spring automatically deserializes incoming HTTP Request to the Java object using Http Message Converters.

```java
@PostMapping("/request")
public ResponseEntity postController(
  @RequestBody LoginForm loginForm) {
 
    exampleService.fakeAuthenticate(loginForm);
    return ResponseEntity.ok(HttpStatus.OK);
}
```

When we use the @ResponseBody annotation on a handler method in the Spring MVC controller, it indicates that we'll write the return type of the method directly to the HTTP response body. We'll not put it in a Model, and Spring won't interpret as a view name.

```java
@PostMapping("/response")
@ResponseBody
public ResponseTransfer postResponseController(
    @RequestBody LoginForm loginForm) {
    return new ResponseTransfer("Thanks For Posting!!!");
}
```

### Q: @ModelAttribute vs @RequestBody in Spring Data Binding?

1

`@ModelAttribute` is used for binding data from request param (in key value pairs).

`@RequestBody` is used for binding data from whole body of the request like POST,PUT.. request types which contains other format like json, xml.

2

I think @ModelAttribute and @RequestBody both are having same use, only difference is @ModelAttribute use for normal spring MVC and @RequestBody use for REST web service. It is @PathVariable and @PathParam. But in in both the cases we can mix it. we can use @PathVariable in REST and vice versa.

```java
@RequestMapping(value="/owners/{ownerId}/pets/{petId}/edit", method = RequestMethod.POST)
public String processSubmit(@ModelAttribute Pet pet) { }
```

```java
@RequestMapping(value = "/user/savecontact", method = RequestMethod.POST
public String saveContact(@RequestBody Contact contact){ }
```

3

The `@RequestBody` method parameter annotation indicates that a method parameter should be bound to the value of the HTTP request body. For example:

```java
@PutMapping("/something")
public void handle(@RequestBody String body, Writer writer) throws IOException {
    writer.write(body);
}
```

### Q: Explain *Model*, ModelMap and ModelAndView?

The Model interface defines a holder for model attributes. The ModelMap has a similar purpose, with the ability to pass a collection of values. It then treats those values as if they were within a Map. We should note that in Model (ModelMap) we can only store data. We put data in and return a view name.

On the other hand, with the ModelAndView, we return the object itself. We set all the required information, like the data and the view name, in the object we're returning.

Model

```java
@GetMapping("/showViewPage")
public String passParametersWithModel(Model model) {
    Map<String, String> map = new HashMap<>();
    map.put("spring", "mvc");
    model.addAttribute("message", "Baeldung");
    model.mergeAttributes(map);
    return "viewPage";
}
```

ModelMap

```java
@GetMapping("/printViewPage")
public String passParametersWithModelMap(ModelMap map) {
    map.addAttribute("welcomeMessage", "welcome");
    map.addAttribute("message", "Baeldung");
    return "viewPage";
}
```

ModelAndView

```java
@GetMapping("/goToViewPage")
public ModelAndView passParametersWithModelAndView() {
    ModelAndView modelAndView = new ModelAndView("viewPage");
    modelAndView.addObject("message", "Baeldung");
    return modelAndView;
}
```



### Q: Explain SessionAttributes and SessionAttribute?

**@SessionAttributes**

The @SessionAttributes annotation is used for storing the model attribute in the user’s session.
We use it at the controller class level, as shown in below:

```java
@Controller
@RequestMapping("/sessionattributes")
@SessionAttributes("todos")
public class TodoControllerWithSessionAttributes {
 
    @GetMapping("/form")
    public String showForm(Model model,
      @ModelAttribute("todos") TodoList todos) {
        // method body
        return "sessionattributesform";
    }
}
```

the model attribute ‘todos‘ will be added to the session if the @ModelAttribute and the @SessionAttributes have the same name attribute.

**@SessionAttribute**

@SessionAttribute annotation is used for retrieve the existing attribute from a session that is managed globally.

```java
@GetMapping
public String getTodos(@SessionAttribute("todos") TodoList todos) {
    // method body
    return "todoView";
}
```

### Q: What is the Purpose of @EnableWebMVC?

The @EnableWebMvc annotation's purpose is to enable Spring MVC via Java configuration. It's equivalent to <mvc: annotation-driven> in an XML configuration. This annotation imports Spring MVC Configuration from WebMvcConfigurationSupport. It enables support for @Controller-annotated classes that use @RequestMapping to map incoming requests to a handler method.


### Q: What Is ViewResolver in Spring?

The ViewResolver enables an application to render models in the browser – without tying the implementation to a specific view technology – by mapping view names to actual views.

### Q: What is the *BindingResult*?

BindingResult is an interface from org.springframework.validation package that represents binding results. We can use it to detect and report errors in the submitted form. It's easy to invoke — we just need to ensure that we put it as a parameter right after the form object we're validating. The optional Model parameter should come after the BindingResult

```java
@PostMapping("/user")
public String submitForm(@Valid NewUserForm newUserForm, 
  BindingResult result, Model model) {
    if (result.hasErrors()) {
        return "userHome";
    }
    model.addAttribute("message", "Valid form");
    return "userHome";
}
```

When Spring sees the @Valid annotation, it'll first try to find the validator for the object being validated. Then it'll pick up the validation annotations and invoke the validator. Finally, it'll put found errors in the BindingResult and add the latter to the view model.

### Q: What Is the Role of the @Qualifier Annotation?

**It is used simultaneously with the \*@Autowired\* annotation to avoid confusion when multiple instances of a bean type are present**.

Let's see an example. We declared two similar beans in XML config:

```xml
<bean id="person1" class="com.baeldung.Person" >
    <property name="name" value="Joe" />
</bean>
<bean id="person2" class="com.baeldung.Person" >
    <property name="name" value="Doe" />
</bean>
```

When we try to wire the bean, we'll get an *org.springframework.beans.factory.NoSuchBeanDefinitionException.* To fix it, we need to use *@Qualifier* to tell Spring about which bean should be wired:

```java
@Autowired
@Qualifier("person1")
private Person person;
```

### Q: What Is the Role of the @Required Annotation?

**The \*@Required\* annotation is used on setter methods, and it indicates that the bean property that has this annotation must be populated at configuration time. Otherwise, the Spring container will throw a \*BeanInitializationException\* exception.**

Also, *@Required* differs from *@Autowired* – as it is limited to a setter, whereas *@Autowired* is not. *@Autowired* can be used to wire with a constructor and a field as well, while *@Required* only checks if the property is set.

```java
public class Person {
    private String name;
 
    @Required
    public void setName(String name) {
        this.name = name;
    }
}
```

### View technologies

### CORS Support

### Integrating With Other Web Framework

### WebSocKet Support

### Web Reactive Framework

### Q: What is Reactive Programming?

Reactive programming is about non-blocking, event-driven applications that scale with a small number of threads, with back pressure being a key ingredient that aims to ensure producers don't overwhelm consumers.

The primary benefits of reactive programming are:

- increased utilization of computing resources on multicore and multi-CPU hardware
- and increased performance by reducing serialization

Reactive programming is generally event-driven, in contrast to reactive systems, which are message-driven. Thus, using reactive programming does not mean we're building a reactive system, which is an architectural style.

However, reactive programming may be used as a means to implement reactive systems if we follow the [Reactive Manifesto](https://www.reactivemanifesto.org/), which is quite vital to understand.

Based on this, reactive systems have four important characteristics:

- **Responsive**: the system should respond in a timely manner
- **Resilient**: in case the system faces any failure, it should stay responsive
- **Elastic**: reactive systems can react to changes and stay responsive under varying workload
- **Message-driven**: reactive systems need to establish a boundary between components by relying on asynchronous message passing

### Q: What is Spring Webflux?

[Spring WebFlux](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html#webflux) is Spring's reactive-stack web framework, and it's an alternative to Spring MVC.

In order to achieve this reactive model and be highly scalable, the entire stack is non-blocking. Check out our [tutorial on Spring 5 WebFlux](https://www.baeldung.com/spring-webflux) for additional details.

## Integration

## Others

### Q: Name Some of the Design Patterns Used in the Spring Framework?

- **Singleton Pattern:** Singleton-scoped beans
- **Factory Pattern:** Bean Factory classes
- **Prototype Pattern:** Prototype-scoped beans
- **Adapter Pattern:** Spring Web and Spring MVC
- **Proxy Pattern:** Spring Aspect Oriented Programming support
- **Template Method Pattern:** *JdbcTemplate*, *HibernateTemplate,* etc.
- **Front Controller:** Spring MVC *DispatcherServlet*
- **Data Access Object:** Spring DAO support
- **Model View Controller:** Spring MVC

### Q: What is Spring Boot?

Spring Boot is a project that provides a pre-configured set of frameworks to reduce boilerplate configuration so that you can have a Spring application up and running with the smallest amount of code.

### Q: What is Spring Security?

Spring Security is a separate module of the Spring framework that focuses on providing authentication and authorization methods in Java applications. It also takes care of most of the common security vulnerabilities such as CSRF attacks.

To use Spring Security in web applications, you can get started with a simple annotation: *@EnableWebSecurity*.

## References

[1]: https://docs.spring.io/autorepo/docs/spring-framework/5.0.0.M1/spring-framework-reference/htmlsingle/#beans-introduction "3.1 Introduction to the Spring IoC container and beans - Spring Framework Reference 5.0.0"
[2]: https://docs.spring.io/autorepo/docs/spring-framework/5.0.0.M1/spring-framework-reference/htmlsingle/#aware-list "3.6.3 Other Aware interfaces - Spring Framework Reference 5.0.0"

- [Top Spring Framework Interview Questions](https://www.baeldung.com/spring-interview-questions)
- [Spring MVC Interview Questions](https://www.baeldung.com/spring-mvc-interview-questions) 
- [Intro to Inversion of Control and Dependency Injection with Spring](https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring)

