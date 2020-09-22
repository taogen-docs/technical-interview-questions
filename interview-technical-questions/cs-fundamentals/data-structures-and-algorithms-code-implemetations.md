# Data Structures and Algorithms Implementations

### Content

- Data Structure Implementations
  - Array
  - Linked List
  - Stack and Queue
  - Tree
    - [ ] Q: Binary tree implementation?
    - [ ] Q: Binary search tree implementation? 
    - [ ] Q: preorder traversal in a given binary tree?
    - [ ] Q: preorder without recursion?
    - [ ] Q: inorder traversal in a given binary tree?
    - [ ] Q: inorder traversal without recursion?
    - [ ] Q: postorder traversal algorithm?
    - [ ] Q: postorder traversal without recursion?
  - Graph
- Algorithms Implementations
  - Sort
    - [ ] Q: Bubble sort algorithm implementation?
    - [ ] Q: insertion sort algorithm implementation?
    - [ ] Q: selection sort algorithm implementation?
    - [ ] Q: Iterative quicksort algorithm implementation?
    - [ ] Q: merge sort algorithm implementation?
    - [ ] Q: bucket sort algorithm implementation?
    - [ ] Q: counting sort algorithm implementation?
    - [ ] Q: radix sort algorithm implementation? 
  - Search
    - [ ] Q: Binary Search Implementation?
- Advanced Data Structure Implementations
- References

## Main

## Data Structure Implementations

### Array

`ArrayList.java`

```java

public class ArrayList 
{
	private int MAX_SIZE = 5;
	private int a[];
	private int currSize = 0;
	
	public ArrayList()
	{
		this.a = new int[MAX_SIZE];
	}
	
	public ArrayList(int size)
	{
		this.MAX_SIZE = size;
		this.a = new int[MAX_SIZE];
	}
	
	public void add(int data)
	{
		if (currSize + 1 > MAX_SIZE)
		{
			int arr[] = new int[MAX_SIZE * 2];
			for (int i = 0; i < currSize; i++)
			{
				arr[i] = a[i];
			}
			a = arr;
			MAX_SIZE *= 2;
		}
		a[currSize] = data;
		currSize++;
	}
	
	public void remove(int pos)
	{
		if (pos < 0 || pos > currSize -1)
		{
			System.out.println("Failed to remove! Cause by invalide parameter.");
			return;
		}
		
		if (pos == currSize - 1)
		{
			a[currSize] = 0;
			return;
		}
		
		for (int i = pos; i < currSize; i++)
		{
			a[i] = a[i+1];
		}
		currSize--;
	}
	
	public int get(int pos)
	{
		if (pos < 0 || pos > currSize - 1)
		{
			System.out.println("Failed to get! Cause by over range of list!");
		}
		return a[pos];
	}
    
	public void print()
	{
		for (int i = 0; i < currSize; i++)
		{
			System.out.print(a[i] + " ");
		}
		System.out.println();
	}
}
```



### Linked List

`SingleLinkedList.java`

```java

/**
 * @Description
 * Sigle LinkedList 
 *     Node first;
 *     Node last;
 *     int size;
 *     SingleLinkedList();
 *     insertAtStart();
 *     insertAtEnd();
 *     removeAtPos(int pos);
 *     print();
 * Node
 *     int data;
 *     Node next;
 *     Node(int data)
 *
 */
public class SingleLinkedList 
{
	private Node first;
	private Node last;
	private int size = 0;
	
	static class Node
	{
		private int data;
		private Node next;
		public Node(int data)
		{
			this.data = data;
			this.next = null;
		}
	}
	
	public SingleLinkedList()
	{
	}
	
	public void insertFirst(int data)
	{
		Node newNode = new Node(data);
		if (this.first == null)
		{
			last = newNode;
		}
		else
		{
			newNode.next = first;
			first = newNode;
		}
		this.size++;
	}
	
	public void insertLast(int data)
	{
		Node newNode = new Node(data);
		if (this.first == null)
		{
			first = newNode;
		}
		else
		{
			last.next = newNode;
		}
		last = newNode;
		size++;
	}
	
	public void removeAtPos(int pos)
	{
		if (size == 0)
		{
			System.out.println("Failed to remove! Cause by list is empty!");
		}
		if (pos > size - 1 || pos < 0)
		{
			System.out.println("Failed to remove! Cause by invalid parameter!");
		}
		Node node = first;
		if (pos == 0)
		{
			if (size > 1)
			{
				first = first.next;
			}
			if (size == 1)
			{
				first = null;
				last = null;
			}
		}

		for (int i = 1; i < size; i++)
		{
			if (pos == i)
			{
				if (pos != size - 1)
				{
					node.next = node.next.next;
				}
				else
				{
					node.next = null;
					last = node;
				}
				break;
			}
			node = node.next;
		}
	}
	
	public void print()
	{
		if (size == 0)
		{
			System.out.println("empty!");
			return;
		}
		
		Node node = first;
		while(node != null)
		{
			System.out.print(node.data);
			if (node.next != null)
			{
				System.out.print("->");
			}
			node = node.next;
		}
		System.out.println();
	}
}
```

