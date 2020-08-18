# Java SE Interview Questions

### Content

- I. Introduction
  - <a name="java-platform-c" href="#java-platform-t">Java Platform</a>
    - [Explain JDK, JRE and JVM?](#Explain JDK, JRE and JVM?)
  - <a name="java-features-c" href="#java-features-t">Java Features</a>
    - [How Java cross platforms(Write once, run anywhere)?](#How Java cross platforms(Write once, run anywhere)?)
  - <a name="java-history-c" href="#java-history-t">Java History</a>
- II. Basics
  - <a name="variables-and-types-c" href="#variables-and-types-t">Variables and Types</a>
    - [What are the basic data types in Java? What are their value ranges?](#What are the basic data types in Java? What are their value ranges?)
    - [Why does computer float data type can't precisely represent decimal fraction?](#Why does computer float data type can't precisely represent decimal fraction?)
    - [Why can't you use float data type to represent amount of money?](#Why can't you use float data type to represent amount of money?)
    - [Character encoding and charsets?](#Character encoding and charsets?)
    - [String length vs byte array length of string?](#String length vs byte array length of string?)
  - <a name="operators-and-expressions-c" href="#operators-and-expressions-t">Operators and Expressions</a>
  - <a name="control-flow-c" href="#control-flow-t">Control Flow</a>
  - <a name="string-and-array-c" href="#string-and-array-t">String and Array</a>
    - [Why String is immutable or final in java?](#Why String is immutable or final in java?)
    - `String` vs `StringBuffer` vs `StringBuilder`?
- III. Core
  - <a name="classes-and-objects-c" href="#classes-and-objects-t">Classes and Objects</a>
    - Object-Oriented
      - Object-Oriented vs Procedure-Oriented?
      - Object-Oriented basic features?
      - Object-Oriented basic principles?
    - Functions
      - Pass by value vs. pass by reference?
    - Keywords
      - [What is final meaning?](#What is final meaning?)
      - (final, abstract, static)
      - (public, protected, private)
      - (transient, volatile, synchronized)
      - (instanceof)
    - The java.lang.Object
      - (hashcode() method)
  - <a name="inheritance-and-polymorphism-c" href="#inheritance-and-polymorphism-t">Inheritance and Polymorphism</a>
    - What is Polymorphism?
    - Method overriding vs method overloading?
    - Inheritance vs composition
  - <a name="interface-c" href="#interface-t">Interface, Lambada, and Inner Classes</a>
  - <a name="exceptions-c" href="#exceptions-t">Exceptions, Assertions, and Logging</a>
    - Common Exception class names?
    - How to handle exception? Right ways of handling exception.
    - Return statements in try-catch-finally?
  - <a name="generic-c" href="#generic-t">Generic Programming</a>
  - <a name="annotations-c" href="#annotations-t">Annotations</a>
  - <a name="reflection-c" href="#reflection-t">Reflection and Proxy</a>
    - What is reflection
    - Static proxy vs dynamic proxy?
  - <a name="enum-c" href="#enum-t">Enumeration Types and Wrapper Types</a>
    - What are wrapper classes? Why do we need it?
    - What are boxing, unboxing, and autoboxing? What are wrapper classes caches?
    - [Using primitive data types or wrapper classes to declare a variable?](#Using primitive data types or wrapper classes to declare a variable?)
- IV. Advanced
  - <a name="io-c" href="#io-t">Input and Output</a>
  - <a name="collections-c" href="#collections-t">Collections and Streams</a>
    - Collection API and Their Difference
    - Collection Applicability
      - (How to choice data structure for different usage scenario?)
    - Implementation Principles
    - Iterator
      - (Fail fast and fail safe iterators)
  - <a name="concurrency-c" href="#concurrency-t">Concurrency</a>
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

### Why String is immutable or final in java?

TODO







## III. Core


<br>
<h2><a name="classes-and-objects-t" href="#classes-and-objects-c">Classes and Objects</a></h2>
<br>

### What is final meaning?

- the `final` keyword for variables it is meaning the variable can't reassignment. 
- final for method
- final for class 



<br>
<h2><a name="inheritance-and-polymorphism-t" href="#inheritance-and-polymorphism-c">Inheritance and Polymorphism</a></h2>

<br>



<br>
<h2><a name="interface-t" href="#interface-c">Interface, Lambada, and Inner Classes</a></h2>
<br>




<br>
<h2><a name="exceptions-t" href="#exceptions-c">Exceptions, Assertions, and Logging</a></h2>
<br>





<br>
<h2><a name="generic-t" href="#generic-c">Generic Programming</a></h2>
<br>





<br>
<h2><a name="annotations-t" href="#annotations-c">Annotations</a></h2>
<br>





<br>
<h2><a name="reflection-t" href="#reflection-c">Reflection and Proxy</a></h2>
<br>




<br>
<h2><a name="enum-t" href="#enum-c">Enumeration Types and Wrapper Types</a></h2>
<br>

### Using primitive data types or wrapper classes to declare a variable?

Wrapper classes. Because they have not concrete default values. When variables have not assignment, primitive data types have default values, but wrapper classes are null. Default values of primitive data type may cause error result. When wrapper classes are null, the program may occur `NullPointerException`, but it can't cause error results.

## IV. Advanced



<br>
<h2><a name="io-t" href="#io-c">Input and Output</a></h2>
<br>



<br>
<h2><a name="collections-t" href="#collections-c">Collections and Streams</a></h2>
<br>



<br>
<h2><a name="concurrency-t" href="#concurrency-c">Concurrency</a></h2>
<br>



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