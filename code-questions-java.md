# Java Code Questions

Menu

- <a id="varAndTypeMenu" href="varAndTypeTitle">I. Variable and Basic Types</a>
  - Primitive Build-in Types
  - Type Conversions
  - Literals
  - Variable (Definition, Initialization, Scope)
- II. Strings , Vectors, and Arrays
  - String 
  - Array
- III. Expressions
  - Operators Priority
  - Arithmetic Operators (+, -, *, /, %)
  - Logical and Relational Operators 
  - Assignment Operators
  - Increment and Decrement Operators (++, --)
  - Member Access operators (.)
  - Conditional Operators (x ? r1 : r2)
  - Bitwise Operators (&, |, !, ^, <<)
- IV. Statements
  - Conditional Statements
  - Iterative Statements
  - Jump Statements
  - try Blocks and Exception Handling
- V. Functions
- VI. Classes & Object
  - Access Control
  - Key Word
  - Object
  - Wrapper class
  - Inheritance
  - Polymorphism
  - Abstract and Interface
- VII. Libraries
  - IO library
  - Container
- VIII. Advanced Topics
  - Reflect
  - Generics
  - Thread
  - JVM
  - Socket
- VIII. Others
  - Design Patterns

### Main

<h3 id="varAndTypeTitle">I. Variable and Basic Types</h3>



### II. Strings , Vectors, and Arrays



### III. Expressions

Question: Operators Priority

```java
public static void main(String[] args)
{
    int i = 1, j = 2;
    int k = i +++ j;
    System.out.println("i: " + i + ", j: " + j + ", k: " + k);
}
```

Result


<details>
  <summary>Click to expand!</summary>

```java
Result:
i: 2, j: 2, k: 3

Reason:
Priority ++ > + ,  so i +++ j  is same with  (i++) + j, 
```
</details>



### IV. Statements

#### Exception

Question: return statement in exception handling

```java
public static int test()
{
    try
    {
        System.out.println("try...");
        int i = 1/0;
        return 1;
    }
    catch(Exception e)
    {
        System.out.println("catch...");
        return 2;
    }
    finally
    {
        System.out.println("finally...");
        return 3;
    } 
}
```

Result

<details>
  <summary>Click to expand!</summary>

```java
Result:
3

Reason:
- if occur exception, the try block return statement will not be executed. the catch have return statement will be executed. else try executed, catch not executed.
- Anyway, if finally block have return statement， it will be executed and cover either try or catch block return statement.
```
</details>



Question: Nested Exception Run Sequence

```java
try
{
	try
	{
		System.out.println("try...");
		int i = 1/0;
	}
	catch (NullPointerException e )
	{
		System.out.println("catch...");
	}
	finally
	{
		System.out.println("finally...");
	}
}
catch(Exception e) 
{
	System.out.println("base catch...");
}
finally
{
	System.out.println("base finally...");
}
```

Result

<details>
	<summary>Click to expand!</summary>

```
Result:
try...
finally...
base catch..
base finally..

Reason:
`try` - `try` execute until the last executable line.
`catch` - It can execute outside `catch` block if inside `catch` can't catch the exception.
`finally` - all `finally` block must execute from inside to outside.
```
</details>




### V. Functions



### VI. Classes & Object

#### Object

Question: equals vs == in String

```java
String a1 = "hello";
String a2 = "he" + "llo";
String b1 = new String("hello");
String b2 = "he" + new String("llo");
String b3 = new String("he") + "llo";
String b4 = new String("hello");
// type1
System.out.println(a1 == a2); 
System.out.println();

// type2
System.out.println(a1 == b1); 
System.out.println(a1 == b2);
System.out.println(a1 == b3);
System.out.println(a1 == b4);
System.out.println();

// type3
System.out.println(b1 == b2); 
System.out.println(b1 == b3);
System.out.println(b3 == b4);
System.out.println();

// type4
System.out.println(b1.equals(a1));
System.out.println(b1.equals(a2));
System.out.println(b1.equals(b2));
System.out.println(b1.equals(b3));
System.out.println();
```