`DoubleLinkedList.java`

```java

/**
 * @Description
 * DoubleLinkedList
 *     Node first;
 *     Node last;
 *     int size;
 *     SingleLinkedList();
 *     insertFirst();
 *     insertLast();
 *     removeAtPos(int pos);
 *     print();
 * Node
 *     int data;
 *     Node next;
 *     Node prev
 *     Node(int data)
 *
 */
public class DoubleLinkedList 
{
	private Node first;
	private Node last;
	private int size = 0;
	
	static class Node
	{
		private int data;
		private Node next;
		private Node prev;
		public Node(int data)
		{
			this.data = data;
			this.next = null;
			this.prev = null;
		}
	}
	
	public DoubleLinkedList()
	{}
	
	public void insertFirst(int data)
	{
		Node newNode = new Node(data);
		Node f = first;
		first = newNode;
		first.next = f;
		if (f == null)
		{
			last = newNode;
		}
		else
		{
			f.prev = first;
			first.next = f;
		}
		size++;
	}
	
	public void insertLast(int data)
	{
		Node newNode = new Node(data);
		Node l = last;
		last = newNode;
		if (first == null)
		{
			first = newNode;
		}
		else
		{
			l.next = newNode;
			newNode.prev = l;
		}
		size++;
	}
	
	public void removeAtPos(int pos)
	{
		if (size <= 0)
		{
			System.out.println("Failed to remove! Cause by list is empty!");
		}
		
		if (pos < 0 || pos > size - 1)
		{
			System.out.println("Failed to remove! Cause by invalid paramter.");
		}
		
		Node node = first;
		for (int i = 0; i < size; i++)
		{
			if (pos == i)
			{
				if (node.prev == null)
				{
					first = null;
					last = null;
				}
				else
				{
					if (node.next != null)
					{
						node.prev.next = node.next;
						node.next.prev = node.prev;
					}
					else
					{
						node.prev.next = node.next;
					}
				}
				break;
			}
			node = node.next;
		}
		size--;
	}
	
	public void print()
	{
		if (size == 0)
		{
			System.out.println("list is empty!");
		}
		Node node = first;
		while (node != null)
		{
			System.out.print(node.data);
			if (node.next != null)
			{
				System.out.print("->");
			}
			node = node.next;
		}
		System.out.println();
	}
}
```



### Stack and Queue

`Stack.java`

```java

/**
 * Stack
 *     int MAX;
 *     int top;
 *     int a[MAX];
 *     isEmpty();
 *     isFull();
 *     size();
 *     push();
 *     pop();
 *     peek();
 *
 */
public class Stack 
{
	static final int MAX = 3;
	int top;
	int a[] = new int[MAX];
	
	public Stack()
	{
		top = -1;
	}
	
	boolean isEmpty()
	{
		return (top < 0);
	}
	
	boolean isFull()
	{
		return (top == MAX - 1);
	}
	
	int size()
	{
		return top + 1;
	}
	
	boolean push(int data)
	{
		if (top + 1 > MAX - 1)
		{
			System.out.println("Stack overflow!");
			return false;
		}
		else
		{
			a[++top] = data;
			return true;
		}
	}
	
	int pop()
	{
		if (top < 0)
		{
			System.out.println("Stack underflow!");
			return -1;
		}
		else
		{
			return a[top--];
		}
	}
	
	int peek()
	{
		if (top < 0)
		{
			System.out.println("Stack is empty!");
			return -1;
		}
		else
		{
			return a[top];
		}
	}
}
```

`Queue.java`

