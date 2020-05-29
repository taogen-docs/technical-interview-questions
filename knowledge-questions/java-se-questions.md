# Java SE Knowledge Points and Questions

### Content

- Part I: Fundamental
  - Introduction to Java
  - Variable and Primitive Data Type
  - String and Arrays
  - Expressions (Operations)
  - Statements (Control Flow)
- Part II: Core
  - Objects and Classes (Objects, Classes, Wrapper Classes)
  - Inheritance (Inheritance, Polymorphism)
  - Interface and Inner Classes
  - Keywords
  - Exceptions, Assertions, and Logging
  - Reflection, Static Proxy, Dynamic Proxy
  - Generic Programming
  - Annotation
  - Lambda Expressions and Streams
  - Input and Output (IO)
  - **Container** (Data Structures)
- Part III: Advanced
  - **Concurrency**
  - Network Programming (Socket, NIO, HTTP, RPC, MQ, AMQP, MQTT)
  - **JVM**
  - **Design Patterns**
- Others
  - XML and JSON
  - Database Programming
  - Date and Time
  - Regular Expression
  - Internationalization
  - //Swing and Graphics
  - Native Methods

## Main

## Part I: Fundamental

## Introduction to Java

### JDK, JRE, and JVM

Q: [Explain JDK, JRE and JVM?](https://www.edureka.co/blog/interview-questions/java-interview-questions/#Jdk-Jre-and-Jvm)

A: ...

### Java Core Features

Q: How Java cross platforms(Write once, run anywhere)?

### Java Version and new Features



## Variable and Primitive Data Type

### Basic Data Types

Q: What are the basic data types in Java? What are their value ranges?

Q: Why does computer float data type can't precisely represent decimal fraction?

A: Computer using binary number to store data. It just can represent 2^(-1)=0.5, 2^(-2)=0.25, 2^(-3)=0.125. 

Q: Why can't you use float data type to represent amount of money?

A: A float number just is an approximate value. It can't precisely represent a decimal fraction. You can use `BigDecimal` or `Long` in Java to represent the amount of money.

### Character Encodings



## String and Arrays

### String

Q: Why String is immutable or final in java?

Q: `String` vs `StringBuffer` vs `StringBuilder`?

## Expressions (Operations)



## Statements (Control Flow)

---

## Part II: Core

## Objects and Classes (Objects, Classes, Wrapper Classes)

### Object-Oriented

Q: Object-Oriented vs Procedure-Oriented?

Q: Object-Oriented basic features?

Q: Object-Oriented basic principles?

### Methods pass by value vs. pass by reference

Q: Pass by value vs. pass by reference

### wrapper class

Q: What are wrapper classes? Why do we need it?

Q: What are boxing, unboxing, and autoboxing? What are wrapper classes caches?

Q: Using primitive data types or wrapper classes to declare a variable?

A: Wrapper classes. Because they have not concrete default values. When variables have not assignment, primitive data types have default values, but wrapper classes are null. Default values of primitive data type may cause error result. When wrapper classes are null, the program may occur `NullPointerException`, but it can't cause error results.

## Inheritance (Inheritance, Polymorphism)

Q: What is Polymorphism?

Q: Method overriding vs method overloading?

Q: Inheritance vs composition

## Interface and Inner Classes

## Keywords

> final, abstract, static
>
> public, protected, private
>
> transient, volatile, synchronized
>
> instanceof

### final

Q: What is final meaning?

A: 

- the `final` keyword for variables it is meaning the variable can't reassignment. 
- final for method
- final for class 

## Exceptions, Assertions, and Logging

### Exceptions

Q: Common Exception class names?

Q: How to handle exception? Right ways of handling exception.

Q: Return statements in try-catch-finally?

## Reflection, Static Proxy, Dynamic Proxy

Q: What is reflection

Q: static proxy vs dynamic proxy?

## Generic Programming

## Annotation

## Lambda Expressions and Streams

## Input and Output (IO)

### BIO(Blocking IO), AIO(Asynchronous IO), NIO (Non-blocking IO)

### Serialization

## Container

### Container Hierarchy

### Difference. Difference between Implementation classes of a data structure

> Lists, Sets, Maps

### Applicability. 

Q: How to choice data structure for different usage scenario?

### Implementation Details

`hashcode()`

### Iterator

Q: Fail fast and fail safe iterators

---

## Part III: Advanced

## Concurrency

> Thread Safe
>
> volatile
>
> synchronized
>
> lock
>
> ThreadLocal
>
> Thread Pool
>
> ConcurrentHashMap







## Network Programming

## JVM

> Memory Model, Class Load Mechanism, GC Mechanism
>
> How to location OOM, How to location infinite dead loop

## Design Patterns

Singleton

---

## Part IV: Others

## Date and Time