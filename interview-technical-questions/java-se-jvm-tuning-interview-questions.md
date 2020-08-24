# JVM Tuning Interview Questions

### Content

- JVM Basics
  - (Memory Model, Class Load Mechanism, GC Mechanism)
  - Code Generation
    - JIT compiler
      - [What is JIT compiler in Java?](#What is JIT compiler in Java?)
  - Memory Management
    - Run-time Memory
      - [What are the differences between Heap and Stack Memory?](#What are the differences between Heap and Stack Memory?)
  - Threads and Synchronization
- JVM Tuning
  - (How to location OOM, How to location infinite dead loop)

## Code Generation

### *JIT compiler*

### What is JIT compiler in Java?

JIT stands for Just-In-Time compiler in Java. It is a program that helps in converting the Java bytecode into instructions that are sent directly to the processor. By default, the JIT compiler is enabled in Java and is activated whenever a Java method is invoked. The JIT compiler then compiles the bytecode of the invoked method into native machine code, compiling it “just in time” to execute. Once the method has been compiled, the JVM summons the compiled code of that method directly rather than interpreting it. This is why it is often responsible for the performance optimization of Java applications at the run time.

## Memory Management

### *Run-time Memory*

### What are the differences between Heap and Stack Memory?

|    **Features**     | **Stack**                                                    | **Heap**                                                     |
| :-----------------: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|      *Memory*       | Stack memory is used only by one thread of execution.        | Heap memory is used by all the parts of the application.     |
|      *Access*       | Stack memory can’t be accessed by other threads.             | Objects stored in the heap are globally accessible.          |
| *Memory Management* | Follows LIFO manner to free memory.                          | Memory management is based on the generation associated with each object. |
|     *Lifetime*      | Exists until the end of execution of the thread.             | Heap memory lives from the start till the end of application execution. |
|       *Usage*       | Stack memory only contains local primitive and reference variables to objects in heap space. | Whenever an object is created, it’s always stored in the Heap space. |