```java

/**
 * Queue
 *     int front;
 *     int rear;
 *     int size;
 *     int a[];
 *     isEmpty();
 *     isFull();
 *     size();
 *     enqueue();
 *     dequeue();
 *     peek();
 */
public class Queue 
{
	int front, rear, size, capacity, a[];
	public Queue(int capacity)
	{
		this.capacity = capacity;
		front = size = 0;
		rear = capacity - 1;
		a = new int[capacity];
	}
	
	boolean isEmpty()
	{
		return (size == 0);
	}
	
	boolean isFull()
	{
		return (size == capacity);
	}
	
	int size()
	{
		return size;
	}
	
	void enqueue(int data)
	{
		if (isFull())
		{
			return;
		}
		rear = (rear + 1) % capacity;
		a[rear] = data;
		size++;
	}
	
	int dequeue()
	{
		if (isEmpty())
		{
			return -1;
		}
		int item = a[front];
		front = (front + 1) % capacity;
		size--;
		return item;
	}
}
```



### Tree

`BinaryTree.java`

```java
public class BinaryTree 
{
	TreeNode root;
	
	public BinaryTree()
	{}
	
	public BinaryTree(int data)
	{
		root = new TreeNode(data);
	}
    
    static class TreeNode
    {
        int data;
        TreeNode left;
        TreeNode right;
        public TreeNode(int data)
        {
            this.data = data;
            left = right = null;
        }
    }
    
    /*
	 * traverse Preorder
	 * Binary Tree Example:
	 *         1
	 *     2       3
	 *   4   5   6
	 * result: 1 2 4 5 3 6
	 */
	public static void traversePreorder(Node root)
	{
		if (root != null)
		{
			System.out.print(root.data + " ");
			traversePreorder(root.left);
			traversePreorder(root.right);
		}
	}
	
	/*
	 * traverse Inorder
	 * Binary Tree Example:
	 *         1
	 *     2       3
	 *   4   5   6
	 * result: 4 2 5 1 6 3
	 */
	public static void traverseInorder(Node root) 
	{
		Stack<Node> stack = new Stack<Node>();
		while (root != null)
		{
			stack.push(root);
			root = root.left;
		}
		while (! stack.isEmpty())
		{
			Node node = stack.pop();
			System.out.print(node.data + " ");
			traverseInorder(node.right);
		}
	}
	
	/*
	 * traverse Postorder
	 * Binary Tree Example:
	 *         1
	 *     2       3
	 *   4   5   6
	 * result: 4 5 2 6 3 1
	 */
	public static void traversePostorder(Node root)
	{
		Stack<Node> stack = new Stack<Node>();
		while (root != null)
		{
			stack.push(root);
			root = root.left;
		}

		while (! stack.isEmpty())
		{
			Node node = stack.pop();
			if (node.right != null)
			{
				traversePostorder(node.right);
			}
			System.out.print(node.data + " ");
		}
	}
	
	/*
	 * traverse Level Order
	 * Binary Tree Example:
	 *         1
	 *     2       3
	 *   4   5   6
	 * result: 1 2 3 4 5 6
	 */
	public static void traverseLevelOrder(Node root)
	{
		int h = height(root);
		for (int i = 1; i <= h; i++)
		{
			printLevel(root, i);
		}
	}
	
	/*
	 * BFS help 
	 */
	public static int height(Node root)
	{
		if (root == null)
		{
			return 0;
		}
		else
		{
			int lheight = height(root.left);
			int rheight = height(root.right);
			if (lheight > rheight)
			{
				return (lheight + 1);
			}
			else
			{
				return (rheight + 1);
			}
		}
	}
	
	/*
	 * BFS help 
	 */
	public static void printLevel(Node root, int level)
	{
		if (root == null)
		{
			return;
		}
		else
		{
			if (level == 1)
			{
				System.out.print(root.data + " ");
			}
			else 
			{
				printLevel(root.left, level - 1);
				printLevel(root.right, level - 1);
			}
		}
	}
}
```



### Graph

`AdjMatrixGraph.java`

