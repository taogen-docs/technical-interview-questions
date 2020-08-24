# JVM Tuning Interview Questions

### Content

- JVM Basics
  - > Memory Model, Class Load Mechanism, GC Mechanism
  
  - Introductions
    
  - Code Generation
    
    - JIT compiler
      - [What is JIT compiler in Java?](#What is JIT compiler in Java?)
    - Class Loaders
      - [What is a classloader?](#What is a classloader?)
    
  - Memory Management
    - Run-time Memory Model
      - [What is JVM run-time memory model in JVM Specification?](#What is JVM run-time memory model in JVM Specification?)
      - [Heap memory model for generational garbage collection(GC)?](#Heap memory model for generational garbage collection(GC)?   )   
      - [What are the differences between Heap and Stack Memory?](#What are the differences between Heap and Stack Memory?)
    
  - Threads and Synchronization
- JVM Tuning
  
  - (How to location OOM, How to location infinite dead loop)

## Code Generation

### *JIT compiler*

### What is JIT compiler in Java?

JIT stands for Just-In-Time compiler in Java. It is a program that helps in converting the Java bytecode into instructions that are sent directly to the processor. By default, the JIT compiler is enabled in Java and is activated whenever a Java method is invoked. The JIT compiler then compiles the bytecode of the invoked method into native machine code, compiling it “just in time” to execute. Once the method has been compiled, the JVM summons the compiled code of that method directly rather than interpreting it. This is why it is often responsible for the performance optimization of Java applications at the run time.

### *ClassLoader*

### What is a classloader?

The **Java ClassLoader** is a subset of JVM (Java Virtual Machine) that is responsible for loading the class files. Whenever a Java program is executed it is first loaded by the classloader. Java provides three built-in classloaders:

1. Bootstrap ClassLoader
2. Extension ClassLoader
3. System/Application ClassLoader

## Memory Management

### *Run-time Memory Model*

### What is JVM run-time memory model in JVM Specification?

Per-Thread data area: 

- **Program Counter (PC) Register**: the `pc` register contains the address of the JVM instruction currently being executed. If the method is `native`, the value of the `pc` register is undefined.
- **JVM Stacks**: A JVM stack stores frames. The JVM stack holds local variables and partial results, and plays a part in method invocation and return. Each frame in a stack stores the current method’s local variable array, operand stack, and constant pool reference. A JVM stack may have many frames because until any method of a thread is finished it may call many other methods, and frames of these methods also store in the same JVM stack.
- **Native Method Stacks**: JVM may use native method stacks to support native methods. The native methods are written in a language other than the Java programming language. JVM implementations that cannot load native methods and that do not themselves rely on conventional stacks need not supply native method stack.

Common area

- **Heap**: The JVM has a heap that is shared among all JVM threads. The heap is the run-time data area from which memory for all class instances and arrays is allocated.
- **Method Area**: It’s part of `heap`. The JVM has a method area that is shared among all JVM threads. The method area is analogous to the storage area for compiled code of conventional language or analogous to the “text” segment in an operating system process. It stores per-class structures such as the run-time constant poll, field and method data, and the code for methods and constructors, including the special methods used in class and instance initialization and interface initialization.
- **Run-time Constant Pool**: It’s part of `method area`. A run-time constant pool is a per-class or per-interface run-time representation of the `constant_pool` table in a `class` file. It contains several kinds of constant, ranging from numeric literals known at compile-time to method and field references that must be resolved at run-time. The run-time constant pool serves a function similar to that of a symbol table for a conventional programming language, although it contains a wider range of data than a typical symbol table.

### Heap memory model for generational garbage collection(GC)?   

> Permanent Generation: 
>
> - HotSpot JVM prior to JDK 8 had a third generation called Permanent Generation. 
> - Used for: JVM internal representation of classes and their metadata, Class statics, Interned strings.
> - Contiguous with the Java Heap.

Memory Structure of Java SE 8 HotSpot VM 

- Java Heap
  - Young Generation
    - Eden
    - Survivor
    - Virtual
  - Old Generation
- Metaspace 
  - Compressed Class Space
- CodeCache
- Native Memory

Data Areas Description of Java SE 8 HotSpot VM 

Metaspace:

- JDK 8 does not have Permanent Generation.
- Class metadata is stored in a new space called Metaspace.
- Not contiguous with the Java Heap.

CodeCache

- Code Cache is used to store the compiled code generated by the Just-intime compilers.
- It is allocated out of native memory.
- Managed by the Code Cache Sweeper.

Native Memory

- Available system memory.
- Not managed by the JVM memory management.

### What are the differences between Heap and Stack Memory?

|    **Features**     | **Stack**                                                    | **Heap**                                                     |
| :-----------------: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|      *Memory*       | Stack memory is used only by one thread of execution.        | Heap memory is used by all the parts of the application.     |
|      *Access*       | Stack memory can’t be accessed by other threads.             | Objects stored in the heap are globally accessible.          |
| *Memory Management* | Follows LIFO manner to free memory.                          | Memory management is based on the generation associated with each object. |
|     *Lifetime*      | Exists until the end of execution of the thread.             | Heap memory lives from the start till the end of application execution. |
|       *Usage*       | Stack memory only contains local primitive and reference variables to objects in heap space. | Whenever an object is created, it’s always stored in the Heap space. |