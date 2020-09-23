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
    - [x] [Q: Java Version History?](#Q: Java Version History?)
    - [x] [Q: Java Version Major Changes?](#Q: Java Version Major Changes?)
- II. Basics
  - <a name="variables-and-types-c" href="#variables-and-types-t">Variables and Types</a>
    - [x] [What are the primitive data types in Java? What are their value ranges?](#What are the primitive data types in Java? What are their value ranges?)
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
    - Class and Object
      - [ ] Q: Object Creation Ways?
      - [ ] Q: the process of object creation?
    - Methods
      - [x] [Pass by value vs. pass by reference?](#Pass by value vs. pass by reference?)
    - Keywords
      - [x] [What is final keyword meaning?](#What is final keyword meaning?)
      - [x] [What is static keyword meaning?](#What is static keyword meaning?)
      - [x] [What is abstract keyword meaning?](#What is abstract keyword meaning?)
      - [x] [What are access modifiers in Java?](#What are access modifiers in Java?) (public, protected, private)
    - The java.lang.Object
      - [x] [What is equals() and hashcode() method?](#What is equals() and hashcode() method?)
      - [x] [equals() vs ==?](#equals() vs ==?)
  - <a name="inheritance-and-polymorphism-c" href="#inheritance-and-polymorphism-t">Inheritance and Polymorphism</a>
    - [x] [What is Polymorphism?](#What is Polymorphism?)
    - [x] [Method overriding vs method overloading?](#Method overriding vs method overloading?)
  - <a name="interface-c" href="#interface-t">Interface, Lambada, and Inner Classes</a>
    - [x] [Why use nested classes?](#Why use nested classes?)
    - [x] [Q: Static Inner Class vs Inner Class?](#Q: Static Inner Class vs Inner Class?)
  - <a name="exceptions-c" href="#exceptions-t">Exceptions, Assertions, and Logging</a>
    - [x] [Common Exception class names?](#Common Exception class names?)
    - [ ] How to handle exception? Right ways of handling exception.
    - [ ] Return statements in try-catch-finally?
  - <a name="generic-c" href="#generic-t">Generic Programming</a>
  - <a name="annotations-c" href="#annotations-t">Annotations</a>
  - <a name="reflection-c" href="#reflection-t">Reflection and Proxy</a>
    - [x] [What is reflection?](#What is reflection?)
    - [x] [Proxy Applicability?](#Proxy Applicability?)
  - <a name="enum-c" href="#enum-t">Enumeration Types and Wrapper Types</a>
    - [ ] What are wrapper classes? Why do we need it?
    - [ ] What are boxing, unboxing, and autoboxing? What are wrapper classes caches?
    - [x] [Using primitive data types or wrapper classes to declare a variable?](#Using primitive data types or wrapper classes to declare a variable?)
- IV. Advanced
  - <a name="io-c" href="#io-t">Input and Output</a>
    - [x] [What are I/O Streams? What are IO stream types?](#What are I/O Streams? What are IO stream types?)
    - [x] [BIO vs NIO vs AIO?](#BIO vs NIO vs AIO?)
    - [x] [What is serialization?](#What is serialization?)
    - [x] [What is transient keyword meaning?](#What is transient keyword meaning?)
  - <a name="collections-c" href="#collections-t">Collections and Streams</a>
    - Container API
      - [x] [Talk about Collection API?](#Talk about Collection API?)
      - [x] [HashMap vs Hashtable?](#HashMap vs Hashtable?)
      - [x] [Why HashMap allows null key but Hashtable does not?](#Why HashMap allows null key but Hashtable does not?)
      - [x] [Array vs ArrayList?](#Array vs ArrayList?)
    - Container Implementation Principles
      - [x] [How HashMap works?](#How HashMap works?) (HashMap implementation?)
      - How Concurrent Collection Classes Work?
    - Container Applicability
      - (How to choice data structure for different usage scenario?)
    - Iterator
      - [x] [Fail fast and fail safe iterators?](#Fail fast and fail safe iterators?)
  - <a name="concurrency-c" href="#concurrency-t">Concurrency</a>
    - Processes and Threads
      - [x] [Process vs Thread?](#Process vs Thread?)
      - [x] [What is daemon thread?](#What is daemon thread?)
    - Thread Objects
      - [x] [Creating Thread classes ways?](#Creating Thread classes ways?)
      - [x] [Starting Thread ways?](#Starting Thread ways?)
      - [x] [What are Thread status?](#What are Thread status?)
      - [x] [sleep() vs wait()?](#sleep() vs wait()?)
      - [ ] sleep(), join(), yield() of Thread class
      - wait(), notify(), notifyAll() of Object class
      - FutureTask and ForkJoinTask
    - Synchronization and Thread-Safe
      - [x] [How thread-safe works?](#How thread-safe works?)
      - [ ] How synchronized works or exclusive lock works?
    - Liveness Problems
      - [x] [Deadlock vs starvation vs livelock?](#Deadlock vs starvation vs livelock?) 
      - [x] [How to avoid deadlock?](#How to avoid deadlock?)
      - [ ] Deadlock code examples
      - [ ] Livelock code examples
    - Guarded Blocks
    - Advanced Concurrency Objects
      - Lock
        - [x] [synchronized vs ReentrantLock?](#synchronized vs ReentrantLock?)
        - [ ] ReentrantLock Implementation Principles
      - Executors and Thread Pools
        - Thread Pool Types?
      - Concurrent Collections
      - Atomic Variables
        - [x] [Volatile variables vs atomic variables vs immutable objects?](#Volatile variables vs atomic variables vs immutable objects?)
      - ThreadLocal and ThreadLocalRandom
        - [x] [What is ThreadLocal?](#What is ThreadLocal?)
        - [x] [When should I use a ThreadLocal variable?](#When should I use a ThreadLocal variable?)
    - Concurrency Others
      - java.util.concurrent.CountDownLatch
      - java.util.concurrent.CyclicBarriers
      - java.util.concurrent.Semaphore
      - java.util.concurrent.Exchanger
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

|               | **JDK**                                                      | **JRE**                                                      | **JVM**                                                      |
| ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| What is it    | It stands for Java Development Kit.                          | It stands for Java Runtime Environment.                      | It stands for Java Virtual Machine.                          |
| Details       | It is the tool necessary to compile, document and package Java programs. | JRE refers to a runtime environment in which Java bytecode can be executed. | It is an abstract machine. It is a specification that provides a run-time environment in which Java bytecode can be executed. |
| Relationships | It contains JRE + development tools.                         | It’s an implementation of the JVM which physically exists.   | JVM follows three notations: Specification, **Implementation,** and **Runtime Instance**. |

JDK:

- development kit (such as javac, java, javap, jconsole)
- document
- java runtime environment (JRE).

JRE:

- JVM Implementation
- Standard libraries

**If you only need to run a java application, you can just install JRE.**

<br>

<h2><a name="java-features-t" href="#java-features-c">Java Features</a></h2>

<br>

### How Java cross platforms(Write once, run anywhere)?

Java is called platform independent because of its byte codes which can run on any system irrespective of its underlying operating system.

Same byte codes can run on any JVM, Different JVM can run on different operating system irrespective.

Byte codes + JVM + OS = Cross Platforms

### Why Java is not 100% Object-oriented?

Eight primitive data types such as boolean, byte, int which are not objects.

<br>

<h2><a name="java-history-t" href="#java-history-c">Java History</a></h2>
<br>

### Q: Java Version History?

|         Version          |  Release date  | End of Free Public Updates[[1\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-auto9-1)[[6\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-6) | Extended Support Until |
| :----------------------: | :------------: | :----------------------------------------------------------: | :--------------------: |
|         JDK Beta         |      1995      |                              ?                               |           ?            |
|         JDK 1.0          |  January 1996  |                              ?                               |           ?            |
|         JDK 1.1          | February 1997  |                              ?                               |           ?            |
|         J2SE 1.2         | December 1998  |                              ?                               |           ?            |
|         J2SE 1.3         |    May 2000    |                              ?                               |           ?            |
|         J2SE 1.4         | February 2002  |                         October 2008                         |     February 2013      |
|         J2SE 5.0         | September 2004 |                        November 2009                         |       April 2015       |
|        Java SE 6         | December 2006  |                          April 2013                          |     December 2018      |
|        Java SE 7         |   July 2011    |                          April 2015                          |       July 2022        |
|     Java SE 8 (LTS)      |   March 2014   | **January 2019 for Oracle (commercial)** December 2020 for Oracle (personal use) At least May 2026 for AdoptOpenJDK At least May 2026[[7\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-Corretto2020-7) for Amazon Corretto |     December 2030      |
|        Java SE 9         | September 2017 |                    March 2018 for OpenJDK                    |          N/A           |
|        Java SE 10        |   March 2018   |                  September 2018 for OpenJDK                  |          N/A           |
|     Java SE 11 (LTS)     | September 2018 | At least September 2027[[7\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-Corretto2020-7) for Amazon Corretto October 2024 for AdoptOpenJDK |     September 2026     |
|        Java SE 12        |   March 2019   |                  September 2019 for OpenJDK                  |          N/A           |
|        Java SE 13        | September 2019 |                    March 2020 for OpenJDK                    |          N/A           |
| **Java SE 14** (current) |   March 2020   |                  September 2020 for OpenJDK                  |          N/A           |
|        Java SE 15        | September 2020 |                    March 2021 for OpenJDK                    |          N/A           |
|        Java SE 16        |   March 2021   |                  September 2021 for OpenJDK                  |          N/A           |
|     Java SE 17 (LTS)     | September 2021 |                             TBA                              |          TBA           |

### Q: Java Version Major Changes?

JDK 1.0

- The first version was released on January 23, 1996.[[10\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-pr10-10)[[11\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-JavaHistory-11) The first stable version, JDK 1.0.2, is called Java 1.

JDK 1.1

- an extensive retooling of the [AWT](https://en.wikipedia.org/wiki/Abstract_Window_Toolkit) event model
- [inner classes](https://en.wikipedia.org/wiki/Inner_class) added to the language
- [JavaBeans](https://en.wikipedia.org/wiki/JavaBeans)
- [JDBC](https://en.wikipedia.org/wiki/Java_Database_Connectivity)
- [RMI](https://en.wikipedia.org/wiki/Java_remote_method_invocation)
- [reflection](https://en.wikipedia.org/wiki/Reflection_(computer_science)) which supported Introspection only, no modification at runtime was possible. (The ability to modify objects reflectively was added in J2SE 1.2, by introducing the [AccessibleObject](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/reflect/AccessibleObject.html) class and its subclasses such as the [Field](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/reflect/Field.html) class.)
- [JIT (Just In Time) compiler](https://en.wikipedia.org/wiki/Just-in-time_compilation) on Microsoft Windows platforms, produced for JavaSoft by Symantec
- **[Internationalization](https://en.wikipedia.org/wiki/Internationalization_and_localization) and [Unicode](https://en.wikipedia.org/wiki/Unicode) support originating from [Taligent](https://en.wikipedia.org/wiki/Taligent)[[13\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-taligentau-13)**

J2SE 1.2

Codename **Playground**

- `strictfp` keyword
- the [Swing](https://en.wikipedia.org/wiki/Swing_(Java)) graphical API was integrated into the core classes
- Sun's JVM was equipped with a [JIT compiler](https://en.wikipedia.org/wiki/Just-in-time_compilation) for the first time
- [Java plug-in](https://en.wikipedia.org/wiki/Java_plug-in)
- [Java IDL](https://en.wikipedia.org/wiki/Java_IDL), an [IDL](https://en.wikipedia.org/wiki/Interface_description_language) implementation for [CORBA](https://en.wikipedia.org/wiki/Common_Object_Request_Broker_Architecture) interoperability
- [Collections](https://en.wikipedia.org/wiki/Java_collections_framework) framework

J2SE 1.3

Codename **Kestrel**

- [HotSpot](https://en.wikipedia.org/wiki/HotSpot) JVM included (the HotSpot JVM was first released in April 1999 for the J2SE 1.2 JVM)
- [RMI](https://en.wikipedia.org/wiki/Java_remote_method_invocation) was modified to support optional compatibility with [CORBA](https://en.wikipedia.org/wiki/CORBA)
- [Java Naming and Directory Interface](https://en.wikipedia.org/wiki/Java_Naming_and_Directory_Interface) (JNDI) included in core libraries (previously available as an extension)
- [Java Platform Debugger Architecture](https://en.wikipedia.org/wiki/Java_Platform_Debugger_Architecture) (JPDA)
- JavaSound
- Synthetic proxy classes

J2SE 1.4

Codename **Merlin**

- Language changes
  - `assert` keyword (specified in [JSR 41](https://web.archive.org/web/20080616233205/http://www.jcp.org/en/jsr/detail?id=41))
- Library improvements
  - [Regular expressions](https://en.wikipedia.org/wiki/Regular_expressions) modeled after [Perl](https://en.wikipedia.org/wiki/Perl) regular expressions
  - [Exception chaining](https://en.wikipedia.org/wiki/Exception_chaining) allows an exception to encapsulate original lower-level exception
  - Internet Protocol version 6 ([IPv6](https://en.wikipedia.org/wiki/IPv6)) support
  - [Non-blocking I/O (Java)](https://en.wikipedia.org/wiki/Non-blocking_IO) (named NIO) (specified in [JSR 51](http://www.jcp.org/en/jsr/detail?id=51))
  - Logging API (specified in [JSR 47](http://www.jcp.org/en/jsr/detail?id=47))
  - Image I/O API for reading and writing images in formats like [JPEG](https://en.wikipedia.org/wiki/JPEG) and [PNG](https://en.wikipedia.org/wiki/Portable_Network_Graphics)
  - Integrated [XML](https://en.wikipedia.org/wiki/XML) parser and [XSLT](https://en.wikipedia.org/wiki/XSLT) processor ([JAXP](https://en.wikipedia.org/wiki/JAXP)) (specified in [JSR 5](http://www.jcp.org/en/jsr/detail?id=5) and [JSR 63](http://www.jcp.org/en/jsr/detail?id=63))
  - Integrated security and cryptography extensions ([JCE](https://en.wikipedia.org/wiki/Java_Cryptography_Extension), [JSSE](https://en.wikipedia.org/wiki/JSSE), [JAAS](https://en.wikipedia.org/wiki/Java_Authentication_and_Authorization_Service))
  - [Java Web Start](https://en.wikipedia.org/wiki/Java_Web_Start) included (Java Web Start was first released in March 2001 for J2SE 1.3) (specified in [JSR 56](http://www.jcp.org/en/jsr/detail?id=56))
  - Preferences API (`java.util.prefs`)

J2SE 5.0

Codename **Tiger**

Tiger added a number of significant new language features:[[21\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-pr15-21)[[22\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-ch15-22)

- [Generics](https://en.wikipedia.org/wiki/Generics_in_Java): provides compile-time (static) [type safety](https://en.wikipedia.org/wiki/Type_safety) for collections and eliminates the need for most [typecasts (type conversion)](https://en.wikipedia.org/wiki/Type_conversion) (specified by [JSR 14](http://www.jcp.org/en/jsr/detail?id=14))
- [Metadata](https://en.wikipedia.org/wiki/Metadata_(computing)): also called [annotations](https://en.wikipedia.org/wiki/Java_annotation); allows language constructs such as classes and methods to be tagged with additional data, which can then be processed by metadata-aware utilities (specified by [JSR 175](http://www.jcp.org/en/jsr/detail?id=175))
- [Autoboxing](https://en.wikipedia.org/wiki/Autoboxing)/unboxing: automatic conversions between [primitive types](https://en.wikipedia.org/wiki/Primitive_type) (such as `int`) and [primitive wrapper classes](https://en.wikipedia.org/wiki/Primitive_wrapper_class) (such as `Integer`) (specified by [JSR 201](http://www.jcp.org/en/jsr/detail?id=201))
- [Enumerations](https://en.wikipedia.org/wiki/Enumeration_(programming)): the `enum` keyword creates a [typesafe](https://en.wikipedia.org/wiki/Type_safety), ordered list of values (such as `Day.MONDAY`, `Day.TUESDAY`, etc.); previously this could only be achieved by non-typesafe constant integers or manually constructed classes (typesafe enum pattern) (specified by [JSR 201](http://www.jcp.org/en/jsr/detail?id=201))
- [Varargs](https://en.wikipedia.org/wiki/Java_syntax#Varargs): the last parameter of a method can now be declared using a type name followed by three dots (e.g. `void drawtext(String... lines)`); in the calling code any number of parameters of that type can be used and they are then placed in an array to be passed to the method, or alternatively the calling code can pass an array of that type
- Enhanced `for each` loop: the `for` loop syntax is extended with special syntax for iterating over each member of either an array or any `Iterable`, such as the standard `Collection` classes (specified by [JSR 201](http://www.jcp.org/en/jsr/detail?id=201))
- Improved semantics of execution for multi-threaded Java programs; the new [Java memory model](https://en.wikipedia.org/wiki/Java_memory_model) addresses issues of complexity, effectiveness, and performance of previous specifications[[23\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-jsr-133-23)
- [Static imports](https://en.wikipedia.org/wiki/Static_import)

There were also the following improvements to the standard libraries:

- Automatic [stub](https://en.wikipedia.org/wiki/Method_stub) generation for [RMI](https://en.wikipedia.org/wiki/Java_remote_method_invocation) objects
- [Swing](https://en.wikipedia.org/wiki/Swing_(Java)): New [skinnable](https://en.wikipedia.org/wiki/Skin_(computing)) [look and feel](https://en.wikipedia.org/wiki/Look_and_feel#In_widget_toolkits), called [synth](https://en.wikipedia.org/wiki/Synth_Look_and_Feel)
- The [concurrency utilities](https://java.sun.com/j2se/1.5.0/docs/guide/concurrency/overview.html) in package [`java.util.concurrent`](https://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/package-summary.html)[[24\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-24)
- Scanner class for parsing data from various input streams and buffers

Java SE 6

Codename **Mustang**

- Support for older Win9x versions dropped; unofficially, Java 6 Update 7 was the last release of Java shown to work on these versions of Windows.[*[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)*] This is believed[*[by whom?](https://en.wikipedia.org/wiki/Wikipedia:Manual_of_Style/Words_to_watch#Unsupported_attributions)*] to be due to the major changes in Update 10.
- Scripting Language Support ([JSR 223](https://en.wikipedia.org/wiki/JSR_223)): Generic API for tight integration with scripting languages, and built-in [Mozilla](https://en.wikipedia.org/wiki/Mozilla) [JavaScript](https://en.wikipedia.org/wiki/JavaScript) [Rhino](https://en.wikipedia.org/wiki/Rhino_(JavaScript_engine)) integration.
- Dramatic performance improvements for the core platform,[[50\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-lobby-50)[[51\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-weblog-51) and [Swing](https://en.wikipedia.org/wiki/Swing_(Java)).
- Improved Web Service support through [JAX-WS](https://en.wikipedia.org/wiki/JAX-WS) ([JSR 224](https://en.wikipedia.org/wiki/JSR_224)).
- [JDBC](https://en.wikipedia.org/wiki/Java_Database_Connectivity) 4.0 support ([JSR 221](https://en.wikipedia.org/wiki/JSR_221)).
- Java Compiler API ([JSR 199](https://en.wikipedia.org/wiki/JSR_199)): an API allowing a Java program to select and invoke a Java Compiler programmatically.
- Upgrade of [JAXB](https://en.wikipedia.org/wiki/JAXB) to version 2.0: Including integration of a [StAX](https://en.wikipedia.org/wiki/StAX) parser.
- Support for pluggable [annotations](https://en.wikipedia.org/wiki/Java_annotation) ([JSR 269](https://en.wikipedia.org/w/index.php?title=JSR_269&action=edit&redlink=1)).[[52\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-52)
- Many [GUI](https://en.wikipedia.org/wiki/Graphical_user_interface) improvements, such as integration of [SwingWorker](https://en.wikipedia.org/wiki/SwingWorker) in the API, table sorting and filtering, and true Swing [double-buffering](https://en.wikipedia.org/wiki/Multiple_buffering) (eliminating the gray-area effect).
- [JVM](https://en.wikipedia.org/wiki/Java_virtual_machine) improvements include: [synchronization](https://en.wikipedia.org/wiki/Data_synchronization) and [compiler](https://en.wikipedia.org/wiki/Compiler) performance optimizations, new algorithms and upgrades to existing [garbage collection algorithms](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)), and application start-up performance.

Java SE 7

codename **Dolphin**

- [JVM](https://en.wikipedia.org/wiki/Java_Virtual_Machine) support for [dynamic languages](https://en.wikipedia.org/wiki/Dynamic_programming_language), with the new `invokedynamic` bytecode under JSR-292,[[141\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-JSR292-141) following the prototyping work currently done on the [Multi Language Virtual Machine](https://en.wikipedia.org/wiki/Da_Vinci_Machine)
- Compressed 64-bit pointers[[142\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-142) (available in Java 6 with `-XX:+UseCompressedOops`)[[143\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-143)
- These small language changes (grouped under a project named Coin):[[144\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-144)
  - Strings in [switch](https://en.wikipedia.org/wiki/Switch_statement)[[145\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-145)
  - Automatic resource management in try-statement[[146\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-146)
  - Improved [type inference](https://en.wikipedia.org/wiki/Type_inference) for generic instance creation, aka *the diamond operator <>*[[147\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-147)
  - Simplified varargs method declaration[[148\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-148)
  - Binary integer literals[[149\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-149)
  - Allowing underscores in numeric literals[[150\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-150)
  - Catching multiple exception types and rethrowing exceptions with improved type checking
- Concurrency utilities under JSR 166[[152\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-152)
- New file [I/O](https://en.wikipedia.org/wiki/I/O) library (defined by JSR 203) adding support for multiple file systems, file metadata and symbolic links. The new packages are `java.nio.file`, `java.nio.file.attribute` and `java.nio.file.spi`[[153\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-153)[[154\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-154)
- [Timsort](https://en.wikipedia.org/wiki/Timsort) is used to sort collections and arrays of objects instead of [merge sort](https://en.wikipedia.org/wiki/Merge_sort)
- Library-level support for [elliptic curve cryptography](https://en.wikipedia.org/wiki/Elliptic_curve_cryptography) algorithms
- An [XRender](https://en.wikipedia.org/wiki/XRender) pipeline for Java 2D, which improves handling of features specific to modern [GPUs](https://en.wikipedia.org/wiki/Graphics_processing_unit)
- New platform APIs for the graphics features originally implemented in version 6u10 as unsupported APIs[[155\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-155)
- Enhanced library-level support for new network protocols, including [SCTP](https://en.wikipedia.org/wiki/Stream_Control_Transmission_Protocol) and [Sockets Direct Protocol](https://en.wikipedia.org/wiki/Sockets_Direct_Protocol)
- [Upstream](https://en.wikipedia.org/wiki/Upstream_(software_development)) updates to [XML](https://en.wikipedia.org/wiki/XML) and [Unicode](https://en.wikipedia.org/wiki/Unicode)
- Java deployment rule sets[[156\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-156)

Java SE 8

Work on features was organized in terms of [JDK Enhancement Proposals (JEPs)](https://en.wikipedia.org/wiki/JDK_Enhancement_Proposal).[[226\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-226)

- JSR 335, JEP 126: Language-level support for [lambda expressions](https://en.wikipedia.org/wiki/Lambda_(programming)) (officially, lambda expressions; unofficially, [closures](https://en.wikipedia.org/wiki/Closure_(computer_programming))) under Project Lambda[[227\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-227) and default methods (virtual [extension methods](https://en.wikipedia.org/wiki/Extension_method))[[228\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-goetz_interface_evolution-228)[[229\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-229)[[230\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-230) which allow the addition of methods to interfaces without breaking existing implementations. 
  - There was an ongoing debate in the Java community on whether to add support for lambda expressions.[[231\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-231)[[232\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-232) Sun later declared that lambda expressions would be included in Java and asked for community input to refine the feature.[[233\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-233) Supporting lambda expressions also enables [functional](https://en.wikipedia.org/wiki/Functional_programming)-style operations on streams of elements, such as [MapReduce](https://en.wikipedia.org/wiki/MapReduce)-inspired transformations on collections. Default methods allow an author of an API to add new methods to an interface without breaking the old code using it. Although it was not their primary intent,[[228\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-goetz_interface_evolution-228) default methods also allow multiple inheritance of behavior (but not state).

- JSR 223, JEP 174: Project [Nashorn](https://en.wikipedia.org/wiki/Nashorn_(JavaScript_engine)), a JavaScript runtime which allows developers to embed JavaScript code within applications
- JSR 308, JEP 104: Annotation on Java types[[234\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-234)
- Unsigned integer arithmetic[[235\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-235)
- JSR 337, JEP 120: Repeating annotations[[236\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-236)
- JSR 310, JEP 150: Date and time API[[237\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-237)
- JEP 178: Statically-linked JNI libraries[[238\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-238)
- JEP 153: Launch [JavaFX](https://en.wikipedia.org/wiki/JavaFX) applications (direct launching of JavaFX application JARs)[[239\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-239)
- JEP 122: Remove the [permanent generation](https://en.wikipedia.org/wiki/Java_virtual_machine#Generational_heap)

Java SE 9

- JSR 376: Modularization of the JDK under Project Jigsaw ([Java Platform Module System](https://en.wikipedia.org/wiki/Java_Platform_Module_System))[[158\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-Jigsaw-158)

- JEP 222: [JShell](https://en.wikipedia.org/wiki/JShell): The Java Shell (a Java [REPL](https://en.wikipedia.org/wiki/REPL))[[295\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-295)

- JEP 295: [Ahead-of-time compilation](https://en.wikipedia.org/wiki/Graal_(compiler)#Ahead-of-Time_Compilation)[[296\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-296)

- JEP 268: [XML catalogs](https://en.wikipedia.org/wiki/XML_catalog)[[297\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-297)

- JEP 266: More concurrency updates.[[298\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-298) It includes a Java implementation of [Reactive Streams](https://en.wikipedia.org/wiki/Reactive_Streams),[[299\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-299) including a new `Flow` class[[300\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-300) that included the interfaces previously provided by Reactive Streams[[301\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-infoq-301)

- JEP 193: Variable handles:[[302\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-302) define a standard means to invoke the equivalents of various `java.util.concurrent.atomic` and `sun.misc.Unsafe` operations

- JEP 282: jlink: The Java Linker:[[303\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-303) create a tool that can assemble and optimize a set of modules and their dependencies into a custom run-time image. It effectively allows to produce a fully usable executable including the JVM to run it

- [JavaDB](https://en.wikipedia.org/wiki/JavaDB) was removed from JDK[[304\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-304)

- JEP 263: [HiDPI](https://en.wikipedia.org/wiki/HiDPI) graphics: automatic scaling and sizing[[305\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-305)

- JEP 254: Compact Strings[[306\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-306)

- JEP 213: Milling Project Coin

  [[307\]](https://en.wikipedia.org/wiki/Java_version_history#cite_note-307)

  - Allow @SafeVarargs on private instance methods
  - Allow effectively-final variables to be used as resources in the try-with-resources statement
  - Allow diamond with anonymous classes if the argument type of the inferred type is denotable
  - Complete the removal, begun in Java SE 8, of underscore from the set of legal identifier names
  - Support for private methods in interfaces

Java SE 10

- [JEP-286: Local-Variable Type Inference](https://openjdk.java.net/jeps/286)
- [JEP-296: Consolidate the JDK Forest into a Single Repository](https://openjdk.java.net/jeps/296)
- [JEP-304: Garbage-Collector Interface](https://openjdk.java.net/jeps/304)
- [JEP-307: Parallel Full GC for G1](https://openjdk.java.net/jeps/307)
- [JEP-310: Application Class-Data Sharing](https://openjdk.java.net/jeps/310)
- [JEP-312: Thread-Local Handshakes](https://openjdk.java.net/jeps/312)
- [JEP-313: Remove the Native-Header Generation Tool (javah)](https://openjdk.java.net/jeps/313)
- [JEP-314: Additional Unicode Language-Tag Extensions](https://openjdk.java.net/jeps/314)
- [JEP-316: Heap Allocation on Alternative Memory Devices](https://openjdk.java.net/jeps/316)
- [JEP-317: Experimental Java-Based JIT Compiler](https://openjdk.java.net/jeps/317)
- [JEP-319: Root Certificates](https://openjdk.java.net/jeps/319)
- [JEP-322: Time-Based Release Versioning](https://openjdk.java.net/jeps/322)

Java SE 11

- [JEP-181: Nest-Based Access Control](https://openjdk.java.net/jeps/181)
- [JEP-309: Dynamic Class-File Constants](https://openjdk.java.net/jeps/309)
- [JEP-315: Improve Aarch64 Intrinsics](https://openjdk.java.net/jeps/315)
- [JEP-318: Epsilon: A No-Op Garbage Collector](https://openjdk.java.net/jeps/318)
- [JEP-320: Remove the Java EE and CORBA Modules](https://openjdk.java.net/jeps/320)
- [JEP-321: HTTP Client (Standard)](https://openjdk.java.net/jeps/321)
- [JEP-323: Local-Variable Syntax for Lambda Parameters](https://openjdk.java.net/jeps/323)
- [JEP-324: Key Agreement with Curve25519 and Curve448](https://openjdk.java.net/jeps/324)
- [JEP-327: Unicode 10](https://openjdk.java.net/jeps/327)
- [JEP-328: Flight Recorder](https://openjdk.java.net/jeps/328)
- [JEP-329: ChaCha20 and Poly1305 Cryptographic Algorithms](https://openjdk.java.net/jeps/329)
- [JEP-330: Launch Single-File Source-Code Programs](https://openjdk.java.net/jeps/330)
- [JEP-331: Low-Overhead Heap Profiling](https://openjdk.java.net/jeps/331)
- [JEP-332: Transport Layer Security (TLS) 1.3](https://openjdk.java.net/jeps/332)
- [JEP-333: ZGC: A Scalable Low-Latency Garbage Collector (Experimental)](https://openjdk.java.net/jeps/333)
- [JEP-335: Deprecate the Nashorn JavaScript Engine](https://openjdk.java.net/jeps/335)
- [JEP-336: Deprecate the Pack200 Tools and API](https://openjdk.java.net/jeps/336)

Java SE 12

- [JEP-189: Shenandoah: A Low-Pause-Time Garbage Collector (Experimental)](https://openjdk.java.net/jeps/189)
- [JEP-230: Microbenchmark Suite](https://openjdk.java.net/jeps/230)
- [JEP-325: Switch Expressions (Preview)](https://openjdk.java.net/jeps/325)
- [JEP-334: JVM Constants API](https://openjdk.java.net/jeps/334)
- [JEP-340: One AArch64 Port, Not Two](https://openjdk.java.net/jeps/340)
- [JEP-341: Default CDS Archives](https://openjdk.java.net/jeps/341)
- [JEP-344: Abortable Mixed Collections for G1](https://openjdk.java.net/jeps/344)
- [JEP-346: Promptly Return Unused Committed Memory from G1](https://openjdk.java.net/jeps/346)

Java SE 13

- [JEP-350: Dynamic CDS Archives](https://openjdk.java.net/jeps/350)
- [JEP-351: ZGC: Uncommit Unused Memory](https://openjdk.java.net/jeps/351)
- [JEP-353: Reimplement the Legacy Socket API](https://openjdk.java.net/jeps/353)
- [JEP-354: Switch Expressions (Preview)](https://openjdk.java.net/jeps/354)
- [JEP-355: Text Blocks (Preview)](https://openjdk.java.net/jeps/355)

Java SE 14

- [JEP-305: Pattern Matching for instanceof (Preview)](https://openjdk.java.net/jeps/305)
- [JEP-343: Packaging Tool (Incubator)](https://openjdk.java.net/jeps/343)
- [JEP-345: NUMA-Aware Memory Allocation for G1](https://openjdk.java.net/jeps/345)
- [JEP-349: JFR Event Streaming](https://openjdk.java.net/jeps/349)
- [JEP-352: Non-Volatile Mapped Byte Buffers](https://openjdk.java.net/jeps/352)
- [JEP-358: Helpful NullPointerExceptions](https://openjdk.java.net/jeps/358)
- [JEP-359: Records (Preview)](https://openjdk.java.net/jeps/359)
- [JEP-361: Switch Expressions (Standard)](https://openjdk.java.net/jeps/361)
- [JEP-362: Deprecate the Solaris and SPARC Ports](https://openjdk.java.net/jeps/362)
- [JEP-363: Remove the Concurrent Mark Sweep (CMS) Garbage Collector](https://openjdk.java.net/jeps/363)
- [JEP-364: ZGC on macOS](https://openjdk.java.net/jeps/364)
- [JEP-365: ZGC on Windows](https://openjdk.java.net/jeps/365)
- [JEP-366: Deprecate the ParallelScavenge + SerialOld GC Combination](https://openjdk.java.net/jeps/366)
- [JEP-367: Remove the Pack200 Tools and API](https://openjdk.java.net/jeps/367)
- [JEP-368: Text Blocks (Second Preview)](https://openjdk.java.net/jeps/368)
- [JEP-370: Foreign-Memory Access API (Incubator)](https://openjdk.java.net/jeps/370)

Java SE 15

- [JEP-339: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://openjdk.java.net/jeps/339)
- [JEP-360: Sealed Classes (Preview)](https://openjdk.java.net/jeps/360)
- [JEP-371: Hidden Classes](https://openjdk.java.net/jeps/371)
- [JEP-372: Remove the Nashorn JavaScript Engine](https://openjdk.java.net/jeps/372)
- [JEP-373: Reimplement the Legacy DatagramSocket API](https://openjdk.java.net/jeps/373)
- [JEP-374: Disable and Deprecate Biased Locking](https://openjdk.java.net/jeps/374)
- [JEP-375: Pattern Matching for instanceof (Second Preview)](https://openjdk.java.net/jeps/375)
- [JEP-377: ZGC: A Scalable Low-Latency Garbage Collector](https://openjdk.java.net/jeps/377)
- [JEP-378: Text Blocks](https://openjdk.java.net/jeps/378)
- [JEP-379: Shenandoah: A Low-Pause-Time Garbage Collector](https://openjdk.java.net/jeps/379)
- [JEP-381: Remove the Solaris and SPARC Ports](https://openjdk.java.net/jeps/381)
- [JEP-383: Foreign-Memory Access API (Second Incubator)](https://openjdk.java.net/jeps/383)
- [JEP-384: Records (Second Preview)](https://openjdk.java.net/jeps/384)
- [JEP-385: Deprecate RMI Activation for Removal](https://openjdk.java.net/jeps/385)



## II. Basics



<br>

<h2><a name="variables-and-types-t" href="#variables-and-types-c">Variables and Types</a></h2>
<br>

### What are the primitive data types in Java? What are their value ranges?

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

### Q: Static Nested Class vs Inner Class?

Inner Class

- Can access to outer class both instance and static methods and fields

- Associated with instance of enclosing class so to instantiate it first needs an instance of outer class (note new keyword place): 

  ```
  Outerclass.InnerClass innerObject = outerObject.new Innerclass();
  ```

- Cannot define any static members itself

- Cannot have Class or Interface declaration

Static Nested Class

- Only can access outer class instance static methods or fields.

- Not associated with any instance of enclosing class So to instantiate it:

  ```
  OuterClass.StaticNestedClass nestedObject = new OuterClass.StaticNestedClass();
  ```

Similarities

- Both Inner classes can access even private fields and methods of outer class
- Also the Outer class have access to private fields and methods of inner classes
- Both classes can have private, protected or public access modifier

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
  
  

### What is transient keyword meaning?

`transient` is a Java keyword which marks a member variable not to be serialized when it is persisted to streams of bytes. When an object is transferred through the network, the object needs to be 'serialized'. Serialization converts the object state to serial bytes. Those bytes are sent over the network and the object is recreated from those bytes. Member variables marked by the java `transient` keyword are not transferred.

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

| Array                                                      | **ArrayList**                                                |
| ---------------------------------------------------------- | ------------------------------------------------------------ |
| Cannot contain values of different data types              | Can contain values of different data types.                  |
| Size must be defined at the time of declaration            | Size can be dynamically changed                              |
| Need to specify the index in order to add data             | No need to specify the index                                 |
| Arrays are not type parameterized                          | Arraylists are type                                          |
| Arrays can contain primitive data types as well as objects | Arraylists can contain only objects, no primitive data types are allowed |

### How HashMap works?

HashMap is store key-value entry data structure. It is based hash function to locate the key-value entry in map.

A HashMap is a LinkedList array. To get entry or put a entry:

- Firstly, to find the index of the array by its key's hashCode. Any element is LinkedList in the array, because multiple keys may have some hashCode, and these entries that have the same key will store in a LinkedList.
- Then, find really entry by comparing the specified key with every keys in the LinkedList.

Since Java 1.8, the HashMap has some improvement. When elements number of the LinkedList over 8, the LinkedList will convert to Red-Black Tree, and the time cost of to find really entry that have the same key's hashCode is from O(n) to O(logn) 

### Fail fast and fail safe iterators?

First of all, there is no term as fail-safe given in many places as Java SE specifications does not use this term. I am using fail safe to segregate between Fail fast and Non fail-fast iterators.

**Concurrent Modification:** Concurrent Modification in programming means to modify an object concurrently when another task is already running over it. For example, in Java to modify a collection when another thread is iterating over it. Some Iterator implementations (including those of all the general purpose collection implementations provided by the JRE) may choose to throw *ConcurrentModificationException* if this behavior is detected.

Fail fast vs non fail fast

- Fail-Fast. Iterators in java are used to iterate over the Collection objects. Fail-Fast iterators immediately throw *ConcurrentModificationException* if there is **structural modification** of the collection. Structural modification means adding, removing or updating any element from collection while a thread is iterating over that collection. Iterator on ArrayList, HashMap classes are some examples of fail-fast Iterator.

- Fail-Safe (Non fail-fast) iterators don’t throw any exceptions if a collection is structurally modified while iterating over it. This is because, they operate on the clone of the collection, not on the original collection and that’s why they are called fail-safe iterators. Iterator on CopyOnWriteArrayList, ConcurrentHashMap classes are examples of fail-safe Iterator.

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

### Starting Thread ways?

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

![Thread status](images/java-se-thread-status.jpg)

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

Java History

- [Java version history - Wikipedia](https://en.wikipedia.org/wiki/Java_version_history)

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