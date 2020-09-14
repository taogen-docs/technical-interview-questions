# Design Patterns Interview Questions

### Content

- [Q: Singleton Design Pattern Implementations?](#Q: Singleton Design Pattern Implementations?)

### Q: Singleton Design Pattern Implementations?

Implementations

- Private constructor method.
- Public getInstance() method.

```java
// Hungry: Eager initialization
public class Singleton{
    private final static Singleton instance =  new Singleton();
    private Singleton(){}
    public static Singleton getInstance(){
        return instance;
    }
}

// Lazy 1: Lazy initialization with Double check locking
public class Singleton
{
	private static Singleton instance;
	private Singleton() {}
	public synchronized static Singleton getInstance() 
	{
		if (instance == null)
		{
			synchronized (Singleton.class)
			{
				if (instance == null)
				{
					instance = new Singleton();
				}
			}
		}
		return instance;
	}
}

// Lazy 2 by Inner Class
public class Singleton 
{
	private Singleton() {}

	public static Singleton getInstance() 
	{
		return Inner.INSTANCE;
	}
    	
	private static class Inner
	{
		private static final Singleton INSTANCE = new Singleton();
	}
}
```

