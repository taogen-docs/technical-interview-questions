# JVM Tuning Interview Questions

### Content

- JVM Basics
  - Introductions
    
  - Code Generation
    
    - JIT compiler
      - [x] [What is JIT compiler in Java?](#What is JIT compiler in Java?)
    - Class Loaders
      - [x] [What is a classloader?](#What is a classloader?)
      - [x] [What is the process of class loading?](#What is the process of class loading?)
      - [ ] [What is parent delegation model in Java?](#What is parent delegation model in Java?)（双亲委派模型）
    
  - Memory Management
    - Run-time Memory Model
      - [x] [What is JVM run-time memory model in JVM Specification?](#What is JVM run-time memory model in JVM Specification?)
      - [x] [Heap memory model for generational garbage collection(GC)?](#Heap memory model for generational garbage collection(GC)?   )   
      - [x] [What are the differences between Heap and Stack Memory?](#What are the differences between Heap and Stack Memory?)
    - Garbage Collection
      - [x] [What are garbage collect algorithms?](#What are garbage collect algorithms?)
      - [x] [What is generation garbage collection?](#What is generation garbage collection?)
      - [x] [What are garbage collectors?](#What are garbage collectors?)
      - [x] [How to select a garbage collector?](#How to select a garbage collector?)
      - [x] [Minor GC vs Major GC vs Full GC?](#Minor GC vs Major GC vs Full GC?)
    
  - Threads and Synchronization

- JVM Tuning
  
  - [x] [Common JVM options?](#Common JVM options?)
  
- JVM Troubleshoting

  - [x] [Common JVM troubleshotting tools?](#Common JVM troubleshotting tools?)
  - [x] [How to location OOM?](#How to location OOM?)
  - [x] [Memory leak code?](#Memory leak code?)

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

### What is the process of class loading?

The Java Virtual Machine dynamically loads, links and initializes classes and interfaces. 

- Loading is the process of finding the binary representation of a class or interface type with a particular name and *creating* a class or interface from that binary representation. 

- Linking is the process of taking a class or interface and combining it into the run-time state of the Java Virtual Machine so that it can be executed. 

- Initialization of a class or interface consists of executing the class or interface initialization method `<clinit>`.

### What is parent delegation model in Java?

The delegation model requires that any request for a class loader to load a given class is first delegated to its parent class loader before the requested class loader tries to load the class itself. The parent class loader, in turn, goes through the same process of asking its parent. This chain of delegation continues through to the bootstrap class loader (also known as the primordial or system class loader). If a class loader's parent can load a given class, it returns that class. Otherwise, the class loader attempts to load the class itself.

The JVM has three class loaders, each possessing a different scope from which it can load classes. As you descend the hierarchy, the scope of available class repositories widens, and typically the repositories are less trusted:

```
Bootstrap
|
Extensions
|
Application
```

At the top of the hierarchy is the bootstrap class loader. This class loader is responsible for loading only the classes that are from the core Java™ API. These classes are the most trusted and are used to bootstrap the JVM.

The extensions class loader can load classes that are standard extensions packages in the extensions directory.

The application class loader can load classes from the local file system, and will load files from the CLASSPATH. The application class loader is the parent of any custom class loader or hierarchy of custom class loaders.

Because class loading is always delegated first to the parent of the class loading hierarchy, the most trusted repository (the core API) is checked first, followed by the standard extensions, then the local files that are on the class path. Finally, classes that are located in any repository that your own class loader can access, are accessible. This system prevents code from less-trusted sources from replacing trusted core API classes by assuming the same name as part of the core API.

The parent-delegation model solving problems:

- Every class only load once.
- Every class loaded by one of ClassLoaders that choosing from top to bottom.
- Avoid load unsafe class. e.g. the `java.lang.Object` is only load from JRE library.

## Memory Management

### *Run-time Memory Model*

### What is JVM run-time memory model in JVM Specification?

Per-Thread data areas: 

- **Program Counter (PC) Register**: the `pc` register contains **the address of the JVM instruction currently being executed**. If the method is `native`, the value of the `pc` register is undefined.
- **JVM Stacks**: A JVM stack stores frames. The JVM stack holds **local variables** and **partial results**, and plays a part in method invocation and return. Each frame in a stack stores the current method’s local variable array, operand stack, and constant pool reference. A JVM stack may have many frames because until any method of a thread is finished it may call many other methods, and frames of these methods also store in the same JVM stack.
- **Native Method Stacks**: JVM may use native method stacks **to support native methods**. The native methods are written in a language other than the Java programming language. JVM implementations that cannot load native methods and that do not themselves rely on conventional stacks need not supply native method stack.

Shared areas:

- **Heap**: The JVM has a heap that is shared among all JVM threads. The heap is the run-time data area from which memory for all **class instances and arrays** is allocated.
- **Method Area**: It’s part of `heap`. The JVM has a method area that is shared among all JVM threads. The method area is analogous to the storage area for **compiled code** of conventional language or analogous to the “text” segment in an operating system process. It stores **per-class structures** such as the **run-time constant pool, field and method data, and the code for methods and constructors**, including the special methods used in class and instance initialization and interface initialization.
- **Run-time Constant Pool**: It’s part of `method area`. A run-time constant pool is a per-class or per-interface run-time representation of the `constant_pool` table in a `class` file. It contains several kinds of constant, ranging from **numeric literals** known at compile-time to method and **field references** that must be resolved at run-time. The run-time constant pool serves a function similar to that of a symbol table for a conventional programming language, although it contains a wider range of data than a typical symbol table.

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
- Metaspace (or Permanent Generation)
  - Compressed Class Space
- CodeCache
- Native Memory

Data Areas Description of Java SE 8 HotSpot VM 

Metaspace:

- JDK 8 does not have Permanent Generation.
- Class metadata is stored in a new space called Metaspace.
- Not contiguous with the Java Heap.

CodeCache

- Code Cache is used to store the compiled code generated by the Just-in-time compilers.
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

### *Garbage Collection*

### What are garbage collect algorithms?

GC algorithms

- reference counting
- mark and sweep
- stop and copy

**Reference counting**

Reference counting is a garbage collection algorithm where the runtime keeps track of how many live objects point to a particular object at a given time.

When the reference count for an object decreases to zero, the object has no referrers left, the object is available for garbage collection.

Advantages of reference counting algorithm

- It is obvious simplicity, is that any unreferenced object may be reclaimed immediately when its reference count drops to zero.

Disadvantages of reference counting algorithm

- The obvious flaw that cyclic constructs can never be garbage collected. Consequently cause a memory leak.
- Keeping the reference counts up to date can be expensive, especially in a parallel environment where synchronization is required.

**Mark and sweep**

The mark and sweep algorithm is the basis of all the garbage collectors in all commercial JVMs today. Mark and sweep can be done with or without copying or moving objects.

```
Mark:
	Add each object in the `root set` to a `queue`
    	For each object X in the `queue`
			Mark X reachable
			Add all objects of `heap` referenced from X to the queue
Sweep:
	For each object X on the `heap`
		If the X not marked, garbage collect it
```

Root set: it means the initial input set for this kind of search algorithm, that is the set of live objects from which the trace will start.

The following figure shows after mark:

![](images/java-se-jvm-mark-and-sweep-2.png)

**Stop and copy**

Stop and copy can be seen as a special case of tracing GC, and is intelligent in its way, but is impractical for large heap sizes in real applications.

Stop and copy garbage collection partitioning the heap into two region of equal size. Only one region is in use at a time. Stop and copy garbage collection goes through all live objects in one of the heap regions, starting at the root set, following the root set pointers to other objects and so on. The marked live objects are moved to the other heap region. After garbage collection, the heap regions are switched so that other half of the heap becomes the active region before the next collection cycle.

Advantages of stop and copy algorithm:

- fragmentation can’t become an issue.

Disadvantages of stop and copy algorithm:

- All live objects must be copied each time a garbage collection is performed, introducing a serious overhead in GC time as a function of the amount of live data.
- Only using half of heap at a time is a waste of memory.

The following figure shows the process of stop and copy:

![](images/java-se-jvm-stop-and-copy.png)

### What is generation garbage collection?

Generation garbage collection is based the mark and sweep GC algorithm.

In object-oriented languages, most objects are temporary or short-lived. However, performance improvement for handling short-lived objects on the heap can be had if the heap is split into two or more parts called generations.

In generational garbage collection, new objects are allocated in “young” generations of the heap, that typically are orders of magnitude smaller than the “old” generation, the main part of the heap. Garbage collection is then split into young and old collections, a young collection merely sweeping the young spaces of the heap, removing dead objects and promoting surviving objects by moving them to an older generation.

Collecting a smaller young space is orders of magnitude faster than collecting the larger old space. Even though young collections need to happen far more frequently, this is more efficient because many objects die young and never need to be promoted. ideally, total throughput is increased and some potential fragmentation is removed.



### What are garbage collectors?

JVM has four types of *GC* implementations:

- Serial Garbage Collector
- Parallel Garbage Collector
- CMS Garbage Collector
- G1 Garbage Collector

**Serial Garbage Collector**

This is the simplest GC implementation, as it basically works with a single thread. As a result, **this \*GC\* implementation freezes all application threads when it runs**. Hence, it is not a good idea to use it in multi-threaded applications like server environments.

The Serial GC is the garbage collector of choice for most applications that do not have small pause time requirements and run on client-style machines. To enable *Serial Garbage Collector*, we can use the following argument:

```
-XX:+UseSerialGC
```

Serial Garbage Collector GC log format: `DefNew`

```
7.732: [GC 7.732: [DefNew: 419456K->47174K(471872K), 0.1321800 secs] 419456K->47174K(1520448K), 0.1322500 secs] [Times: user=0.10 sys=0.03, real=0.14 secs]
```

**Parallel Garbage Collector**

It's the default *GC* of the *JVM* and sometimes called Throughput Collectors. Unlike *Serial Garbage Collector*, this **uses multiple threads for managing heap space**. But it also freezes other application threads while performing *GC*.

If we use this *GC*, we can specify maximum garbage collection *threads and pause time, throughput, and footprint* (heap size).

The numbers of garbage collector threads can be controlled with the command-line option *-XX:ParallelGCThreads=<N>*.

The maximum pause time goal (gap [in milliseconds] between two *GC*)is specified with the command-line option *-XX:MaxGCPauseMillis=<N>*.

The maximum throughput target (measured regarding the time spent doing garbage collection versus the time spent outside of garbage collection) is specified by the command-line option *-XX:GCTimeRatio=<N>.*

The maximum heap footprint (the amount of heap memory that a program requires while running) is specified using the option *-Xmx<N>.*

To enable *Parallel Garbage Collector*, we can use the following argument:

```
-XX:+UseParallelGC
```

Parallel Garbage Collector GC log format: `PSYoungGen`

```
30.250: [GC [PSYoungGen: 441062K->65524K(458752K)] 441062K->76129K(1507328K), 0.1870880 secs] [Times: user=0.33 sys=0.03, real=0.19 secs]
```

**CMS Garbage Collector**

**The \*Concurrent Mark Sweep (CMS)\* implementation uses multiple garbage collector threads for garbage collection.** It's designed for applications that prefer shorter garbage collection pauses, and that can afford to share processor resources with the garbage collector while the application is running.

Simply put, applications using this type of GC respond slower on average but do not stop responding to perform garbage collection.

> This collector also has a mode knows as an incremental mode which is being deprecated in Java SE 8 and may be removed in a future major release. As of Java 9, the CMS garbage collector has been deprecated. Therefore, JVM prints a warning message if we try to use it. Moreover, Java 14 completely dropped the CMS support.

To enable the *CMS Garbage Collector*, we can use the following flag:

```
-XX:+UseParNewGC
```

CMS Garbage Collector GC log format: `ParNew`

```
5.630: [GC 5.630: ['ParNew: 37915K->3941K(38336K), 0.0123210 secs] 78169K->45163K(1568640K), 0.0124030 secs] [Times: user=0.02 sys=0.00, real=0.01 secs]
```



**G1 Garbage Collector**

*G1 (Garbage First) Garbage Collector* is designed for applications running on multi-processor machines with large memory space. It's available since *JDK7 Update 4* and in later releases.

*G1* collector will replace the *CMS* collector since it's more performance efficient.

Unlike other collectors, *G1* collector partitions the heap into a set of equal-sized heap regions, each a contiguous range of virtual memory. When performing garbage collections, *G1* shows a concurrent global marking phase (i.e. phase 1 known as *Marking)* to determine the liveness of objects throughout the heap.

After the mark phase is completed, *G1* knows which regions are mostly empty. It collects in these areas first, which usually yields a significant amount of free space (i.e. phase 2 known as *Sweeping).* It is why this method of garbage collection is called Garbage-First.

To enable the *G1 Garbage Collector*, we can use the following argument:

```
-XX:+UseG1GC
```

G1 Garbage Collector GC log format: `G1 Evacuation Pause`

```
0.970: [GC pause (G1 Evacuation Pause) (young), 0.0096325 secs]
   [Parallel Time: 4.0 ms, GC Workers: 8]
      [GC Worker Start (ms): Min: 969.6, Avg: 969.7, Max: 969.7, Diff: 0.1]
      [Ext Root Scanning (ms): Min: 0.1, Avg: 0.3, Max: 1.5, Diff: 1.4, Sum: 2.8]
      [Update RS (ms): Min: 0.0, Avg: 0.0, Max: 0.0, Diff: 0.0, Sum: 0.0]
         [Processed Buffers: Min: 0, Avg: 0.0, Max: 0, Diff: 0, Sum: 0]
      [Scan RS (ms): Min: 0.0, Avg: 0.0, Max: 0.0, Diff: 0.0, Sum: 0.1]
      [Code Root Scanning (ms): Min: 0.0, Avg: 0.3, Max: 0.8, Diff: 0.8, Sum: 2.6]
      [Object Copy (ms): Min: 2.5, Avg: 3.2, Max: 3.5, Diff: 1.1, Sum: 25.6]
      [Termination (ms): Min: 0.0, Avg: 0.0, Max: 0.0, Diff: 0.0, Sum: 0.0]
         [Termination Attempts: Min: 2, Avg: 35.5, Max: 48, Diff: 46, Sum: 284]
      [GC Worker Other (ms): Min: 0.0, Avg: 0.0, Max: 0.0, Diff: 0.0, Sum: 0.3]
      [GC Worker Total (ms): Min: 3.9, Avg: 3.9, Max: 4.0, Diff: 0.1, Sum: 31.4]
      [GC Worker End (ms): Min: 973.6, Avg: 973.6, Max: 973.6, Diff: 0.0]
   [Code Root Fixup: 0.1 ms]
   [Code Root Purge: 0.0 ms]
   [String Dedup Fixup: 0.5 ms, GC Workers: 8]
      [Queue Fixup (ms): Min: 0.0, Avg: 0.0, Max: 0.0, Diff: 0.0, Sum: 0.0]
      [Table Fixup (ms): Min: 0.0, Avg: 0.0, Max: 0.4, Diff: 0.4, Sum: 0.4]
   [Clear CT: 0.1 ms]
   [Other: 5.0 ms]
      [Choose CSet: 0.0 ms]
      [Ref Proc: 4.7 ms]
      [Ref Enq: 0.0 ms]
      [Redirty Cards: 0.1 ms]
      [Humongous Register: 0.0 ms]
      [Humongous Reclaim: 0.0 ms]
      [Free CSet: 0.1 ms]
   [Eden: 70.0M(70.0M)->0.0B(61.0M) Survivors: 0.0B->9216.0K Heap: 70.0M(188.0M)->11.7M(188.0M)]
 [Times: user=0.02 sys=0.00, real=0.01 secs] 
```

### How to select a garbage collector?

Unless your application has rather strict pause time requirements, first run your application and **allow the VM to select a collector**. If necessary, adjust the heap size to improve performance. If the performance still does not meet your goals, then use the following guidelines as a starting point for selecting a collector.

- If the application has **a small data set** (up to approximately 100 MB), then
select the serial collector with the option `-XX:+UseSerialGC`.
- If the application will be run on **a single processor and there are no pause time requirements**, then let the VM select the collector, or select the serial collector with the option `-XX:+UseSerialGC`.
- If (a) **peak application performance** is the first priority and (b) there are **no pause time requirements** or pauses of 1 second or longer are acceptable, then let the VM select the collector, or select the parallel collector with `-XX:+UseParallelGC`.
- If **response time is more important** than overall throughput and garbage collection pauses must be kept shorter than approximately 1 second, then select the concurrent collector with `-XX:+UseConcMarkSweepGC` or `-XX:+UseG1GC`.

These guidelines provide only a starting point for selecting a collector because performance is dependent on the size of the heap, the amount of live data maintained by the application, and the number and speed of available processors. Pause times are particularly sensitive to these factors, so the threshold of 1 second mentioned previously is only approximate: the parallel collector will experience pause times longer than 1 second on many data size and hardware combinations; conversely, the concurrent collector may not be able to keep pauses shorter than 1 second on some combinations.

If the recommended collector does not achieve the desired performance, first attempt to adjust the heap and generation sizes to meet the desired goals. If performance is still inadequate, then try a different collector: use the concurrent collector to reduce pause times and use the parallel collector to increase overall throughput on multiprocessor hardware.

### Minor GC vs Major GC vs Full GC?

**Minor GC**

Collecting garbage from Young generation space (consisting of Eden and Survivor spaces) is called a **Minor GC**. 

Minor GC is triggered when JVM is unable to allocate space for a new Object, e.g. the Eden is getting full. So the higher the allocation rate, the more frequently Minor GC is executed.

**Major GC**

Major GC is cleaning the Tenured space.

Major GC triggered when old generation (or tenured space) does not have enough available space.

**Full GC**

Full GC is cleaning the entire Heap – both Young and Tenured spaces.

Full GC is triggered:

- When the old generation space no longer has available space for promoted objects. It actually performs a full  garbage collection when it determines there is not enough available space for object promotions from the next minor garbage collection. 
- when the permanent generation space does not have enough available space to store additional VM or class metadata

## JVM Tuning

### Common JVM options?

Option Types

- Standard Options: These are the most commonly used options that are supported by all implementations of the JVM.
- Non-Standard Options: These options are general purpose options that are specific to the Java HotSpot Virtual Machine.

**GC logging options**

```
-XX:+PrintGCDetails 
-XX:+PrintGCDateStamps 
-XX:+PrintCommandLineFlags 
```

GC Log File

```
-XX:+UseGCLogFileRotation  
-XX:NumberOfGCLogFiles=10
-XX:GCLogFileSize=50M 
-Xloggc:/home/user/log/gc.log
```

```
-Xloggc:/home/GCEASY/gc-%t.log
```

> `%t` suffixes timestamp to the GC log file in the format:  `YYYY-MM-DD_HH-MM-SS`. So, the generated GC log file name will start to look like: `gc-2019-01-29_20-41-47.log`.

**JVM Runtime Options**

- Client or Server Runtime

  ```
  -server
  -client
  ```

- 32-bit or 64-bit jvm

  ```
  // JVM automatically chooses 32-bit environmental
  -d<OS_bit>
  ```

- Garbage collector options

  ```
  // Serial Garbage Collector
  -XX:+UseSerialGC
  // Parallel Garbage Collector (default)
  -XX:+UseParallelGC
  // G1 Garbage Collector
  -XX:+UseG1GC
  // CMS Garbage Collector
  (-XX:+UseParNewGC)
  ```

**Memory Footprint options**

- heap size

  ```
  // Sets the initial size (in bytes) of the heap. 
  -Xms<n>[g|m|k]
  // Specifies the maximum size (in bytes) of the memory allocation pool in bytes.
  -Xmx<n>[g|m|k]
  ```

  ```
  -XX:InitialHeapSize=size
  -XX:MaxHeapSize=<size>
  ```

  ```
  // sets the maximum percentage of heap free after GC to avoid shrinking
  -XX:MaxHeapFreeRatio
  // sets the minimum percentage of heap free after GC to avoid expansion
  -XX:MinHeapFreeRatio
  ```

- young generation size

  ```
  // initial size young generation
  -XX:NewSize=<n>[g|m|k]
  // maximum size young generation
  -XX:MaxNewSize=<n>[g|m|k]
  ```

  ```
  // initial and maximum size young generation
  -Xmn<n>[g|m|k]
  ```

- Metaspace size

  ```
  // Java >= 8
  -XX:MetaspaceSize=<n>[g|m|k]
  -XX:MaxMetaspaceSize=<n>[g|m|k]
  // Java < 8
  -XX:PermSize=<perm gen size>[g|m|k] 
  -XX:MaxPermSize=<perm gen size>[g|m|k]
  ```

- Survivor

  ```
  // Ratio of eden/survivor space size 
  -XX:SurvivorRatio=<ratio>
  ```

- Stack size

  ```
  -Xss<n>[g|m|k]
  ```

  ```
  -XX:ThreadStackSize=<n>[g|m|k]
  ```

**Tuning for Response time/latency Options**

```
-XX:+PrintGCApplicationStoppedTime
-XX:+PrintGCApplicationConcurrentTime
-XX:+PrintSafepointStatistics
```

**Handling OutOfMemory Erorr**

- To trigger heap dump on out of memory

  ```
  -XX:+HeapDumpOnOutOfMemoryError
  -XX:HeapDumpPath=<file_path>
  -XX:HeapDumpPath=<file_path>`date`.hprof
  // limits the proportion of the VM's time that is spent in GC before an OutOfMemory error is thrown
  -XX:+UseGCOverheadLimit
  ```

- To restart the server immediately after out of memory occur

  ```
  -XX:OnOutOfMemoryError="shutdown -r"
  ```

**Others Options**

- `-XX:+UseStringDeduplication`: Java 8u20 has introduced this JVM parameter for reducing the unnecessary use of memory by creating too many instances of the same String; this optimizes the heap memory by reducing duplicate String values to a single global char[] array
- `-XX:+UseLWPSynchronization`: sets LWP (Light Weight Process) – based synchronization policy instead of thread-based synchronization
- `-XX:LargePageSizeInBytes`: sets the large page size used for the Java heap; it takes the argument in GB/MB/KB; with larger page sizes we can make better use of virtual memory hardware resources; however, this may cause larger space sizes for the PermGen, which in turn can force to reduce the size of Java heap space
- `-XX:+UseLargePages`: use large page memory if it is supported by the system; please note that OpenJDK 7 tends to crash if using this JVM parameter
- `-XX:+UseStringCache`: enables caching of commonly allocated strings available in the String pool
- `-XX:+UseCompressedStrings`: use a byte[] type for String objects which can be represented in pure ASCII format
- `-XX:+OptimizeStringConcat`: it optimizes String concatenation operations where possible

## JVM Troubleshotting

### Common JVM troubleshotting tools?

Visual JVM Monitoring Tools

- jvisualvm
- jconsole
- jmc

JVM command line utilities

- jps: obtain jvm Process ID
- jstack: obtain Java and native stack information
- jmap: obtain memory map information, including a heap histogram
- jstat: obtain information about performance and resource consumption
- jcmd: to send diagnostic command requests to the JVM)

JVM profiling tools

- JProfiler: live profiling, offline profiling, view HPROF snapshot.
- Eclipse Memory Analyzer(MAT): To analyze heap dumps.

### How to location OOM?

Steps

- Using visual JVM monitor (JVisualVM, JConsole) to find the reason of OutOfMemory or StackOverflow Error.
- Using `jmap` to get the heap dump HPROF binary file.
- Using JVM profiling tools (JProfiler, MAT) to analyzing the HPROF file, and to check the biggest objects, to find the error code.

### Memory leak code?

```java
public class MemLeak {
    public final String key;
    public MemLeak(String key) {
        this.key = key;
    }

    public static void main(String args[]) throws InterruptedException {
            Map map = System.getProperties();
            for(;;) {
                map.put(new MemLeak("hello" + new Date()), new Date());
                Thread.sleep(1);
            }
    }
}
```



## References

JVM Basics

- [JVM Garbage Collectors](https://www.baeldung.com/jvm-garbage-collectors)
- [Minor GC vs Major GC vs Full GC](https://plumbr.io/blog/garbage-collection/minor-gc-vs-major-gc-vs-full-gc)

JVM Tuning

- [10 Important JVM Options for Production JAVA Application System](https://geekflare.com/important-jvm-options/)
- [Guide to the Most Important JVM Parameters](https://www.baeldung.com/jvm-parameters)
- [Java VM Options You Should Always Use in Production](https://blog.sokolenko.me/2014/11/javavm-options-production.html)

JVM Troubleshotting