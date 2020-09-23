# Java Interview Questions [Simplified Version]

### Content

- Java
  - Java SE
  - Java Data Access
    - JDBC
    - Persistence Frameworks
      - MyBatis
      - Hibernate
    - NoSQL Access
      - Jedis
      - MongoDB Java Drivers
    - Java Cache
      - Guava Cache
      - Ehcache
  - Java Web
    - Java Servlet
    - Web Pages
      - JavaServer Pages
    - Web Frameworks
      - Spring
      - Spring Boot
    - Security Frameworks
      - Spring Security
      - Apache Shiro
    - Web Servers
      - Tomcat
      - Jetty
    - Web Protocols
      - HTTP
      - HTTPS
      - HTTP2
- Data Storage
- CS fundamentals
- System Design

## Main

## Java SE

### I. Introduction

Java Platform

- JDK vs JRE vs JVM

Java Features
- cross platforms
- not 100% object-oriented

Java History

### II. Basics

Variables and Types

- 8 primitive data types (bytes, scope, default value)
- decimal numbers can't precisely represent
- character encoding and charsets
- string length vs string byte array length

Operators and Expressions

- operator kinds
- operators priority

String and Array

- why String is immutable or final
- String vs StringBuffer vs StringBuilder

### III. Core

Classes and Objects

- Object-Oriented Programming
  - object-oriented vs procedure-oriented
  - features of object-oriented programming
  - principles of object-oriented design
  - relationships between classes
- Classes and Objects
  - object creation ways
  - the process of object creation 
- Methods
  - pass by value vs pass by reference
- Keywords
  - final (keyword for classes, methods, variables)
  - static
  - abstract
  - access modifiers
- java.lang.Object
  - equals() and hashcode()
  - equals() vs ==

Inheritance and Polymorphism

- polymorphism definition
- method overriding vs method overloading

Interface, Lambada, and Inner Classes

- interface vs abstract class
- why use nested classes
- static nested class vs inner class

Exceptions, Assertions, and Logging

- common exception class names
- return statements in try-catch-finally

Generic Programming

Annotations

Reflection and Proxy

- reflection definition
- proxy applicability

Enumeration Types and Wrapper Types

- wrapper classes definition
- boxing, unboxing, and auto boxing of wrapper classes
- wrapper classes caches
- primitive data types vs wrapper classes (declare variables selection)

### IV. Advanced

Input and Output and NIO

- I/O streams definitions
- I/O steam types
- BIO vs NIO vs AIO
- serialization definition
- transient keyword

Collections and Streams

- Container API
  - Common Container classes
  - HashMap vs Hashtable
  - Array vs ArrayList
- Container Implementation Principles
  - HashMap implementation
  - Concurrent collection classes implementation
- Iterator
  - fail fast and non-fail fast

Concurrency

- Processes and Threads
  - process vs thread
  - daemon thread
- Thread Objects
  - thread class creation ways
  - start thread ways
  - thread status
  - sleep() vs wait()
  - sleep(), join(), yield() of Thread class
  - wait(), notify(), notifyAll() of Object class
  - FutureTask and ForkJoinTask
- Synchronization and Thread-Safe
  - what is concurrency problems (Thread Interference, Memory Consistency Errors)
  - how to solve concurrency problems
  - synchronized implementation
- Liveness Problems
  - deadlock, starvation and livelock definitions
  - how to avoid deadlock
  - Deadlock code examples
  - Livelock code examples
- Guarded Blocks
- Advanced Concurrency Objects
  - Lock
    - synchronized vs ReentrantLock
    - ReentrantLock implementation pricinples
  - Executors and Thread Pools
    - thread pool types
  - Concurrent Collections
  - Atomic Variables
    - volatile variables vs atomic variables vs immutable variables 
  - ThreadLocal and ThreadLocalRandom
    - ThreadLocal definition and usage
    - ThreadLocalRandom definition and usage
  - Concurrency Others
    - java.util.concurrent.CountDownLatch
    - java.util.concurrent.CyclicBarriers
    - java.util.concurrent.Semaphore
    - java.util.concurrent.Exchanger

Network Programming

Java Security

JMX, JNDI, JAXP, RMI

Native Methods

### V. Utility

## Java Data Access

## JDBC

## MyBatis

## Hibernate

## Java Web





