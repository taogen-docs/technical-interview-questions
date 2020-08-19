# Java SE Interview Questions

### Content

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
    - [ ] Method overriding vs method overloading?
    - [ ] Inheritance vs composition
  - <a name="interface-c" href="#interface-t">Interface, Lambada, and Inner Classes</a>
    - [ ] [Why use nested classes?](#Why use nested classes?)
  - <a name="exceptions-c" href="#exceptions-t">Exceptions, Assertions, and Logging</a>
    - [ ] Common Exception class names?
    - [ ] How to handle exception? Right ways of handling exception.
    - [ ] Return statements in try-catch-finally?
  - <a name="generic-c" href="#generic-t">Generic Programming</a>
  - <a name="annotations-c" href="#annotations-t">Annotations</a>
  - <a name="reflection-c" href="#reflection-t">Reflection and Proxy</a>
    - [ ] What is reflection
    - [ ] Static proxy vs dynamic proxy?
  - <a name="enum-c" href="#enum-t">Enumeration Types and Wrapper Types</a>
    - [ ] What are wrapper classes? Why do we need it?
    - [ ] What are boxing, unboxing, and autoboxing? What are wrapper classes caches?
    - [x] [Using primitive data types or wrapper classes to declare a variable?](#Using primitive data types or wrapper classes to declare a variable?)
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

String

- [Why String is Immutable or Final in Java](https://javarevisited.blogspot.com/2010/10/why-string-is-immutable-or-final-in-java.html)

Object-Oriented Programming

- [Functional vs Object-Oriented vs Procedural Programming](https://medium.com/@LiliOuakninFelsen/functional-vs-object-oriented-vs-procedural-programming-a3d4585557f3)
- [What are four basic principles of Object Oriented Programming?](https://medium.com/@cancerian0684/what-are-four-basic-principles-of-object-oriented-programming-645af8b43727)
- [Principles of Object-Oriented Design](http://www.cs.utsa.edu/~cs3443/notes/designPrinciples/designPrinciples.html)

Object

- [Guide to hashCode() in Java](https://www.baeldung.com/java-hashcode)
- [Java equals() and hashCode()](https://www.journaldev.com/21095/java-equals-hashcode)