Result

<details>
	<summary>Click to expand!</summary>

```
Result:
System.out.println(a1 == a2);     // type1, true
System.out.println(a1 == b*);     // type2, false
System.out.println(b* == b*);     // type3, false
System.out.println(b*.equals(*)); // type4, true

Reason:
"xxxxxx"      // It is a string literal. Store in String static pool, no repeat string in there.
"xx" + "xxx"  // It is a string literal too. Store in String static pool.
new String("xxx")          // it is a string object, store in heap.
new String("xxx") + "xxx"  // it is a new String Object, store in heap.
```
</details>




#### Wrapper class

Question: Integer == int

```java
Integer a1 = 1;
Integer a2 = 1;
int a3 = 1;
Integer b1 = 128;
Integer b2 = 128;
int b3 = 128;

System.out.println(a1 == a2); 
System.out.println(a1 == a3); 
System.out.println(b1 == b2); 
System.out.println(b1 == b3); 

```

Result

<details>
	<summary>Click to expand!</summary>

```
Result: 
System.out.println(a1 == a2); // 1. true
System.out.println(a1 == a3); // 2. true
System.out.println(b1 == b2); // 3. false
System.out.println(b1 == b3); // 4. true

Reason:
// 1. less than max_default_int_cache = 127, There are two int cache contrast.
// 2. same to 1.
// 3. greater than max_default_int_cache = 127, There are two object contrast. 
// 4. int == Integer or Integer == int, There are numeric value contrast. Integer will auto unbox. It always == is true.
// Integer => Byte, Short, Long, the output result will be same. All cache of Byte, Short, Integer, Long max_default_cache = 127. They are between -128~127. Only Integer cache max value can set over 127. 
// private static class IntegerCache, ByteCache, LongCache
```
</details>





#### Inheritance

#### Polymorphism

Question: instanceof in Polymorphism

```java
class A{}
class B extends A{}
class C extends A{}
class D extends B{}
public class Main
{
    public static void main(String[] args)
    {
        A obj = new D();
        System.out.println(obj instanceof B); 
        System.out.println(obj instanceof C); 
        System.out.println(obj instanceof D); 
        System.out.println(obj instanceof A); 
        B  b = new B();
        System.out.println(b instanceof B);
        System.out.println(b instanceof A); 
    }
}

```

Result

<details>
	<summary>Click to expand!</summary>

```
Result:
System.out.println(obj instanceof B); // 1. true
System.out.println(obj instanceof C); // 2. false
System.out.println(obj instanceof D); // 3. true
System.out.println(obj instanceof A); // 4. true

System.out.println(b instanceof B); // 5. true
System.out.println(b instanceof A); // 6. true

Reason:
1, 2, 3, 4 
A obj = new D(); The object is D, the obj instance of D it ture, so #3 is true. D has inheritance relation with A, B, so #1, #4 is true. It has't relation with C, so #2 is false.
5, 6
A instanceof B. if A has direct or indirect Inheritance relation. The #5, #6 is ture.
```
</details>



Question: Function Calling in Polymorphism

```java
class A {
    public String show(D obj) {
        return ("A and D");
    }
    public String show(A obj) {
        return ("A and A");
    } 
}

class B extends A{
    public String show(B obj){
        return ("B and B");
    }
    public String show(A obj){
        return ("B and A");
    } 
}

class C extends B{
}

class D extends B{
}

public class Test {
    public static void main(String[] args) {
        A a1 = new A();
        A a2 = new B();
        B b = new B();
        C c = new C();
        D d = new D();
        
        System.out.println("1--" + a1.show(b));
        System.out.println("2--" + a1.show(c));
        System.out.println("3--" + a1.show(d));
        System.out.println("4--" + a2.show(b));
        System.out.println("5--" + a2.show(c));
        System.out.println("6--" + a2.show(d));
        System.out.println("7--" + b.show(b));
        System.out.println("8--" + b.show(c));
        System.out.println("9--" + b.show(d));    
    }
}

```

