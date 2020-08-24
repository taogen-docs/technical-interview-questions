# Java SE Interview Questions

### Content

- I. Introduction
  - Java Platform
  - Java Features
  - Java History
- II. Basics
  - Variables and Types
  - Operators and Expressions
  - String and Array
- III. Core
  - Classes and Objects
  - Inheritance and Polymorphism
  - Interface, Lambada, and Inner Classes
  - Exceptions, Assertions, and Logging
  - Generic Programming
  - Annotations
  - Reflection and Proxy
  - Enumeration Types and Wrapper Types
- IV. Advanced
  - Input and Output
  - Collections and Streams
  - Concurrency
  - Network Programming
  - Java Security
  - JMX, JNDI, JAXP, RMI
  - Native Methods
- V. Utility



### Details

- I. Introduction
  - <a name="java-platform-c" href="#java-platform-t">Java Platform</a>
    - [x] [Explain JDK, JRE and JVM?](#Explain JDK, JRE and JVM?)
  - <a name="java-features-c" href="#java-features-t">Java Features</a>
    - [x] [How Java cross platforms(Write once, run anywhere)?](#How Java cross platforms(Write once, run anywhere)?)
    - [x] [Why Java is not 100% Object-oriented?](#Why Java is not 100% Object-oriented?)
  - <a name="java-history-c" href="#java-history-t">Java History</a>
- II. Basics
  - <a name="variables-and-types-c" href="#variables-and-types-t">Variables and Types</a>
    - [x] [What are the basic data types in Java? What are their value ranges?](#What are the basic data types in Java? What are their value ranges?)
    - [x] [Why does computer float data type can't precisely represent decimal fraction?](#Why does computer float data type can't precisely represent decimal fraction?)
    - [x] [Why can't you use float data type to represent amount of money?](#Why can't you use float data type to represent amount of money?)
    - [x] [Character encoding and charsets?](#Character encoding and charsets?)
    - [x] [String length vs byte array length of string?](#String length vs byte array length of string?)
  - <a name="operators-and-expressions-c" href="#operators-and-expressions-t">Operators and Expressions</a>
  - <a name="control-flow-c" href="#control-flow-t">Control Flow</a>
  - <a name="string-and-array-c" href="#string-and-array-t">String and Array</a>
    - [x] [Why String is immutable (or final) in java?](#Why String is immutable or final in java?)
    - [x] [Why is the String class declared final in Java?](#Why is the String class declared final in Java?)
    - [x] [How does String implement immutability](#How does String implement immutability)
    - [x] [String vs StringBuffer vs StringBuilder?](#String vs StringBuffer vs StringBuilder?)
- III. Core
  - <a name="classes-and-objects-c" href="#classes-and-objects-t">Classes and Objects</a>
    - Object-Oriented Programming
      - [x] [Object-Oriented vs Procedure-Oriented?](#Object-Oriented vs Procedure-Oriented?)
      - [x] [What are object-oriented programming major features?](#What are object-oriented programming major features?)
      - [x] [Principles of object-oriented design?](#Principles of object-oriented design?)
      - [x] [Relationships between classes: Generalization vs realization vs composition vs aggregation vs association vs dependency?](#Relationships between classes: Generalization vs realization vs composition vs aggregation vs association vs dependency?)
    - Methods
      - [x] [Pass by value vs. pass by reference?](#Pass by value vs. pass by reference?)
    - Keywords
      - [x] [What is final keyword meaning?](#What is final keyword meaning?)
      - [x] [What is static keyword meaning?](#What is static keyword meaning?)
      - [x] [What is abstract keyword meaning?](#What is abstract keyword meaning?)
      - [x] [What are access modifiers in Java?](#What are access modifiers in Java?) (public, protected, private)
      - (transient, volatile, synchronized)
      - (instanceof)
    - The java.lang.Object
      - [x] [What is equals() and hashcode() method?](#What is equals() and hashcode() method?)
      - [x] [equals() vs ==?](#equals() vs ==?)
  - <a name="inheritance-and-polymorphism-c" href="#inheritance-and-polymorphism-t">Inheritance and Polymorphism</a>
    - [x] [What is Polymorphism?](#What is Polymorphism?)
    - [x] [Method overriding vs method overloading?](#Method overriding vs method overloading?)
  - <a name="interface-c" href="#interface-t">Interface, Lambada, and Inner Classes</a>
    - [x] [Why use nested classes?](#Why use nested classes?)
  - <a name="exceptions-c" href="#exceptions-t">Exceptions, Assertions, and Logging</a>
    - [x] [Common Exception class names?](#Common Exception class names?)
    - [ ] How to handle exception? Right ways of handling exception.
    - [ ] Return statements in try-catch-finally?
  - <a name="generic-c" href="#generic-t">Generic Programming</a>
  - <a name="annotations-c" href="#annotations-t">Annotations</a>
  - <a name="reflection-c" href="#reflection-t">Reflection and Proxy</a>
    - [x] [What is reflection?](#What is reflection?)
    - [ ] [Proxy Applicability?](#Proxy Applicability?)
  - <a name="enum-c" href="#enum-t">Enumeration Types and Wrapper Types</a>
    - [ ] What are wrapper classes? Why do we need it?
    - [ ] What are boxing, unboxing, and autoboxing? What are wrapper classes caches?
    - [x] [Using primitive data types or wrapper classes to declare a variable?](#Using primitive data types or wrapper classes to declare a variable?)
- IV. Advanced
  - <a name="io-c" href="#io-t">Input and Output</a>
    - [x] [What are I/O Streams? What are IO stream types?](#What are I/O Streams? What are IO stream types?)
    - [x] [BIO vs NIO vs AIO?](#BIO vs NIO vs AIO?)
    - [ ] [What is serialization?](#What is serialization?)
  - <a name="collections-c" href="#collections-t">Collections and Streams</a>
    - [x] [Talk about Collection API?](#Talk about Collection API?)
    - [x] [HashMap vs Hashtable?](#HashMap vs Hashtable?)
    - [x] [Why HashMap allows null key but Hashtable does not?](#Why HashMap allows null key but Hashtable does not?)
    - [x] [Array vs ArrayList?](#Array vs ArrayList?)
    - [x] [How HashMap works?](#How HashMap works?) (HashMap implementation?)
    - Contrast List: Array vs ArrayList vs LinkedList vs Vector vs CopyOnWriteArrayList
    - Stack and Queue: Queue vs Deque vs BlockingDeque vs BlockingQueue 
      - Stack vs ArrayDeque vs ConcurrentLinkedDeque vs LinkedBlockingDeque
    - Set and Map
    - Collection Applicability
      - (How to choice data structure for different usage scenario?)
    - Implementation Principles
      - How Concurrent Collection Classes Work?
    - Iterator
      - (Fail fast and fail safe iterators)
  - <a name="concurrency-c" href="#concurrency-t">Concurrency</a>
    - Processes and Threads
      - [x] [Process vs Thread?](#Process vs Thread?)
      - [x] [What is daemon thread?](#What is daemon thread?)
    - Thread Objects
      - [x] [Creating Thread classes ways?](#Creating Thread classes ways?)
      - [x] [Creating Thread ways?](#Creating Thread ways?)
      - [x] [What are Thread status?](#What are Thread status?)
      - [x] [sleep() vs wait()?](#sleep() vs wait()?)
    - Synchronization and Thread-Safe
      - [x] [How thread-safe works?](#How thread-safe works?)
      - [ ] [How synchronized works or exclusive lock works?](#How synchronized works or exclusive lock works?)
    - Liveness Problems
      - [x] [Deadlock vs starvation vs livelock?](#Deadlock vs starvation vs livelock?) 
      - [x] [How to avoid deadlock?](#How to avoid deadlock?)
    - High Concurrency
      - [x] [synchronized vs ReentrantLock?](#synchronized vs ReentrantLock?)
      - [x] [Volatile variables vs atomic variables vs immutable objects?](#Volatile variables vs atomic variables vs immutable objects?)
    - Concurrency Others
      - [x] [What is ThreadLocal?](#What is ThreadLocal?)
      - [x] [When should I use a ThreadLocal variable?](#When should I use a ThreadLocal variable?)
  - <a name="network-c" href="#network-t">Network Programming</a>
  - <a name="java-security-c" href="#java-security-t">Java Security</a>
  - <a name="jmx-c" href="#jmx-t">JMX, JNDI, JAXP, RMI</a>
  - <a name="native-methods-c" href="#native-methods-t">Native Methods</a>
- V. Utility

## I. Introduction


<br>
<h2><a name="java-platform-t" href="#java-platform-c">Java Platform</a></h2>
<br>

### Explain JDK, JRE and JVM?

| **JDK**                                                      | **JRE**                                                      | **JVM**                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| It stands for Java Development Kit.                          | It stands for Java Runtime Environment.                      | It stands for Java Virtual Machine.                          |
| It is the tool necessary to compile, document and package Java programs. | JRE refers to a runtime environment in which Java bytecode can be executed. | It is an abstract machine. It is a specification that provides a run-time environment in which Java bytecode can be executed. |
| It contains JRE + development tools.                         | It’s an implementation of the JVM which physically exists.   | JVM follows three notations: Specification, **Implementation,** and **Runtime Instance**. |

JDK: it provide development kit (such as javac, java, javap, jconsole), document, and java runtime environment (JRE).

JRE: It provide java bytecode runtime environment. It contains lib and bin.

If you only need to run a java application, you can just install JRE.

<br>

<h2><a name="java-features-t" href="#java-features-c">Java Features</a></h2>

<br>

### How Java cross platforms(Write once, run anywhere)?

Java is called platform independent because of its byte codes which can run on any system irrespective of its underlying operating system.

### Why Java is not 100% Object-oriented?

Eight primitive data types such as boolean, byte, int which are not objects.

<br>

<h2><a name="java-history-t" href="#java-history-c">Java History</a></h2>
<br>

## II. Basics



<br>

<h2><a name="variables-and-types-t" href="#variables-and-types-c">Variables and Types</a></h2>
<br>

### What are the basic data types in Java? What are their value ranges?

| Data Type | Bytes   | Scope         | Default Value               |
| --------- | ------- | ------------- | --------------------------- |
| boolean   | 1 byte  | true or false | false                       |
| byte      | 1 byte  | -128~127      | 0                           |
| short     | 2 bytes | -2^15~2^15-1  | 0                           |
| int       | 4 bytes | -2^31~2^31-1  | 0                           |
| long      | 8 bytes | -2^63~2^63-1  | 0                           |
| float     | 4 bytes |               | 0.0F                        |
| double    | 8 bytes |               | 0.0D                        |
| char      | 2 bytes | 0~2^16-1      | \u0000 (represent for null) |

numeric types

- byte
- short
- int
- long
- float
- double

others type

- boolean
- char

### Why does computer float data type can't precisely represent decimal fraction?

Computer using binary number to store data. It just can represent 2^(-1)=0.5, 2^(-2)=0.25, 2^(-3)=0.125. 

### Why can't you use float data type to represent amount of money?

A float number just is an approximate value. It can't precisely represent a decimal fraction. You can use `BigDecimal` or `Long` in Java to represent the amount of money.

### Character encoding and charsets?

Character encoding: converting text characters to binary representation. For example, "T" in ASCII encodes to "01010100"

Character decoding: converting binary to text characters.

Charsets: The set of characters that are included in a mapping definition.

Code point: A code point is an integer reference to a particular character. For example, "T" in Unicode has a code point "U+0054".

Unicode standard: Unicode is an information technology (IT) standard for the consistent encoding, representation, and handling of text expressed in most of the world's writing systems.

Charsets of Unicode standard: UTF-8, UTF-16, UTF-32.

**Charsets Table**

| Charset           | Bytes              | Number of characters | Represent                                                    | Code point       |
| ----------------- | ------------------ | -------------------- | ------------------------------------------------------------ | ---------------- |
| ASCII             | 1 byte (7 bits)    | 128 characters       | English alphabets, digits, special characters                |                  |
| ISO-8859-1        | 1 byte             | 256 characters       | ASCII extensions.                                            |                  |
| GB2312            | 2 bytes            |                      | Chinese. Compatible with ASCII                               |                  |
| GBK               | 2 bytes            |                      | Chinese. GB2312 extensions. Compatible with GBK.             |                  |
| Big5              |                    |                      | Chinese for Taiwan.                                          |                  |
| Unicode（UTF-16） | 2 bytes            |                      | Universal.                                                   |                  |
| UTF-8             | variable 1~6 bytes |                      | Universal. It has space efficiency. It is the most common encoding used on the web. | u+4e2d or \u4e2d |
| UTF-32            | 4 bytes            |                      | Universal.                                                   |                  |

Print Java default charset

```java
System.out.println(Charset.defaultCharset().displayName());
```

Print String bytes values

```java

public static void printBinary(String source, Charset charset){
    byte[] bytes = source.getBytes(charset);
    for (Byte b : bytes) {
        System.out.println(String.format("%8s",Integer.toBinaryString(b & 0xff)).replace(' ', '0'));
    }
}

public static void printHex(String source, Charset charset) {
    byte[] bytes = source.getBytes(charset);
    for (Byte b : bytes) {
        System.out.println(Integer.toHexString(b & 0xff));
    }
}

public static void printDecimal(String source, Charset charset) {
    byte[] bytes = source.getBytes(charset);
    for (Byte b : bytes) {
        System.out.println(Byte.toUnsignedInt(b));
    }
}
```



### String length vs byte array length of string?

 Get a String character number (String length)

```java
string.length();
```

Get a String using of the number of bytes

> It depend on what charset the string use.
>
> UTF-16 bytes size: prefix two bytes + character-size(string-length) * 2
>
> UFT-8 bytes size: Sum of bytes of every character use.
>
> For example, the "中" used 2 bytes in UTF-16, and used 3 bytes in UTF-8.
>
> "中".getBytes(UTF_8).length is 3
>
> "中".getBytes(UTF_16).length is 4

<br>

<h2><a name="operators-and-expressions-t" href="#operators-and-expressions-c">Operators and Expressions</a></h2>
<br>



<br>
<h2><a name="control-flow-t" href="#control-flow-c">Control Flow</a></h2>
<br>



<br>
<h2><a name="string-and-array-t" href="#string-and-array-c">String and Array</a></h2>
<br>

### Why String is immutable (or final) in java?

Because String objects are cached in String pool, all same characters strings only one instance and can't modify. Since cached String literals are shared between multiple clients there is always a risk, where one client's action would affect all another client. Since caching of String objects was important from performance reason this risk was avoided by making String class Immutable.

### Why is the String class declared final in Java?

Avoid other classes extend the `java.lang.String` class. Methods of `java.lang.String` can't be overridden. Keep all String object have same behaviors. 

### How does String implement immutability

Most of fields in String are `final` and assign in declaration or in its constructor.

The `java.lang.String` class is final. There no class extends `java.lang.String`, methods of `java.lang.String` can't be overridden, all String object is only `java.lang.String`'s instance, all String objects have the same methods or same behaviors (like equals, length).

### String vs StringBuffer vs StringBuilder?

| **Factor**      | **String**           | **StringBuilder** | **StringBuffer** |
| --------------- | -------------------- | ----------------- | ---------------- |
| *Storage Area*  | Constant String Pool | Heap Area         | Heap Area        |
| *Mutability*    | Immutable            | Mutable           | Mutable          |
| *Thread Safety* | Yes                  | No                | Yes              |
| *Performance*   | Fast                 | More efficient    | Less efficient   |



## III. Core


<br>
<h2><a name="classes-and-objects-t" href="#classes-and-objects-c">Classes and Objects</a></h2>
<br>

### *Object-Oriented Programming*

### Object-Oriented vs Procedure-Oriented?

Object-oriented programming and procedure-oriented programming both are programming paradigm.

**Object-oriented programming** (**OOP**) is a programming paradigm based on the concept of “objects”, which may contain data, in the form of fields, often known as *attributes*.

Object-oriented programming (OOP) is about encapsulating data and behavior into objects. An OOP application will use a collection of objects which knows how to perform certain actions and how to interact with other elements of the application. For example an object could be a person. That person would have a name (that would be a property of the object), and would know how to walk (that would be a method).

**Procedural programming** is a programming paradigm, derived from structured programming, based upon the concept of the *procedure call*. Procedures, also known as routines, subroutines, or functions, simply contain a series of computational steps to be carried out.

Procedural programming (PP), also known as inline programming takes a top-down approach. It is about writing a list of instructions to tell the computer what to do step by step. It relies on procedures or routines.

### What are object-oriented programming major features?

There are three major features in object-oriented programming: encapsulation, inheritance and polymorphism.

- Encapsulation: A class does not allow calling code to access internal object data and permits access through methods only. Encapsulation is a technique that encourages decoupling.
- Inheritance: Using Inheritance, In derived classes we can reuse the code of existing super classes.
- Polymorphism: It means one name many forms. It is further of two types — static and dynamic. Static polymorphism is achieved using method overloading and dynamic polymorphism using method overriding. We can write a code that works on the superclass, and it will work with any subclass type as well.
- Abstraction: Abstract means a concept or an Idea which is not associated with any particular instance. Using abstract class/Interface we express the intent of the class rather than the actual implementation. In a way, one class should not know the inner details of another in order to use it, just knowing the interfaces should be good enough.

### Principles of object-oriented design?

the **SOLID** principles, that is, Single responsibility, Open-closed, Liskov substitution, Interface segregation and Dependency inversion. 

- Single Responsibility Principle (SRP)

The SRP requires that a class should have only a single responsibility. 

For example, If a class `SalesOrder` keeps information about a sales order, and in addition has a method `saveOrder()` that saves the `SaleOrder` in a database, this design will violate the SRP because there will be different types of users of this class and different reasons for making changes to this class.

- Open-Closed Principle (OCP)

The OCP requires that each software entity should be open for extension, but closed for modification. 

For example, Suppose an `OrderValidation` class has a method `validate(Order order)` that is programmed to validate an order based on a set of hard-coded rules. This design violates the OCP because if the rules change, the `OrderValidation` class has to be modified, tested, and compiled. A better design will be to let the `OrderValidation` class contain a collection of `ValidationRule` objects each of which has a `validate``(Order order)` method.

- Liskov Substitution Principle (LSP)

The LSP requires that objects in a program should be replaceable with instances of their subclasses without altering the correctness of that program.

The users must be able to use objects of subclasses via references to base classes without noticing any difference. When using an object through its base class interface, the object of a subclass must not expect the user to obey preconditions that are stronger than those required by the base class.

For example, Suppose a `Rectangle` class has two instance variables `height` and `width`, and a method `setSize(int a, int b)`, which set `height` to `a` and `width` to `b`. Suppose `Square` is a subclass of `Re``ctangle` and it overrides the inherited method by setting both `height` and `width` to `a`. This design will violate LSP. To see this, consider a client uses a reference variable of type `Rectangle` to call the `setSize()` method to assign different values of `a` and `b`, and then immediately verify if the sizes were set correctly or the area is correctly computed. The results will be different if the variable references to a `Rectangle` object than to a `Square` object.

- Interface Segregation Principle (ISP)

The ISP requires that clients should not be forced to depend on interfaces that they do not use.

A better design is to design smaller interfaces for different types of clients.

- Dependency Inversion Principle (DIP)

The DIP requires that high level modules should not depend on low level modules, both should depend on abstraction. Also, abstraction should not depend on details, details should depend on abstractions.

For example, Making an `EBookReader` class to use `PDFBook` class is a violation of DIP because it requires to change the `EBookReader `class to read other types of e-books. A better design is to let `EBookReader ` use an interface `EBook` and let `PDFBook` and other types of e-book classes implement `EBook`. Now adding or changing e-book classes will not require any change to `EBookReader `class.

### Relationships between classes: Generalization vs realization vs composition vs aggregation vs association vs dependency?

- Generalization

Generalization is a relationship of inheritance, is a relationship of "general and special".

Representation:

```
generalization
A ——————▷ B
A is a special B
```

Examples:

```
Animal ◁—————— Cat
       ◁—————— Dog
```

- Realization

Realization is a relationship of implementation, is a relationship of "interface and class". Classes implements interfaces.

Representation:

```
realization
A ------▷ B
A implements B
```

Examples

```
Servie ◁------ Service Implementation
```

```
Print ◁------ Printer
```

- Composition

Composition is a relationship of "part and entity", and part can't be independent exists.

Composition is again a specialized form of Aggregation and we can call this as a “death” relationship. It is a strong type of Aggregation. Child object does not have their lifecycle and if parent object deletes all child object will also be deleted. Let’s take again an example of a relationship between House and rooms. House can contain multiple rooms there is no independent life of room and any room can not belongs to two different houses if we delete the house room will automatically delete.

Representation:

```
composition
A ——————◆ B
A is part of B, and A isn't independent.
```

Examples: 

```
Person ◆—————— Hand
       ◆—————— Leg
       ◆—————— Head
```

```
Folder ◆—————— File
```

- Aggregation

Aggregation is a relationship of "part and entity", and part can be independent exists.

An aggregation is a specialized form of Association where all object has their own lifecycle but there is ownership and child object can not belong to another parent object. Let’s take an example of Department and teacher. A single teacher can not belong to multiple departments, but if we delete the department teacher object will not destroy. 

Representation:

```
aggregation
A ——————◇ B
A is part of B, and A is independent.
```

Examples:

```
Department ◇—————— Teacher
```

```
Car ◇—————— Engine
    ◇—————— Wheel
```

```
Library ◇—————— Book
```

- Association

Association is a relationship of "have".

If two classes in a model need to communicate with each other, there must be a link between them, and that can be represented by an association (connector).

Association is a relationship where all object have their own lifecycle and there is no owner. Let’s take the example of Teacher and Student. Multiple students can associate with a single teacher and a single student can associate with multiple teachers but there is no ownership between the objects and both have their own lifecycle. These relationships can be one to one, one to many, many to one and many to many.

```
association
A ——————> B
A has B

A <——————> B
or
A —————— B
A has B, B has A
```

```
        1..*
Student <———————————— Instructor
        teaches
```

```
        1     n
Student ——————> Course
```

- Dependency

Dependency is a relationship of "use".

```
dependency
A ------> B
A use B
```

Examples:

```
             <<use>>
Web Shopping ------> Payment
```

```
       <<use>>
Person ------> Computer
```

```
       <<use>>
Animal ------> Air
       ------> Water
```

```
            <<use>>
BeanFactory ------> Bean
```



### *Methods*

### Pass by value vs. pass by reference?

pass by value: primitive type variables, wrapper variables, String variables

pass by reference: reference variables (non wrapper/string), array variables

### *Keywords*

### What is final keyword meaning?

- `final` for variables

  When the final keyword is used with a variable then its value can’t be changed once assigned. In case the no value has been assigned to the final variable then using only the class constructor a value can be assigned to it.

- final for methods

  When a method is declared final then it can’t be overridden by the inheriting class.

- final for classes

  When a class is declared as final in Java, it can’t be extended by any subclass class but it can extend other class.

### What is static keyword meaning?

*static* is a non-access modifier in Java which is applicable for the following:

1. blocks
2. variables
3. methods
4. nested classes

static members (variables and methods)

When a member is declared static, it can be accessed before any objects of its class are created, and without reference to any object. 

static blocks

If you need to do computation in order to initialize your **static variables**, you can declare a static block that gets executed exactly once, when the class is first loaded.

static nested classes

A static nested class may be instantiated without instantiating its outer class.

A static class can access only the static members of the outer class. But non-static inner classes can access both static and non-static members of the outer class. 

### What is abstract keyword meaning?

The abstract keyword is used to achieve abstraction in Java. It is a non-access modifier which is used to

- abstract class
- abstract method

Abstract class

- An abstract class can contain constructors and static methods.
- An abstract class can contain the main method and the final method.
- An abstract class can contain overloaded abstract methods.
- We can declare the local inner class as abstract.

Abstract Notice

- An abstract keyword cannot be used with variables and constructors. An abstract keyword can only be used with class and method.
- If a class is abstract, it cannot be instantiated.
- If a method is abstract, it doesn't contain the body.
- We cannot use the abstract keyword with the **final**.
- We cannot declare abstract methods as **private**.
- We cannot declare abstract methods as **static**.
- An abstract method can't be synchronized.

### What are access modifiers in Java?

| **Modifier**                     | **Default** | **Private** | **Protected** | **Public** |
| -------------------------------- | ----------- | ----------- | ------------- | ---------- |
| *Same class*                     | YES         | YES         | YES           | YES        |
| *Same Package subclass*          | YES         | NO          | YES           | YES        |
| *Same Package non-subclass*      | YES         | NO          | YES           | YES        |
| *Different package subclass*     | NO          | NO          | YES           | YES        |
| *Different package non-subclass* | NO          | NO          | NO            | YES        |

### *The java.lang.Object*

### What is equals() and hashcode() method?

`equals()`

```java
public boolean equals(Object obj) {
    return (this == obj);
}
```

According to java documentation of equals() method, any implementation should adhere to following principles.

- For any object x, `x.equals(x)` should return `true`.
- For any two object x and y, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- For multiple objects x, y, and z, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- Multiple invocations of `x.equals(y)` should return same result, unless any of the object properties is modified that is being used in the `equals()` method implementation.
- Object class equals() method implementation returns `true` only when both the references are pointing to same object.

`hashCode()`

Java Object hashCode() is a native method and returns the integer hash code value of the object. The general contract of hashCode() method is:

- Multiple invocations of hashCode() should return the same integer value, unless the object property is modified that is being used in the equals() method.
- An object hash code value can change in multiple executions of the same application.
- If two objects are equal according to equals() method, then their hash code must be same.
- If two objects are unequal according to equals() method, their hash code are not required to be different. Their hash code value may or may-not be equal.

Java hashCode() and equals() method are used in Hash table based implementations in java for storing and retrieving data.

The implementation of equals() and hashCode() should follow these rules.

- If `o1.equals(o2)`, then `o1.hashCode() == o2.hashCode()` should always be `true`.
- If `o1.hashCode() == o2.hashCode` is true, it doesn’t mean that `o1.equals(o2)` will be `true`.

When to override equals() and hashCode() methods

When we override equals() method, it’s almost necessary to override the hashCode() method too so that their contract is not violated by our implementation.

Note that your program will not throw any exceptions if the equals() and hashCode() contract is violated, if you are not planning to use the class as Hash table key, then it will not create any problem.

If you are planning to use a class as Hash table key, then it’s must to override both equals() and hashCode() methods.

What if we don’t implement both hashCode() and equals()?

We have already seen above that if hashCode() is not implemented, we won’t be able to retrieve the value because HashMap use hash code to find the bucket to look for the entry.

If we only use hashCode() and don’t implement equals() then also value will be not retrieved because equals() method will return false.

`Hashtable.java`

```java
public synchronized V get(Object key) {
    Hashtable.Entry<?, ?>[] tab = this.table;
    int hash = key.hashCode();
    int index = (hash & 2147483647) % tab.length;

    for(Hashtable.Entry e = tab[index]; e != null; e = e.next) {
        if (e.hash == hash && e.key.equals(key)) {
            return e.value;
        }
    }
    return null;
}
```



### equals() vs ==?

"=="

- primitive type variables: compare values.
- reference variables: compare reference address.

"equals()"

it only use in reference variables. It is the same with using "==" to compare reference variables,  but `java.lang.String`, and wrapper class override the equals() methods, make the method to compare value of string or wrapper variables.

| type                                    | ==              | equals                     |
| --------------------------------------- | --------------- | -------------------------- |
| string variable                         | compare address | compare value (characters) |
| wrapper variable                        | compare address | compare value              |
| reference variable (non-wrapper/string) | compare address | compare address            |
| primitive type                          | compare value   | NONE                       |

<br>
<h2><a name="inheritance-and-polymorphism-t" href="#inheritance-and-polymorphism-c">Inheritance and Polymorphism</a></h2>

<br>

### What is Polymorphism?

Polymorphism is briefly described as “one interface, many implementations”. Polymorphism is a characteristic of being able to assign a different meaning or usage to something in different contexts – specifically, to allow an entity such as a variable, a function, or an object to have more than one form. There are two types of polymorphism:

1. Compile time polymorphism
2. Run time polymorphism

Compile time polymorphism is method overloading whereas Runtime time polymorphism is done using inheritance and interface.

### Method overriding vs method overloading?

Method overloading

- In Method Overloading, Methods of the same class shares the same name but each method must have a different number of parameters or parameters having different types and order. The methods must have a different signature.
- Method Overloading is to “add” or “extend” more to the method’s behavior.
- It is a compile-time polymorphism.

Method Overriding

- In Method Overriding, the subclass has the same method with the same name and exactly the same number and type of parameters and same return type as a superclass. The methods must have the same signature and same return type.
- Method Overriding is to “Change” existing behavior of the method.
- It is a run time polymorphism.
- It always requires inheritance in Method Overriding.

<br>

<h2><a name="interface-t" href="#interface-c">Interface, Lambada, and Inner Classes</a></h2>
<br>

### Why use nested classes?

Compelling reasons for using nested classes include the following:

- **It is a way of logically grouping classes that are only used in one place**: If a class is useful to only one other class, then it is logical to embed it in that class and keep the two together. Nesting such "helper classes" makes their package more streamlined.
- **It increases encapsulation**: Consider two top-level classes, A and B, where B needs access to members of A that would otherwise be declared `private`. By hiding class B within class A, A's members can be declared private and B can access them. In addition, B itself can be hidden from the outside world.
- **It can lead to more readable and maintainable code**: Nesting small classes within top-level classes places the code closer to where it is used.

<br>

<h2><a name="exceptions-t" href="#exceptions-c">Exceptions, Assertions, and Logging</a></h2>
<br>

### Common Exception class names?

Hierarchy of Exception classes

```
java.lang.Throwable
|----Error
|----Exception
|--------RuntimeException
```

Checked Exceptions

- IOException

  ```
  try {
      new FileReader(new File("/invalid/file/location"));
  } catch (FileNotFoundException e) {
      LOGGER.info("FileNotFoundException caught!");
  }
  ```

- ParseException

  ```
  try {
      new SimpleDateFormat("MM, dd, yyyy").parse("invalid-date");
  } catch (ParseException e) {
      LOGGER.error("ParseException caught!");
  }
  ```

- InterruptedException

  ```
  try {
  	Thread.sleep(1000);
  } catch (InterruptedException e) {
  	LOGGER.error("InterruptedException caught!");
  }
  ```

- SQLExcpetion

Runtime Exceptions

- NullPointerException

  ```
  String strObj = null;
  strObj.equals("Hello World");
  ```

- IndexOutOfBoundsException

  ```
  int[] nums = new int[] {1, 2, 3};
  int numFromNegativeIndex = nums[-1];
  int numFromGreaterIndex = nums[4];
  ```

- NumberFormatException

  ```
  String str = "100ABCD";
  int x = Integer.parseInt(str);
  ```

- ArithmeticException

  ```
  int illegalOperation = 30/0;
  ```

- ClassCastException

  ```
  Animal animal = new Lion();
  Dog tommy = (Dog) animal;
  ```

  

--

<br>
<h2><a name="generic-t" href="#generic-c">Generic Programming</a></h2>
<br>





<br>
<h2><a name="annotations-t" href="#annotations-c">Annotations</a></h2>
<br>





<br>
<h2><a name="reflection-t" href="#reflection-c">Reflection and Proxy</a></h2>
<br>

### What is reflection?

Reflection is an API which is used 

- examine or modify the behavior of methods, classes, interfaces at runtime. 
- It is also possible to instantiate new objects, invoke methods and get/set field values using reflection.

### Proxy Applicability?

- Spring AOP
- Add transaction
- Add permission
- Add logging

<br>

<h2><a name="enum-t" href="#enum-c">Enumeration Types and Wrapper Types</a></h2>
<br>

### Using primitive data types or wrapper classes to declare a variable?

Wrapper classes. Because they have not concrete default values. When variables have not assignment, primitive data types have default values, but wrapper classes are null. Default values of primitive data type may cause error result. When wrapper classes are null, the program may occur `NullPointerException`, but it can't cause error results.

## IV. Advanced



<br>
<h2><a name="io-t" href="#io-c">Input and Output</a></h2>
<br>

### What are I/O Streams? What are IO stream types?

A stream is a way of sequentially accessing a file. 

Input streams and Output streams.

- Input streams read data from source.

- Output streams write data to destination.

Byte streams and character streams

- A byte stream access the file byte by byte. A byte stream is suitable for any kind of file, however not quite appropriate for text files. For example, if the file is using a unicode encoding and a character is represented with two bytes, the byte stream will treat these separately and you will need to do the conversion yourself. Generally, a byte stream is suitable for processing raw data like binary files.

- A character stream will read a file character by character. A character stream needs to be given the file's encoding in order to work properly. Generally, a character stream is useful when we want to process text files. These text files can be processed character by character.

### BIO vs NIO vs AIO?

BIO vs NIO vs AIO

- BIO: Blocking IO is traditional IO. It's synchronous and blocking IO. 

- NIO: New IO is synchronous and non-blocking IO. It uses channels to communicate. In single thread can handle multiple I/O operations. It implemented multiplexing. It has higher performance than BIO.

- AIO: AIO (also called NIO.2) is asynchronous and non-blocking IO. It based event and callback mechanisms.

BIO, NIO, AIO applicable scenario

- The BIO mode is suitable for a small and fixed number of connections. This method has high requirements on server resources. Concurrency is limited to applications. The only choice before JDK1.4, but the program is intuitive and easy to understand.
- The NIO mode is suitable for architectures with a large number of connections and short connections (light operation), such as a chat server. Concurrency is limited to applications, and programming is complicated, and JDK 1.4 supports it.
- The AIO method is used in an architecture with a large number of connections and a long connection (re-operation), such as an album server, which fully invokes the OS to participate in concurrent operations, and the programming is complicated, and JDK7 supports it.

In general, the I/O model can be divided into: synchronous blocking, synchronous non-blocking, asynchronous blocking, asynchronous non-blocking IO.

- synchronous: The user process needs to ask the IO operation status from time to time.
- asynchronous: After the kernel completes the IO operation, it will notify the application.
- blocking: Only after the IO operation is actually completed can the user process run.
- non-blocking: The user process can return to do other things after initiating an IO operation.

### What is serialization?

Serialization is a mechanism of converting the state of an object into a byte stream. Deserialization is the reverse process where the byte stream is used to recreate the actual Java object in memory. This mechanism is used to persist the object.

The byte stream created is platform independent. So, the object serialized on one platform can be deserialized on a different platform.

To make a Java object serializable we implement the **java.io.Serializable** interface.

The ObjectOutputStream class contains **writeObject()** method for serializing an Object.

The ObjectInputStream class contains **readObject()** method for deserializing an object.

Advantages of Serialization

1. To save/persist state of an object.
2. To travel an object across a network.

Note

1. If a parent class has implemented Serializable interface then child class doesn’t need to implement it but vice-versa is not true.
2. Only non-static data members are saved via Serialization process.
3. Static data members and transient data members are not saved via Serialization process. So, if you don’t want to save value of a non-static data member then make it transient.
4. Constructor of object is never called when an object is deserialized.
5. Associated objects must be implementing Serializable interface.

SerialVersionUID

- The Serialization runtime associates a version number with each Serializable class called a SerialVersionUID, which is used during Deserialization to verify that sender and reciever of a serialized object have loaded classes for that object which are compatible with respect to serialization. If the reciever has loaded a class for the object that has different UID than that of corresponding sender’s class, the Deserialization will result in an **InvalidClassException**. A Serializable class can declare its own UID explicitly by declaring a field name.

- It must be static, final and of type long.

- If a serializable class doesn’t explicitly declare a serialVersionUID, then the serialization runtime will calculate a default one for that class based on various aspects of class, as described in Java Object Serialization Specification. However it is strongly recommended that all serializable classes explicitly declare serialVersionUID value, since its computation is highly sensitive to class details that may vary depending on compiler implementations, any change in class or using different id may affect the serialized data.

- It is also recommended to use private modifier for UID since it is not useful as inherited member.

- ```
  private static final long serialversionUID = 1L;
  ```

<br>

<h2><a name="collections-t" href="#collections-c">Collections and Streams</a></h2>
<br>

### Talk about Collection API?

Interfaces of Collection API

```
Collection
|----List
|----Queue
|--------Deque
|------------BlockingDeque
|--------BlockingQueue
|------------TransferQueue
|----Set
|--------AbstractSet
|--------SortedSet
|------------NavigableSet
Map
|----AbstractMap
|----SortedMap
|--------NavigableMap
|----ConcurrentMap
|------------ConcurrentNavigableMap
```

Classes of Collection API

List

- Basic List
  - ArrayList
  - LinkedList
- Thread-safe List
  - Vector
- Concurrent List
  - CopyOnWriteArrayList

Stack/Queue

- Basic Stack/Queue
  - Stack
  - ArrayDeque
  - PriorityQueue
- Blocking Queue (wait for the queue to become non-empty or available, design for producer-consumer queues)
  - ArrayBlockingQueue
  - LinkedBlocingQueue
  - PriorityBlockingQueue
  - DelayQueue
  - SynchronousQueue
  - LinkedBlockingDeque
  - LinkedTransferQueue
- Concurrent Stack/Queue
  - ConcurrentLinkedQeque
  - ConcurrentLinkedDeque

Set

- Basic Set
  - HashSet
  - LinkedHashSet
  - TreeSet
- Concurrent Set
  - CopyOnWriteArraySet
  - ConcurrentSkipListSet

Map

- Basic Map
  - HashMap
  - LinkedHashMap
  - EnumMap
  - IdentityHashMap
  - WeakHashMap
  - TreeMap
- Thread-safe Map
  - Hashtable
- Concurrent Map
  - ConcurrentHashMap
  - ConcurrentSkipListMap

TreeXxx (TreeSet, TreeMap)

- Sorted by key with natural ordering or by a comparator object.
- O(n) time cost for the basic operations (`add`, `remove` and `contains`).

ConcurrentXxx (ConcurrentLinkedQeque, ConcurrentHashMap)

- They have more concurrency.
- write operations (put, putAll, remove)
- read operations (get, size, contains, containsKey, forEach, keySet, keys, values) generally do not block.

CopyOnWriteArrayXxx (CopyOnWriteArrayList, CopyOnWriteArraySet)

- All write operations (like add, addAll, set, remove) are synchronized and using a copy array to write, and then update object filed `transient volatile Object[] array`.
- All read operations (like get, contains, forEach, iterator, size) are not synchronized and directly using the `transient volatile Object[] array` to read.
- Summary
  - The all operations are thread-safe. 
  - Write operations are very expensive, and they need both synchronized lock and a copy array. But read operations have no lock and are very efficient and fast. So you should only use this read when you are doing upwards of 90+% reads.

ConcurrentSkipListXxx (ConcurrentSkipListSet, ConcurrentSkipListMap)

- ...

### HashMap vs Hashtable?

The `HashMap` class is roughly equivalent to `Hashtable`, except that it is unsynchronized and permits nulls.

### Why HashMap allows null key but Hashtable does not?

Because hash-function-based Map need to use key object hashCode() method to get its hashCode and find the value from map by it key's hashCode. But if key is null, you can't get the key hashCode. So essentially any key of a map is can't be null.

But in HashMap, it allows null as a key, because HashMap convert the null to a special value "0" as a key.

```java
public class HashMap{
    ...
	static final int hash(Object key) {
        int h;
        return (key == null) ? 0 : (h = key.hashCode()) ^ (h >>> 16);
    }
    ...
}
```

### Array vs ArrayList?

Array is fixed length, ArrayList is variable length.

Array stores primitive type data and objects, ArrayList only store objects.

Array methods number is less than ArrayList. Array is built-in, it has no class file.

### How HashMap works?

HashMap is store key-value entry data structure. It is based hash function to locate the key-value entry in map.

A HashMap is a LinkedList array. To get entry or put a entry:

- Firstly, to find the index of the array by its key's hashCode. Any element is LinkedList in the array, because multiple keys may have some hashCode, and these entries that have the same key will store in a LinkedList.
- Then, find really entry by comparing the specified key with every keys in the LinkedList.

Since Java 1.8, the HashMap has some improvement. When elements number of the LinkedList over 8, the LinkedList will convert to Red-Black Tree, and the time cost of to find really entry that have the same key's hashCode is from O(n) to O(logn) 

<br>

<h2><a name="concurrency-t" href="#concurrency-c">Concurrency</a></h2>
<br>

### *Processes and Threads*

### Process vs Thread?

|               | Process                                                      | Thread                                                       |
| ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Definition    | a basic unit of program running and resources assignment. A process at least contains one thread. | a basic unit of execution.                                   |
| Memory        | has independent memory space.                                | threads use process resources. has independent and share space. |
| Communication | Inter-process communication (like TCP)                       | directly communicate with other threads of its process.      |
| Control       | Process is controlled by OS                                  | Threads are controlled by process.                           |

### What is daemon thread?

Daemon thread is a low priority thread (in context of JVM) that runs in background to perform tasks such as garbage collection (gc) etc., they do not prevent the JVM from exiting (even if the daemon thread itself is running) when all the user threads (non-daemon threads) finish their execution. JVM terminates itself when all user threads (non-daemon threads) finish their execution, JVM does not care whether Daemon thread is running or not, if JVM finds running daemon thread (upon completion of user threads), it terminates the thread and after that shutdown itself.

Properties of Daemon threads:

- A newly created thread inherits the daemon status of its parent. That’s the reason all threads created inside main method (child threads of main thread) are non-daemon by default, because main thread is non-daemon. However you can make a user thread to Daemon by using **setDaemon() method** of thread class.
- Methods of Thread class that are related to Daemon threads: `void setDaemon(boolean status)`, `boolean isDaemon()`.
- setDaemon() method can only be called before starting the thread.

### *Thread Objects*

### Creating Thread classes ways?

Thread classes mean this class code can run in a new thread.

- extends Thread
- implements Runnable
- implements Callable. (construct a FutureTask object with a callable object, futureTask submit to a thread pool object)

### Creating Thread ways?

- Call Thread object start() method.
- Create thread pool object such as `ThreadPoolExecutor` object. Generally using the utility class `Executors` to create a thread pool e.g. `Executors.newSingleThreadExecutor()`.

Hierarchy of Thread

```
I-Runnable
|----Thread
```

Hierarchy of Executor

```
(I)Executor
|----(I)ExecutorService
|--------(I)ScheduledExecutorService
|--------(A)AbstractExecutorService
|------------ForkJoinPool
|------------ThreadPoolExecutor
|----------------ScheduledThreadPoolExecutor
Executors
```

### What are Thread status?

- New. A thread that has not yet started.
- Runnable. A thread executing in the Java virtual machine.
- Blocked. A thread that is blocked waiting for a monitor lock.
- Waiting. A thread that is waiting indefinitely for another thread to perform a particular action.
- Timed waiting. A thread that is waiting for another thread to perform an action for up to a specified waiting time.
- Terminated. A thread that has exited.

![Thread status](java-se-thread-status.jpg)

### sleep() vs wait()?

**sleep()** is a method which is used to pause the process for few seconds or the time we want to.

**wait()** method, thread goes in waiting state and it won’t come back automatically until we call the `notify()` or `notifyAll()`.

The major difference is that `wait()` releases the lock or monitor while `sleep()` doesn’t releases the lock or monitor while waiting. `wait()` is used for inter-thread communication while `sleep()` is used to introduce pause on execution, generally.

|              | sleep()                           | wait()                                                       |
| ------------ | --------------------------------- | ------------------------------------------------------------ |
| Definition   | just pause process for some times | pause process, enter "waiting status", wait for notification |
| Lock         | doesn't release lock              | release lock                                                 |
| Precondition | no limit                          | only call it in a synchronized block                         |

### *Synchronization and Thread-Safe*

### How thread-safe works?

Thread-safe problems are: 

- Thread Interference: Errors are introduced when multiple threads access shared data.
- Memory Consistency Errors: Errors that result form inconsistent views of shared memory. Memory consistency errors occur when different threads have inconsistent views of what should be the same data. When other thread update value of a variable, your current thread still read old value of the variable.

Solving thread interference:

- Exclusive locks
  - Implicit locks. Synchronized blocks or methods.
  - Explicit locks. ReentrantLock.

Solving memory consistency errors: 

- create happens-before relationships between multiple threads
  - Monitor lock
  - Volatile variable 

### How synchronized works or exclusive lock works?



### *Liveness Problems*

### Deadlock vs starvation vs livelock? 

- Deadlock: Deadlock describes a situation where two or more threads are blocked forever, waiting for each other.
- Starvation describes a situation where a thread is unable to gain regular access to shared resources and is unable to make progress.
- Livelock is a situation threads simply too busy responding to each other and unable to make further progress.

### How to avoid deadlock?

Although it is not completely possible to avoid deadlock condition, but we can follow certain measures or pointers to avoid them:

- **Avoid Nested Locks** – You must avoid giving locks to multiple threads, this is the main reason for a deadlock condition. It normally happens when you give locks to multiple threads.
- **Avoid Unnecessary Locks** – The locks should be given to the important threads. Giving locks to the unnecessary threads that cause the deadlock condition.
- **Using Thread Join** – A deadlock usually happens when one thread is waiting for the other to finish. In this case, we can use Thread.join with a maximum time that a thread will take.

### *High Concurrency*

### synchronized vs ReentrantLock?

ReentrantLock is a reentrant mutual exclusion Lock with the same basic behavior and semantics as the implicit monitor lock accessed using synchronized methods and statements, but with extended capabilities.

the **main difference between synchronized and ReentrantLock** is the ability to trying for lock interruptibly, and with a timeout. The thread[ ](http://javarevisited.blogspot.com/2012/01/difference-thread-vs-runnable-interface.html)doesn’t need to block infinitely, which was the case with synchronized.

- **Fairness** with ReentrantLock(boolean fair) and avoid startvation. You can make ReentrantLock fair by specifying fairness property while creating an instance of ReentrantLock. When set true, under contention, locks favor granting access to the longest-waiting thread.  1)Programs using fair locks accessed by many threads may display lower overall throughput (i.e., are slower; often much slower) than those using the default setting, but have smaller variances in times to obtain locks and guarantee lack of starvation. 2)Note however, that fairness of locks does not guarantee fairness of thread scheduling. Thus, one of many threads using a fair lock may obtain it multiple times in succession while other active threads are not progressing and not currently holding the lock. 3)Also note that the untimed tryLock() method does not honor the fairness setting. 
- **Attempt to acquire a lock** with tryLock() and avoid deadlock. Lock objects work very much like the implicit locks used by synchronized code. The biggest advantage of `Lock` objects over implicit locks is their ability to back out of an attempt to acquire a lock. The `tryLock` method backs out if the lock is not available immediately or before a timeout expires. We can use Lock objects to solve the deadlock problem. First we use `Lock.tryLock()` method to acquire all locks we needed, if fail to acquire, then unlock all acquired locks, else we can acquire all locks and without deadlock problem.
- **Lock interruptibly** with lockInterruptibly(). Acquires the lock unless the current thread is interrupted.
- **Non-block Structured Locking.** 1)Synchronized keyword forces all lock acquisitions and releases to occur in a block-structured way which means when multiple locks are acquired they must be released in the opposite order, and all locks must be released in the same scope in which they were acquired. 2)ReentrantLock provides more flexibility, it allows a lock to be acquired and released in different scopes and allowing multiple locks to be acquired and released in any order.
- More convenient API methods. getHoldCount(), getWaitingThreads(Condition condition), isHeldByCurrentThread(), isLocked()
- Usage. synchronized: It acquiring and releasing lock is done implicitly. ReentrantLock: It acquires and releases lock is done by using lock() and unlock() methods.

### Volatile variables vs atomic variables vs immutable objects?

Volatile variables

- Volatile keyword is used to modify the value of a variable by different threads. It is also used to make classes thread safe. It means that multiple threads can use a method and instance of the classes at the same time without any problem. The volatile keyword can be used either with primitive type or objects.
- The volatile keyword does not cache the value of the variable and always read the variable from the main memory. The volatile keyword cannot be used with classes or methods. However, it is used with variables. It also guarantees visibility and ordering. It prevents the compiler from the reordering of code.

Atomic variables

- The `java.util.concurrent.atomic` package defines classes that support atomic operations on single variable. All classes have `get` and `set` methods that work like reads and writes on volatile variables. A `set` has a happens-before relationship with any subsequent `get` on the same variable. The atomic `compareAndSet` method also has these **memory consistency** feature, as do the simple **atomic arithmetic** methods that apply to integer atomic variables.
- `addAndGet(int delta)`, `decrementAndGet()`, `get()`, `set(int newValue)`

immutable objects

- Don’t provide “setter” methods. Methods that modify fields or objects referred to by fields.
- Make all fields `final` and `private`.
- Don’t allow subclass to override methods. The simplest way to do this is to declare the class as `final`. A more sophisticated approach is to make the constructor private and construct instances in factory methods in this class.
- If the instance fields include references to mutable objects, don’t allow those objects to be change. Don’t provide methods that modify the mutable objects. Don’t share references to the mutable objects.

### *Concurrency Others*

### What is ThreadLocal?

java.lang.ThreadLocal class provides thread-local variables where each thread accesses its own, independent copy of the variable. 

ThreadLocal object only store single object.

To create a ThreadLocal variable:

```
private ThreadLocal<T> myThrLocalVariable = new ThreadLocal<T>();
```

ThreadLocal methods:

- T get()
- void set(T value)

### When should I use a ThreadLocal variable?

One of the common use is when we have a object that is not thread-safe and not want to synchronize on the object, we may use ThreadLocal to have each thread its own instance of the object.

The well known example for ThreadLocal is SimpleDateFormat which is not thread-safe and we may use ThreadLocal to have every thread its own instance of SimpleDateFormat class.

<br>

<h2><a name="network-t" href="#network-c">Network Programming</a></h2>
<br>



<br>
<h2><a name="java-security-t" href="#java-security-c">Java Security</a></h2>

<br>



<br>
<h2><a name="jmx-t" href="#jmx-c">JMX, JNDI, JAXP, RMI</a></h2>
<br>


<br>
<h2><a name="native-methods-t" href="#native-methods-c">Native Methods</a></h2>
<br>

## V. Utility

## References

[1] [100+ Java Interview Questions You Must Prepare In 2020](https://www.edureka.co/blog/interview-questions/java-interview-questions/#Jdk-Jre-and-Jvm)

[2] [Java面试题及答案整理（2020最新版）- 模块一~模块五](https://zhuanlan.zhihu.com/p/64147696?utm_source=com.ideashower.readitlater.pro&utm_medium=social&utm_oi=69586464538624)

Character Encoding

- [Guide to Character Encoding](https://www.baeldung.com/java-char-encoding)
- [Character Sets](https://www.iana.org/assignments/character-sets/character-sets.xml)
- [Unicode - Wikipedia](https://en.wikipedia.org/wiki/Unicode)

String

- [Why String is Immutable or Final in Java](https://javarevisited.blogspot.com/2010/10/why-string-is-immutable-or-final-in-java.html)

Object-Oriented Programming

- [Functional vs Object-Oriented vs Procedural Programming](https://medium.com/@LiliOuakninFelsen/functional-vs-object-oriented-vs-procedural-programming-a3d4585557f3)
- [What are four basic principles of Object Oriented Programming?](https://medium.com/@cancerian0684/what-are-four-basic-principles-of-object-oriented-programming-645af8b43727)
- [Principles of Object-Oriented Design](http://www.cs.utsa.edu/~cs3443/notes/designPrinciples/designPrinciples.html)
- [UML各种图总结](https://www.cnblogs.com/jiangds/p/6596595.html)

Object

- [Guide to hashCode() in Java](https://www.baeldung.com/java-hashcode)
- [Java equals() and hashCode()](https://www.journaldev.com/21095/java-equals-hashcode)

IO Streams

- [The difference between BIO and NIO, AIO](https://www.programmersought.com/article/10551850908/)

Concurrency

- [Difference between sleep() and wait() in Java](https://howtodoinjava.com/java/multi-threading/sleep-vs-wait/)
- [How To Handle Deadlock In Java?](https://www.edureka.co/blog/deadlock-in-java/)
- [Java ThreadLocal](https://www.javapedia.net/Java-ThreadLocal)

--END--