```java
/**
 * AdjMatrixGraph
 *     int V; //vertexs number
 *     int E; // Edges number
 *     int adj[][]; 
 *     AdjMatrixGraph(int V);
 *     addEdge(int src, int dest);
 *     contains(int src, int dest);
 */
public class AdjMatrixGraph
{
	private final int V;
	private int E;
	private boolean adj[][];
    
	public AdjMatrixGraph(int V)
	{
		this.V = V;
		this.E = 0;
		this.adj = new boolean[V][V];
	}
	
	public void addEdge(int src, int dest)
	{
		if (! adj[src][dest])
		{
			E++;
		}
		adj[src][dest] = true;
		adj[dest][src] = true;
	}
	
	public void removeEdge(int src, int dest)
	{
		if (adj[src][dest])
		{
			E--;
		}
		adj[src][dest] = false;
		adj[dest][src] = false;
	}
	
	public boolean contains(int src, int dest)
	{
		return adj[src][dest];
	}
	
	/*
	public void printGraph()
	{
		for (int i = 0; i < V; i++)
		{
			System.out.println("vertex " + i + " list: ");
			System.out.print("head");
			for (int j = 0; j < V; j++)
			{
				if (adj[i][j])
				{
					System.out.print("->" + j + " ");
				}
			}
			System.out.println();
		}
	}
	*/
	
	public void printGraphMatrix()
	{
		for (int i = 0; i < V; i++)
		{
			for (int j = 0; j < V; j++)
			{
				System.out.print(adj[i][j] ? 1 : 0);
				
			}
			System.out.println();
		}
		System.out.println();
		return;
	}
}
```

`Graph.java`

```java
/**
 * Graph
 *     int V;
 *     LinkedList adjListArray[];
 *     Graph(V);
 *     addEdge(int src, int dest);
 *     removeEdge(int src, int dest);
 *     printGraph();
 *     BFS(int vertex);
 *     DFS(int vertex);
 */
public class Graph 
{
	int V;
	LinkedList<Integer> adjListArray[];
	
	public Graph(int V) 
	{
		this.V = V;
		adjListArray = new LinkedList[V];
		
		for (int i = 0; i < adjListArray.length; i++)
		{
			adjListArray[i] = new LinkedList<>();
		}
		visited = new boolean[V];
	}
	
	void addEdge(int src, int dest)
	{
		if (src > V - 1 || src < 0 || dest > V-1 || dest <0)
		{
			System.out.println("Failed to add edge of graph! Cause by invalid parameter.");
		}
		else
		{
			adjListArray[src].add(dest);
			adjListArray[dest].add(src);
		}
	}
	
	void removeEdge(int src, int dest)
	{
		if (src > V - 1 || src < 0 || dest > V-1 || dest <0)
		{
			System.out.println("Failed to add edge of graph! Cause by invalid parameter.");
		} 
		else
		{
			adjListArray[src].remove(Integer.valueOf(dest));
			adjListArray[dest].remove(Integer.valueOf(src));
		}
	}
	
	void printGraph()
	{
		for (int v = 0; v < this.V; v++)
		{
			System.out.println("Adjacency list of vertex " + v);
			System.out.print("head");
			for (Integer i : adjListArray[v])
			{
				System.out.print("->" + i);
			}
			System.out.println();
		}
	}
	private static boolean visited[];
	
	void DFS(int vertex)
	{
		System.out.print(vertex + " ");
		visited[vertex] = true;
		for (Integer i : adjListArray[vertex])
		{
			if (! visited[i])
			{
				DFS(i);
				break;
			}
		}
		return;
	}
	
	void BFS(int vertex)
	{
		boolean visited[] = new boolean[V];
		ArrayDeque<Integer> queue = new  ArrayDeque<Integer>(V);
		visited[vertex] = true; // NOTICE. don't ignore this statement.
		queue.add(vertex);
		
		while (! queue.isEmpty())
		{
			int v = queue.poll();
			System.out.print(v + " ");
			
			Iterator<Integer> iterator = adjListArray[v].listIterator();
			while (iterator.hasNext() )
			{
				int n = iterator.next();
				if (! visited[n])
				{
					visited[n] = true; // NOTICE. don't ignore this statement.
					queue.add(n);					
				}
			}
		}
	}
}
```



## Algorithms Implementations

### Sort

`MergeSort.java`