Result

<details>
	<summary>Click to expand!</summary>

```java
Result：
1--A and A
2--A and A
3--A and D
4--B and A
5--B and A
6--A and D
7--B and B
8--B and B
9--A and D

Reason:
A a1 = new A();
A a2 = new B();
B b = new B();
Super type and super Object - a1：(1)Only find in super. (2)Only call in super
Super type and son Object - a2: (1)only find in super. (2)First call in son. But if not exist in son, then call super.
Son type and son object - b: (1)First find in son, then find in super. (2)Find just call.
```
</details>



Question: Object Instantiating in Polymorphism

```java
class Parent {
	private String name = "parent";
	public Parent()
	{
		System.out.println("Parent constructor...");
		print();
	}
	
	public void print()
	{
		System.out.println("Parent print...");
		System.out.println("name=" + name);
	}
}

class Son extends Parent{
	private String name = "son";
	
	public Son()
	{
		System.out.println("Son constructor..");
	}
	
	public void print()
	{
		System.out.println("Son print..");
		System.out.println("name=" + this.name);
	}
}
public class Main
{
   public static void main(String[] args)
    {
        Parent parent = new Son();
    } 
}

```

Result

<details>
	<summary>Click to expand!</summary>

```
Result:
Parent Constructor...

Son print...

name=null   

Son Constructor...

Reason:
Why name=null ?
When son print() execute by Polymorphism, but instance variales are not initialize and the Son contructor not execute. 
```
</details>





#### Abstract and Interface



### VII. Libraries

### VIII. Advanced Topics

#### Thread

Question: Writing a Deadlock

```java
public class Main
{
    static Object lock1 = new Object();
    static Object lock2 = new Object();

    public static void main(String[] args) throws InterruptedException, ExecutionException
    {
        new Thread(new Runnable() {
            @Override
            public void run()
            {
                synchronized(lock1)
                {
                    System.out.println(Thread.currentThread().getName() + " hold lock1...");
                    sleep();
                    synchronized(lock2)
                    {
                        System.out.println(Thread.currentThread().getName() + " hold lock2...");
                        sleep();
                    }
                }
            }
        }).start();
        new Thread(() -> {
            synchronized(lock2)
            {
                System.out.println(Thread.currentThread().getName() + " hold lock2...");
                sleep();
                synchronized(lock1)
                {
                    System.out.println(Thread.currentThread().getName() + " hold lock1...");
                }
            }
        }).start();
    }
    
    public static void sleep()
    {
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}
```

Result

<details>
	<summary>Click to expand!</summary>

```
Thread-0 hold lock1...
Thread-1 hold lock2...
(deadlock status...)
```
</details>





### VIII. Others

#### Design Patterns

Question: Writing a Singleton 

```java
// hungry mode
public class SingleObject_hungry 
{
	private final static SingleObject_hungry instance = new SingleObject_hungry();
	private SingleObject_hungry() {}
	public static SingleObject_hungry getInstance() 
	{
		return instance;
	}
}
// lazy 1
public class SingleObject_lazy 
{
	private static SingleObject_lazy instance;
	private SingleObject_lazy() {}
	public synchronized static SingleObject_lazy getInstance() 
	{
		if (instance == null)
		{
			synchronized (SingleObject_lazy.class)
			{
				if (instance == null)
				{
					instance = new SingleObject_lazy();
				}
			}
		}
		return instance;
	}
}
// lazy 2
public class SingleObject_lazy2 
{
	private SingleObject_lazy2() {}
	
	private static class SingletonInstance
	{
		private static final SingleObject_lazy2 INSTANCE = new SingleObject_lazy2();
	}
	
	public static SingleObject_lazy2 getInstance() 
	{
		return SingletonInstance.INSTANCE;
	}
}
```



