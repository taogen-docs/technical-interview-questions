# Servlet and JSP Interview Questions

### Content

- [Java Servlet](#Java Servlet)
  - [Introduction to Servlet](#Introduction to Servlet)
    - [x] [Q: What is Servlet?](#Q: What is Servlet?)
    - [x] [Q: What is different between web server and application server?](#Q: What is different between web server and application server?)
    - [x] [Q: Which HTTP method is non-idempotent?](#Q: Which HTTP method is non-idempotent?)
    - [x] [Q: What is MIME Type?](#Q: What is MIME Type?)
    - [x] [Q: What are the advantages of Servlet over CGI?](#Q: What are the advantages of Servlet over CGI?)
    - [x] [Q: What are common tasks performed by Servlet Container?](#Q: What are common tasks performed by Servlet Container?)
    - [x] [Q: What are important features of Servlet 3?](#Q: What are important features of Servlet 3?)
  - [The Servlet Interface](#The Servlet Interface)
    - [x] [Q: How many objects of a servlet is created?](#Q: How many objects of a servlet is created?)
    - [x] [Q: What is the life-cycle of a servlet?](#Q: What is the life-cycle of a servlet?)
    - [x] [Q: What are the life-cycle methods for a servlet?](#Q: What are the life-cycle methods for a servlet?)
    - [x] [Q: Who is responsible to create the object of servlet?](#Q: Who is responsible to create the object of servlet?)
    - [x] [Q: When servlet object is created?](#Q: When servlet object is created?)
    - [x] [Q: What is difference between GenericServlet and HttpServlet?](#Q: What is difference between GenericServlet and HttpServlet?)
    - [x] [Q: What is load-on-startup in servlet?](#Q: What is load-on-startup in servlet?)
    - [x] [Q: What if we pass negative value in load-on-startup?](#Q: What if we pass negative value in load-on-startup?)
    - [x] [Q: What is servlet attributes and their scope?](#Q: What is servlet attributes and their scope?)
    - [x] [Q: What is ServletConfig object?](#Q: What is ServletConfig object?)
    - [x] [Q: How can we create deadlock situation in servlet?](#Q: How can we create deadlock situation in servlet?)
    - [x] [Q: What is SingleThreadModel interface?](#Q: What is SingleThreadModel interface?)
    - [x] [Q: Do we need to override service() method?](#Q: Do we need to override service() method?)
    - [x] [Q: Is it good idea to create servlet constructor?](#Q: Is it good idea to create servlet constructor?)
    - [x] [Q: Are Servlets Thread Safe? How to achieve thread-safety in servlets?](#Q: Are Servlets Thread Safe? How to achieve thread-safety in servlets?)
    - [x] [Q: Why HttpServlet class is declared abstract?](#Q: Why HttpServlet class is declared abstract?)
    - [x] [Q: why we should override only no-agrs init() method?](#Q: why we should override only no-agrs init() method?)
  - [The Request](#The Request)
    - [x] [Q: What is difference between Get and Post method?](#Q: What is difference between Get and Post method?)
    - [x] [Q: How can we upload the file to the server using servlet?](#Q: How can we upload the file to the server using servlet?)
    - [x] [Q: What is the use of servlet wrapper classes?](#Q: What is the use of servlet wrapper classes?)
  - [Servlet Context](#Servlet Context)
    - [x] [Q: What is ServletContext object?](#Q: What is ServletContext object?)
    - [x] [Q: What is difference between ServletConfig and ServletContext?](#Q: What is difference between ServletConfig and ServletContext?)
  - [The Response](#The Response)
    - [x] [Q: What is difference between PrintWriter and ServletOutputStream?](#Q: What is difference between PrintWriter and ServletOutputStream?)
    - [x] [Q: Can we get PrintWriter and ServletOutputStream both in a servlet?](#Q: Can we get PrintWriter and ServletOutputStream both in a servlet?)
    - [x] [Q: How can we invoke another servlet in a different application?](#Q: How can we invoke another servlet in a different application?)
  - [Filtering](#Filtering)
    - [x] [Q: What is filter?](#Q: What is filter?)
    - [x] [Q: Why do we have servlet filters?](#Q: Why do we have servlet filters?)
    - [x] [Q: What is the effective way to make sure all the servlets are accessible only when the user has a valid session?](#Q: What is the effective way to make sure all the servlets are accessible only when the user has a valid session?)
  - [Sessions](#Sessions)
    - [x] [Q: What is Session Tracking?](#Q: What is Session Tracking?)
    - [x] [Q: What are Cookies?](#Q: What are Cookies?)
    - [x] [Q: What is difference between Cookies and HttpSession?](#Q: What is difference between Cookies and HttpSession?)
    - [x] [Q: What is the disadvantage of cookies?](#Q: What is the disadvantage of cookies?)
    - [x] [Q: What are different methods of session management in servlets?](#Q: What are different methods of session management in servlets?)
    - [x] [Q: What is URL Rewriting?](#Q: What is URL Rewriting?)
    - [x] [Q: How does Cookies work in Servlets?](#Q: How does Cookies work in Servlets?)
    - [x] [Q: What is the difference between encodeRedirectUrl and encodeURL?](#Q: What is the difference between encodeRedirectUrl and encodeURL?)
  - [Dispatching Requests](#Dispatching Requests)
    - [x] [Q: What is servlet collaboration?](#Q: What is servlet collaboration?)
    - [x] [Q: What is the purpose of RequestDispatcher Interface?](#Q: What is the purpose of RequestDispatcher Interface?)
    - [x] [Q: How do we call a jsp or servlet from the servlet?](#Q: How do we call a jsp or servlet from the servlet?)
    - [x] [Q: Difference between forward() method and sendRedirect() method ?](#Q: Difference between forward() method and sendRedirect() method ?)
    - [x] [Q: How to handle exceptions thrown by application with another servlet?](#Q: How to handle exceptions thrown by application with another servlet?)
  - [Web Applications](#Web Applications)
    - [x] [Q: What is war file?](#Q: What is war file?)
    - [x] [Q: How to create war file?](#Q: How to create war file?)
    - [x] [Q: What is a web application and what is its directory structure?](#Q: What is a web application and what is its directory structure?)
  - [Application Lifecycle Events](#Application Lifecycle Events)
    - [x] [Q: How can we perform any action at the time of deploying the project?](#Q: How can we perform any action at the time of deploying the project?)
    - [x] [Q: How to notify an object in session when session is invalidated or timed-out?](#Q: How to notify an object in session when session is invalidated or timed-out?)
    - [x] [Q: Why do we have servlet listeners?](#Q: Why do we have servlet listeners?)
  - [Mapping Requests to Servlet](#Mapping Requests to Servlet)
  - [Security](#Security)
    - [x] [Q: What are different ways for servlet authentication?](#Q: What are different ways for servlet authentication?)
    - [x] [Q: How can we achieve transport layer security for our web application?](#Q: How can we achieve transport layer security for our web application?)
  - [Deployment Descriptor](#Deployment Descriptor)
    - [x] [Q: What is a deployment descriptor?](#Q: What is a deployment descriptor?)
  - [Annotation and Pluggability](#Annotation and Pluggability)
    - [x] [Q: What are the annotations used in Servlet 3?](#Q: What are the annotations used in Servlet 3?)
  - Others
    - [x] [Q: What is URL Encoding?](#Q: What is URL Encoding?)
- [JSP](#JSP)
  - [Introduction to JSP](#Introduction to JSP)
    - [ ] TODO
  - [Expression Language (EL)](#Expression Language (EL))
    - [ ] TODO
  - [JSP Standard Tag Library (JSTL)](#JSP Standard Tag Library (JSTL))
    - [ ] TODO
  - [Tag Extensions](#Tag Extensions)
    - [ ] TODO
  - [Tag Files](#Tag Files)
    - [ ] TODO
- References

## I. Java Servlet

## Introduction to Servlet

### Q: What is Servlet?

> Java-based web component
>
> generating dynamic content

Servlet is Java-based Web component. It managed by servlet container. It's used for generating dynamic content response to client.

Servlet is platform-independent Java class, It can run in Web server that supported servlet container.

Servlet interacts with the Web client through the request/response paradigm implemented by the Servlet container.

### Q: What is different between web server and application server?

A **web server** responsibility is **to handler HTTP requests** from client browsers and **respond with HTML response**. A web server understands HTTP language and runs on HTTP protocol.
Apache Web Server is kind of a web server and then we have specific containers that can execute servlets and JSPs known as the servlet container, for example, Tomcat.
**Application Servers** **provide additional features** such as Enterprise JavaBeans support, JMS Messaging support, Transaction Management, etc. So we can say that the Application server is a web server with additional functionalities to help developers with enterprise applications.

### Q: Which HTTP method is non-idempotent?

An HTTP method is said to be idempotent if it returns the same result every time. HTTP methods GET, PUT, DELETE, HEAD, and OPTIONS are idempotent method and we should implement our application to make sure these methods always return the same result. HTTP method **POST is non-idempotent** method and we should use post method when implementing something that changes with every request.

For example, to access an HTML page or image, we should use GET because it will always return the same object but if we have to save customer information to the database, we should use the POST method. Idempotent methods are also known as safe methods and we don’t care about the repetitive request from the client for safe methods.

### Q: What is MIME Type?

> Multipurpose Internet Mail Extensions ([MIME](https://en.wikipedia.org/wiki/MIME)) is an Internet standard that extends the format of email messages to support text in character sets other than ASCII, as well as attachments of audio, video, images, and application programs. Message bodies may consist of multiple parts, and header information may be specified in non-ASCII character sets. Email messages with MIME formatting are typically transmitted with standard protocols, such as the Simple Mail Transfer Protocol (SMTP), the Post Office Protocol (POP), and the Internet Message Access Protocol (IMAP).
>
> -- Wikipedia

The “Content-Type” response header is known as MIME Type. Server sends MIME type to client to let them know the kind of data it’s sending. It helps client in rendering the data for user. Some of the mostly used mime types are text/html, text/xml, application/xml etc.

- ServletContext getMimeType(): To get the correct MIME type of the file and use it to set the response content type. It’s very useful in downloading a file through servlet from the server.
- ServletRequest getContentType(): Returns the MIME type of the body of the request, or `null` if the type is not known.
- ServletResponse setContentType(String type): Sets the content type of the response being sent to the client, if the response has not been committed yet.

### Q: What are the advantages of Servlet over CGI?

Servlet technology was introduced to overcome the shortcomings of CGI technology.

- Servlets provide better performance than CGI in terms of processing time, memory utilization because servlets use benefits of multithreading and for each request, a new thread is created, that is faster than loading creating new Object for each request with CGI.
- Servlets and platform and system independent, the web application developed with Servlet can be run on any standard web container such as Tomcat, JBoss, Glassfish servers and on operating systems such as Windows, Linux, Unix, Solaris, Mac, etc.
- Servlets are robust because container takes care of the life cycle of servlet and we don’t need to worry about memory leaks, security, garbage collection, etc.
- Servlets are maintainable and the learning curve is small because all we need to take care is business logic for our application.

> In computing, Common Gateway Interface (CGI) is an interface specification for web servers to execute programs like console applications (also called command-line interface programs) running on a server that generates web pages dynamically. Such programs are known as CGI scripts or simply as CGIs. The specifics of how the script is executed by the server are determined by the server. In the common case, a CGI script executes at the time a request is made and generates HTML.
>
> In brief, an HTTP GET or POST request from the client may send HTML form data to the CGI program via standard input. Other data, such as URL paths, and HTTP header data, are presented as process environment variables.
>
> -- Wikipedia

### Q: What are common tasks performed by Servlet Container?

Servlet containers are also known as web container, for example, Tomcat. Some of the important tasks of servlet container are:

- **Communication Support**: Servlet Container provides easy way of communication between web client (Browsers) and the servlets and JSPs. Because of the container, we don’t need to build a server socket to listen for any request from the web client, parse the request and generate a response. All these important and complex tasks are done by container and all we need to focus is on business logic for the applications.
- **Lifecycle and Resource Management**: Servlet Container takes care of managing the life cycle of servlet. From the loading of servlets into memory, initializing servlets, invoking servlet methods and to destroy them. The container also provides utility like JNDI for resource pooling and management.
- **Multithreading Support**: Container creates a new thread for every request to the servlet and provides them request and response objects to the processing. So servlets are not initialized for each request and save time and memory.
- **JSP Support**: JSPs doesn’t look like normal java classes but every JSP in the application is compiled by container and converted to Servlet and then container manages them like other servlets.
- **Miscellaneous Task**: Servlet container manages the resource pool, perform memory optimizations, execute garbage collector, provides security configurations, support for multiple applications, hot deployment and several other tasks behind the scene that makes a developer life easier.

### Q: What are important features of Servlet 3?

Servlet Specs 3.0 was a major release and some of the important features are:

1. **Servlet Annotations**: Prior to Servlet 3, all the servlet mapping and its init parameters were used to defined in web.xml, this was not convenient and more error prone when number of servlets are huge in an application.

   Servlet 3 introduced the use of Java annotations to define a servlet, filter and listener servlets and init parameters. Some of the important Servlet API annotations are WebServlet, WebInitParam, WebFilter, and WebListener.

   - Specify servlet path by `@WebServlet`
   - Set initial parameters by `@WebInitParam`
   - Others annotations:`@WebListener`, `@WebFilter`, `@MultipartConfig`
   - Almost don't need `web.xml`

2. **Web Fragments**: Prior to servlet specs 3.0, all the web application configurations are required to be present in the web.xml that makes it cluttered with a lot of elements and chances of error increases. So servlet 3 specs introduced web fragments where we can have multiple modules in a single web application, all these modules should have a web-fragment.xml file in META-INF directory. We can include all the elements of web.xml inside the web-fragment.xml too. This helps us in dividing our web application into separate modules that are included as a JAR file in the web application lib directory.

3. **Adding Web Components dynamically**: We can use ServletContext object to add servlets, filters and listeners programmatically. This helps us in building a dynamic system where we are loading a component only if we need it. These methods are addServlet(), addFilter() and addListener() defined in the servlet context object.

4. **Asynchronous Processing**: Asynchronous support was added to delegate the request processing to another thread rather than keeping the servlet thread busy. It can increase the throughput performance of the application. This is an advance topic and I recommend to read [**Async Servlet**](https://www.journaldev.com/2008/async-servlet-example) tutorial.

## The Servlet Interface

### Q: How many objects of a servlet is created?

Only one object at the time of first request by servlet or web container.

### Q: What is the life-cycle of a servlet?

1. Servlet is loaded
2. servlet is instantiated
3. servlet is initialized
4. service the request
5. servlet is destroyed

A servlet is managed through a well defined life cycle that defines how it is loaded and instantiated, is initialized, handles requests from clients, and is taken out of service. This life cycle is expressed in the API by the init , service , and destroy methods of the javax.servlet.Servlet interface that all servlets must implement directly or indirectly through the GenericServlet or HttpServlet abstract classes.

Loading and Instantiation

The servlet container is responsible for loading and instantiating servlets. The loading and instantiation can occur when the container is started, or delayed until the container determines the servlet is needed to service a request.

When the servlet engine is started, needed servlet classes must be located by the servlet container. The servlet container loads the servlet class using normal Java class loading facilities. The loading may be from a local file system, a remote file system, or other network services. After loading the Servlet class, the container instantiates it for use.

Initialization

After the servlet object is instantiated, the container must initialize the servlet before it can handle requests from clients. Initialization is provided so that a servlet can read persistent configuration data, initialize costly resources (such as JDBC™ API-based connections), and perform other one-time activities. The container initializes the servlet instance by calling the init method of the Servlet interface with a unique (per servlet declaration) object implementing the ServletConfig interface. This configuration object allows the servlet to access name-value initialization parameters from the Web application’s configuration information. The configuration object also gives the servlet access to an object (implementing the ServletContext interface) that describes the servlet’s runtime environment.

Request Handling


After a servlet is properly initialized, the servlet container may use it to handle client requests. Requests are represented by request objects of type ServletRequest. The servlet fills out response to requests by calling methods of a provided object of type ServletResponse . These objects are passed as parameters to the service method of the Servlet interface. In the case of an HTTP request, the objects provided by the container are of types HttpServletRequest and HttpServletResponse .


End of Service

The servlet container is not required to keep a servlet loaded for any particular period of time. A servlet instance may be kept active in a servlet container for a period of milliseconds, for the lifetime of the servlet container (which could be a number of days, months, or years), or any amount of time in between. When the servlet container determines that a servlet should be removed from service, it calls the destroy method of the Servlet interface to allow the servlet to release any resources it is using and save any persistent state. For example, the container may do this when it wants to conserve memory resources, or when it is being shut down.
Before the servlet container calls the destroy method, it must allow any threads that are currently running in the service method of the servlet to complete execution, or exceed a server-defined time limit. Once the destroy method is called on a servlet instance, the container may not route other requests to that instance of the servlet. If the container needs to enable the servlet again, it must do so with a new instance of the servlet’s class. After the destroy method completes, the servlet container must release the servlet instance so that it is eligible for garbage collection.

### Q: What are the life-cycle methods for a servlet?

| Method                                                       | Description                                                  |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| public void init(ServletConfig config)                       | It is invoked only once when first request comes for the servlet. It is used to initialize the servlet. |
| public void service(ServletRequest request,ServletResponse)throws ServletException,IOException | It is invoked at each request.The service() method is used to service the request. |
| public void destroy()                                        | It is invoked only once when servlet is unloaded.            |

### Q: Who is responsible to create the object of servlet?

The web container or servlet container.

### Q: When servlet object is created?

At the time of first request or the container is started.

### Q: What is difference between GenericServlet and HttpServlet?

GenericServlet is protocol independent implementation of Servlet interface whereas HttpServlet is HTTP protocol specific implementation. Most of the times we use servlet for creating web application and that’s why we extend HttpServlet class. HttpServlet class extends GenericServlet and also provide some other methods specific to HTTP protocol.

### Q: What is load-on-startup in servlet?

The load-on-startup element of servlet in web.xml is used to load the servlet at the time of deploying the project or server start. So it saves time for the response of first request.

Usually, servlet container loads a servlet on the first client request. Sometimes the servlet is heavy and takes time to loads, we might want to load it on application startup. We can use a load-on-startup element with servlet configuration in the web.xml file or use WebServlet annotation loadOnStartup variable to tell the container to load the servlet on system startup.

```xml
<servlet>
	<servlet-name>foo</servlet-name>
	<servlet-class>com.foo.servlets.Foo</servlet-class>
	<load-on-startup>5</load-on-startup>
</servlet> 
```

The load-on-startup value should be int, if it’s a negative integer then servlet container will load the servlet based on client requests and requirement but if it’s 0 or positive, then the container will load it on application startup.

If there are multiple servlets with load-on-startup value such as 0,1,2,3 then lower integer value servlet will be loaded first.

### Q: What if we pass negative value in load-on-startup?

It will not affect the container, now servlet will be loaded at first request.

### Q: What is servlet attributes and their scope?

Servlet attributes are used for inter-servlet communication, we can set, get and remove attributes in web application. There are three scopes for servlet attributes – request scope, session scope and application scope.

ServletRequest, HttpSession, and ServletContext interfaces provide methods to get/set/remove attributes from request, session and application scope respectively.

Servlet attributes are different from init parameters defined in web.xml for ServletConfig or ServletContext.

### Q: What is ServletConfig object?

`javax.servlet.ServletConfig` is used to pass configuration information to Servlet. Every servlet has it’s own **ServletConfig** object and servlet container is responsible for instantiating this object. We can provide servlet init parameters in web.xml file or through use of WebInitParam annotation. We can use getServletConfig() method to get the ServletConfig object of the servlet.

### Q: How can we create deadlock situation in servlet?

We can create deadlock in servlet by making a loop of method invocation, just call doPost() method from doGet() method and doGet() method to doPost() method to create deadlock situation in servlet.

### Q: What is SingleThreadModel interface?

SingleThreadModel interface was provided for thread safety and it guarantees that no two threads will execute concurrently in the servlet’s service method. However, SingleThreadModel does not solve all thread-safety issues. For example, session attributes and static variables can still be accessed by multiple requests on multiple threads at the same time, even when SingleThreadModel servlets are used. Also, it takes out all the benefits of multithreading support of servlets, that’s why this interface is Deprecated in Servlet 2.4.

### Q: Do we need to override service() method?

When servlet container receives client request, it invokes the service() method which in turn invokes the doGet(), doPost() methods based on the HTTP method of request. I don’t see any use case where we would like to override the service() method. The whole purpose of service() method is to forward to request to corresponding HTTP method implementations. If we have to do some pre-processing of request, we can always use servlet filters and listeners.

### Q: Is it good idea to create servlet constructor?

We can define a constructor for servlet but I don’t think it’s of any use because we won’t be having access to the ServletConfig object until unless servlet is initialized by the container. Ideally, if we have to initialize any resource for the servlet, we should override init() method where we can access servlet init parameters using ServletConfig object.

### Q: Are Servlets Thread Safe? How to achieve thread-safety in servlets?

HttpServlet init() method and destroy() method are called only once in the servlet life cycle, so we don’t need to worry about their synchronization. But service methods such as doGet() or doPost() are getting called in every client request and since servlet uses multithreading, we should provide thread safety in these methods.

If there are any local variables in service methods, we don’t need to worry about their thread-safety because they are specific to each thread but if we have a shared resource then we can use synchronization to achieve thread-safety in servlets when working with shared resources.

### Q: Why HttpServlet class is declared abstract?

HttpServlet class provide HTTP protocol implementation of servlet but it’s left abstract because there is no implementation logic in service methods such as doGet() and doPost() and we should override at least one of the service methods. That’s why there is no point in having an instance of HttpServlet and is declared abstract class.

### Q: why we should override only no-agrs init() method?

If we have to initialize some resource before we want our servlet to process client requests, we should override the init() method. If we override init(ServletConfig config) method, then the first statement should be super(config) to make sure superclass init(ServletConfig config) method is invoked first. That’s why GenericServlet provides another helper init() method without argument that get’s called at the end of init(ServletConfig config) method. We should always utilize this method for overriding init() method to avoid any issues as we may forget to add super() call in overriding init method with ServletConfig argument.

## The Request

### Q: What is difference between Get and Post method?

| Get                                                          | Post                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| 1) Limited amount of data can be sent because data is sent in header. | Large amount of data can be sent because data is sent in body. |
| 2) Not Secured because data is exposed in URL bar.           | Secured because data is not exposed in URL bar.              |
| 3) Can be bookmarked                                         | Cannot be bookmarked                                         |
| 4) Idempotent                                                | Non-Idempotent                                               |
| 5) It is more efficient and used than Post                   | It is less efficient and used                                |

### Q: How can we upload the file to the server using servlet?

One of the way is by MultipartRequest class provided by third party.



### Q: What is the use of servlet wrapper classes?

Servlet HTTP API provides two wrapper classes – `HttpServletRequestWrapper` and `HttpServletResponseWrapper`. These wrapper classes are provided to help developers with custom implementation of servlet request and response types. We can extend these classes and override only specific methods we need to implement for custom request and response objects. These classes are not used in normal servlet programming.



## Servlet Context



### Q: What is ServletContext object?

`javax.servlet.ServletContext` interface provides access to web application parameters to the servlet. The ServletContext is unique object and available to all the servlets in the web application. When we want some init parameters to be available to multiple or all of the servlets in the web application, we can use ServletContext object and define parameters in web.xml using <context-param> element. We can get the ServletContext object via the *getServletContext()* method of ServletConfig. Servlet containers may also provide context objects that are unique to a group of servlets and which is tied to a specific portion of the URL path namespace of the host.

ServletContext is enhanced in Servlet Specs 3 to introduce methods through which we can programmatically add Listeners and Filters and Servlet to the application. It also provides some utility methods such as *getMimeType()*, *getResourceAsStream()* etc.

### Q: What is difference between ServletConfig and ServletContext?

Some of the differences between ServletConfig and ServletContext are:

- The container creates object of ServletConfig for each servlet whereas object of ServletContext is created for each web application. ServletConfig is a unique object per servlet whereas ServletContext is a unique object for complete application.
- ServletConfig is used to provide init parameters to the servlet whereas ServletContext is used to provide application level init parameters that all other servlets can use.
- We can’t set attributes in ServletConfig object whereas we can set attributes in ServletContext that other servlets can use in their implementation.

## The Response

### Q: What is difference between PrintWriter and ServletOutputStream?

PrintWriter is a character-stream class whereas ServletOutputStream is a byte-stream class. We can use PrintWriter to write character based information such as character array and String to the response whereas we can use ServletOutputStream to write byte array data to the response.

We can use ServletResponse getWriter() to get the PrintWriter instance whereas we can use ServletResponse getOutputStream() method to get the ServletOutputStream object reference.

### Q: Can we get PrintWriter and ServletOutputStream both in a servlet?

We can’t get instances of both PrintWriter and ServletOutputStream in a single servlet method, if we invoke both the methods; getWriter() and getOutputStream() on response; we will get `java.lang.IllegalStateException` at runtime with message as other method has already been called for this response.

### Q: How can we invoke another servlet in a different application?

We can’t use RequestDispatcher to invoke servlet from another application because it’s specific for the application. If we have to forward the request to a resource in another application, we can use the ServletResponse sendRedirect() method and provide the complete URL of another servlet. This sends the response to the client with the response code as 302 to forward the request to another URL. If we have to send some data also, we can use cookies that will be part of the servlet response and sent in the request to another servlet.

## Filtering

### Q: What is filter?

A filter is an object that is invoked either at the preprocessing or postprocessing of a request. It is pluggable.

A filter is a reusable piece of code that can transform the content of HTTP requests, responses, and header information. Filters do not generally create a response or respond to a request as servlets do, rather they modify or adapt the requests for a resource, and modify or adapt responses from a resource.

### Q: Why do we have servlet filters?

Servlet Filters are pluggable java components that we can use to intercept and process requests before they are sent to servlets and response after servlet code is finished and before container sends the response back to the client.

Some common tasks that we can do with filters are:

- Logging request parameters to log files.
- Authentication and authorization of request for resources.
- Formatting of request body or header before sending it to servlet.
- Compressing the response data sent to the client.
- Alter response by adding some cookies, header information etc.

### Q: What is the effective way to make sure all the servlets are accessible only when the user has a valid session?

We know that servlet filters can be used to intercept request between a servlet container and servlet, we can utilize it to create an authentication filter and check if the request contains a valid session or not.

## Sessions

### Q: What is Session Tracking?

**Session** simply means a particular interval of time.

Session Tracking is a way to maintain state of an user. Http protocol is a stateless protocol. Each time user requests to the server, server treats the request as the new request. So we need to maintain the state of an user to recognize to particular user.

### Q: What are Cookies?

A cookie is a small piece of information that is persisted between the multiple client requests. A cookie has a name, a single value, and optional attributes such as a comment, path and domain qualifiers, a maximum age, and a version number.

The HttpServletRequest interface provides the getCookies method to obtain an array of cookies that are present in the request. These cookies are data sent from the client to the server on every request that the client makes. Typically, the only information that the client sends back as part of a cookie is the cookie name and the cookie value. Other cookie attributes that can be set when the cookie is sent to the browser, such as comments, are not typically returned. The specification also allows for the cookies to be HttpOnly cookies. HttpOnly cookies indicate to the client that they should not be exposed to client-side scripting code (It’s not filtered out unless the client knows to look for this attribute). The use of HttpOnly cookies helps mitigate certain kinds of cross-site scripting attacks.

### Q: What is difference between Cookies and HttpSession?

Cookie works at client side whereas HttpSession works at server side.

### Q: What is the disadvantage of cookies?

It will not work if cookie is disabled from the browser.

### Q: What are different methods of session management in servlets?

The session is a conversational state between client and server and it can consist of multiple request and response between client and server. Since HTTP and Web Server both are stateless, the only way to maintain a session is when some unique information about the session (session-id) is passed between server and client in every request and response.

Some of the common ways of session management in servlets are:

1. User Authentication
2. HTML Hidden Field
3. Cookies
4. URL Rewriting
5. Session Management API

Read more about these session management approaches in detail at **Servlet Session Management Tutorial**.

### Q: What is URL Rewriting?

We can use HttpSession for session management in servlets but it works with Cookies and we can disable the cookie in client browser. Servlet API provides support for URL rewriting that we can use to manage session in this case.

The best part is that from a coding point of view, it’s very easy to use and involves one step – encoding the URL. Another good thing with Servlet URL Encoding is that it’s a fallback approach and it kicks in only if browser cookies are disabled.

We can encode URL with HttpServletResponse encodeURL() method and if we have to redirect the request to another resource and we want to provide session information, we can use encodeRedirectURL() method.

### Q: How does Cookies work in Servlets?

Cookies are used a lot in web client-server communication, it’s not something specific to java. Cookies are text data sent by server to the client and it gets saved at the client local machine.

Servlet API provides cookies support through javax.servlet.http.Cookie class that implements Serializable and Cloneable interfaces.

HttpServletRequest getCookies() method is provided to get the array of Cookies from the request, since there is no point of adding Cookie to request, there are no methods to set or add a cookie to request.

Similarly, HttpServletResponse addCookie(Cookie c) method is provided to attach cookie in the response header, there are no getter methods for a cookie.

### Q: What is the difference between encodeRedirectUrl and encodeURL?

HttpServletResponse provide method to encode URL in HTML hyperlinks so that the special characters and white spaces are escaped and append session id to the URL. It behaves similar to URLEncoder encode method with additional process to append jsessionid parameter at the end of the URL.

However HttpServletResponse encodeRedirectUrl() method is used specially for encode the redirect URL in response.

So when we are providing URL rewriting support, for hyperlinks in HTML response, we should use encodeURL() method whereas for redirect URL we should use encodeRedirectUrl() method.

## Dispatching Requests

### Q: What is servlet collaboration?

When one servlet communicates to another servlet, it is known as servlet collaboration. There are many ways of servlet collaboration:

- RequestDispacher interface
- sendRedirect() method etc.

### Q: What is the purpose of RequestDispatcher Interface?

The RequestDispatcher interface is used to dispatching the request to another resource that can be HTML, JSP or another servlet in the same application. We can also use this to include the content of another resource to the response. This interface is used for inter-servlet communication in the same context.

There are two methods defined in this interface:

1. void forward(ServletRequest request, ServletResponse response) – forwards the request from a servlet to another resource (servlet, JSP file, or HTML file) on the server.
2. void include(ServletRequest request, ServletResponse response) – includes the content of a resource (servlet, JSP page, HTML file) in the response.

We can get RequestDispatcher in a servlet using ServletContext getRequestDispatcher(String path) method. The path must begin with a / and is interpreted as relative to the current context root.

### Q: How do we call a jsp or servlet from the servlet?

We can use RequestDispatcher forward() method to forward the processing of a request to another servlet. If we want to include the another servlet output to the response, we can use RequestDispatcher include() method.

For example:

```java
RequestDispatcher requestDispatcher=request.getRequestDispatcher("/login.jsp"); 
requestDispatcher.forward(request,response); 
```



### Q: Difference between forward() method and sendRedirect() method ?

| forward() method                                             | sendRedirect() method                                        |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| forward() sends the same request to another resource.        | sendRedirect() method sends new request always because it uses the URL bar of the browser. |
| forward() method works at server side.                       | sendRedirect() method works at client browser side.          |
| forward() method works within the server only.               | sendRedirect() method works within and outside the server.   |
| In forward() browser is unaware of the actual processing resource and the URL in address bar remains same | In sendRedirect() URL in address bar change to the forwarded resource. |
| forward() can’t be used to invoke a servlet in another context | sendRedirect() can invoke a servlet in another context       |

We should use forward() when accessing resources in the same application because it’s faster than sendRedirect() method that required an extra network call.

### Q: How to handle exceptions thrown by application with another servlet?

If you notice, doGet() and doPost() methods throw ServletException and IOException. Since browser understand only HTML, when our application throw exception, servlet container processes the exception and generate a HTML response. Same goes with other error codes like 404, 403 etc.

Servlet API provides support for custom Exception and Error Handler servlets that we can configure in the deployment descriptor, the whole purpose of these servlets are to handle the Exception or Error raised by application and send HTML response that is useful for the user. We can provide a link to the application home page or some details to let the user know what went wrong.

We can configure them in web.xml like below:

```xml
<error-page>
	<error-code>404</error-code>
    <location>/AppExceptionHandler</location>
</error-page>
   
<error-page>
  	<exception-type>javax.servlet.ServletException</exception-type>
  	<location>/AppExceptionHandler</location>
</error-page>
```

## Web Applications

### Q: What is war file?

A war (web archive) file specifies the web elements. A servlet or jsp project can be converted into a war file. Moving one servlet project from one place to another will be fast as it is combined into a single file.

### Q: How to create war file?

The war file can be created using jar tool found in jdk/bin directory. If you are using Eclipse or Netbeans IDE, you can export your project as a war file.

To create war file from console, you can write following code.

```
jar -cvf abc.war * 
```

Now all the files of current directory will be converted into abc.war file.

### Q: What is a web application and what is its directory structure?

Web Applications are modules that run on the server to provide both static and dynamic content to the client browser. Apache webserver supports PHP and we can create a web application using PHP. Java provides web application support through Servlets and JSPs that can run in a servlet container and provide dynamic content to the client browser.

Java Web Applications are packaged as Web Archive (WAR) and it has a defined structure like below image.

![](images/java-web-servlet-WAR-directory-structure.png)

## Application Lifecycle Events

### Q: How can we perform any action at the time of deploying the project?

By the help of ServletContextListener interface.

### Q: How to notify an object in session when session is invalidated or timed-out?

If we have to make sure an object gets notified when session is destroyed, the object should implement `javax.servlet.http.HttpSessionBindingListener` interface. This interface defines two callback methods – valueBound() and valueUnbound() that we can define to implement processing logic when the object is added as attribute to the session and when session is destroyed.

### Q: Why do we have servlet listeners?

We know that using ServletContext, we can create an attribute with application scope that all other servlets can access but we can initialize ServletContext init parameters as String only in the deployment descriptor (web.xml). What if our application is database-oriented and we want to set an attribute in ServletContext for Database Connection.

If your application has a single entry point (user login), then you can do it in the first servlet request but if we have multiple entry points then doing it everywhere will result in a lot of code redundancy. Also if the database is down or not configured properly, we won’t know until the first client request comes to the server. To handle these scenarios, servlet API provides Listener interfaces that we can implement and configure to listen to an event and do certain operations.

## Mapping Requests to Servlet

## Security

### Q: What are different ways for servlet authentication?

Servlet Container provides different ways of login based servlet authentication:

1. **HTTP Basic Authentication**
2. **HTTP Digest Authentication**
3. **HTTPS Authentication**
4. **Form Based Login**: A standard HTML form for authentication, advantage is that we can change the login page layout as our application requirements rather than using HTTP built-in login mechanisms.

### Q: How can we achieve transport layer security for our web application?

We can configure our servlet container to use SSL for message communication over the network. To configure SSL on Tomcat, we need a digital certificate that can be created using Java keytool for a development environment. For the production environment, you should get the digital certificate from SSL certificate providers, for example, Verisign or Entrust.

## Deployment Descriptor

### Q: What is a deployment descriptor?

The deployment descriptor is a configuration file for the web application and its name is web.xml and it resides in WEB-INF directory. Servlet container uses this file to configure web application servlets, servlet config params, context init params, filters, listeners, welcome pages and error handlers.

With servlet 3.0 annotations, we can remove a lot of clutter from web.xml by configuring servlets, filters, and listeners using annotations.



## Annotation and Pluggability

### Q: What are the annotations used in Servlet 3?

There are mainly 3 annotations used for the servlet.

1. @WebServlet : for servlet class.
2. @WebListener : for listener class.
3. @WebFilter : for filter class.

## Others

### Q: What is URL Encoding?

URL Encoding is the process of converting data into CGI form so that it can travel across the network without any issues. URL Encoding strips the white spaces and replaces special characters with escape characters. We can use java.net.URLEncoder.encode(String str, String unicode) to encode a String. URL Decoding is the reverse process of encoding and we can use java.net.URLDecoder.decode(String str, String unicode) to decode the encoded string. For example “Pankaj’s Data” is encoded to “Pankaj%27s+Data”.

## II. JSP

## Introduction to JSP

## Expression Language (EL)

## JSP Standard Tag Library (JSTL)

## Tag Extensions

## Tag Files



## References

- [Servlet interview questions - Javatpoint](https://www.javatpoint.com/servletinterview)
- [50 Servlet Interview Questions and Answers - JournalDev](https://www.journaldev.com/2015/servlet-interview-questions-and-answers)
- [Top 55 Servlets Interview Question You Need to Know - edureka](https://www.edureka.co/blog/interview-questions/servlet-interview-questions/)