```java

/**
 * Worst: T(n) = O(nlogn)
 * Average: T(n) = O(nlogn)
 * Best: T(n) = O(nlogn)
 */
public class Mergesort
{
	static void mergesort(int arr[], int left, int right)
	{
		if (left < right)
		{
			int middle = (left + right) / 2;
			mergesort(arr, left, middle);
			mergesort(arr, middle+1, right);
			merge(arr, left, middle, right);
		}
	}
	
	static void merge(int arr[], int left, int middle, int right)
	{
		int n1 = middle - left + 1;
		int n2 = right - middle;
		int L[] = new int[n1];
		int R[] = new int[n2];
		for (int i = 0; i < n1; i++)
		{
			L[i] = arr[left+i]; // notice. it is left+i rather than i
		}
		for (int j = 0; j < n2; j++)
		{
			R[j] = arr[middle+1+j];
		}
		int k = left, i = 0, j = 0; // notice. k=left rather than k = 0
		while(i < n1 && j < n2)
		{
			if (L[i] < R[j])
			{
				arr[k++] = L[i++];
			}
			else
			{
				arr[k++] = R[j++];
			}
		}
		
		while (i < n1)
		{
			arr[k++] = L[i++];
		}
		while (j < n2)
		{
			arr[k++] = R[j++];
		}
	}
	
	public static void main(String[] args)
	{
		int arr[] = {3, 1, 2, 4, 7, 4, 0, 3, 5}; // 0, 1, 2, 3, 3,  4, 4, 5, 7
		mergesort(arr, 0, arr.length - 1);
		for (int i = 0; i < arr.length; i++)
		{
			System.out.print(arr[i] + " ");
		}
		System.out.println();
	}
}
```

`QuickSort.java`

```java


/**
 * Worst: T(n) = O(n^2)
 * Average: T(n) = O(nlogn)
 * Best: T(n) = O(nlogn)
 */
public class Quicksort 
{
	public static void quicksort(int a[], int left, int right)
	{
		if (a == null || left >= right)
		{
			return;
		}
		int pi = partition(a, left, right);
		quicksort(a, left, pi-1);
		quicksort(a, pi+1, right);
		
	}

	private static int partition(int[] a, int left, int right) 
	{
		int temp = a[right];
		int i = left, j = right - 1;
		while (i < j)
		{
			while(a[i] < temp && i < right) 
			{
				i++;
			}
			while(a[j] >= temp && j > left)
			{
				j = j-1;
			}
			if (i < j)
			{
				int t = a[i];
				a[i] = a[j];
				a[j] = t;
			}
		}
		if (i >= j)
		{
			a[right] = a[i];
			a[i] = temp;
		}
		return i;
	}
	public static int partition2(int arr[], int low, int high)
	{
		// pivot (Element to be placed at right position)
	    int pivot = arr[high];  
	 
	    int i, j;
	    i = (low - 1);  // Index of smaller element

	    for (j = low; j <= high- 1; j++)
	    {
	        // If current element is smaller than or
	        // equal to pivot
	        if (arr[j] <= pivot)
	        {
	            i++;    // increment index of smaller element
	            //swap arr[i] and arr[j]
	            int t = arr[i];
	            arr[i] = arr[j];
	            arr[j] = t;
	        }
	    }
	    //swap arr[i + 1] and arr[high])
	    arr[high] = arr[i+1];
	    arr[i+1] = pivot;
	    return (i + 1);
	}
	
	public static void main(String[] args) 
	{
		int a[] = {1, 4, 2, 5, 6, 1, 4, 23, 2, 12};
		quicksort(a, 0, a.length - 1);
		for (int i = 0; i < a.length; i++)
		{
			System.out.print(a[i] + " ");
		}
	}
}
```



### Search

`BinarySearch.java`

```java

/**
 * @Description
 * T(n) = O(logn)
 */
 public class BinarySearch
 {
	 static int binarySearch(int arr[], int left, int right, int N)
	 {
		 if (left <= right)
		 {
			 int mid = left + (right - left) / 2;
			 if (arr[mid] == N)
			 {
				 return mid;
			 }
			 if (arr[mid] > N)
			 {
				return binarySearch(arr, left, mid-1, N); // NOTICE. add return sentence.
			 }
			return binarySearch(arr, mid+1, right, N); 
		 }
		
		return -1;
		 
	 }
	 
	 public static void main(String[] args)
	 {
		 int arr[] = {1, 3, 4, 5, 7, 9}; // NOTICE. array is ordered.
		 System.out.println(binarySearch(arr, 0, arr.length-1, 9));
		 System.out.println(binarySearch(arr, 0, arr.length-1, 3));
	 }
 }
```



## Advanced Data Structure Implementations





## References