# Data Structures and Algorithms Code Questions

### Content

- Fundamental Data Structures Problems
  - Array
    - [ ] Q: How do you find the missing number in a given integer array of 1 to 100?
    - [ ] Q: How do you find the duplicate number on a given integer array?
    - [ ] Q: How do you find the largest and smallest number in an unsorted integer array?
    - [ ] Q: How do you find all pairs of an integer array whose sum is equal to a given number?
    - [ ] Q: How do you find duplicate numbers in an array if it contains multiple duplicates?
    - [ ] Q: How are duplicates removed from a given array in Java?
    - [ ] Q: How is an integer array sorted in place using the quicksort algorithm?
    - [ ] Q: How do you remove duplicates from an array in place?
    - [ ] Q: How do you reverse an array in place in Java?
    - [ ] Q: How are duplicates removed from an array without using any library?
  - Linked List
    - [ ] Q: How do you find the middle element of a singly linked list in one pass?
    - [ ] Q: How do you check if a given linked list contains a cycle? How do you find the starting node of the cycle?
    - [ ] Q: How do you reverse a linked list?
    - [ ] Q: How do you reverse a singly linked list without recursion?
    - [ ] Q: How are duplicate nodes removed in an unsorted linked list?
    - [ ] Q: How do you find the length of a singly linked list?
    - [ ] Q: How do you find the third node from the end in a singly linked list?
    - [ ] Q: How do you find the sum of two linked lists using Stack? 
  - Stack and Queue
  - Tree (Binary Tree)
    - [ ] Q: How are all leaves of a binary search tree printed?
    - [ ] Q: How do you count a number of leaf nodes in a given binary tree?
    - [ ] Q: How do you perform a binary search in a given array?
  - Graph
- Common Algorithms Problems
  - Sort
  - Search
- Advanced Data Structures Problems
  - Binary Search Tree, AVL Tree
  - B-Tree, Red–black Tree
  - Heap
  - Trie
  - Dictionary
  - Hashing (Hash Table)
  - Priority Queue
  - String
    - [ ] How do you print duplicate characters from a string?
    - [ ] How do you check if two strings are anagrams of each other?
    - [ ] How do you print the first non-repeated character from a string?
    - [ ] How can a given string be reversed using recursion?
    - [ ] How do you check if a string contains only digits?
    - [ ] How are duplicate characters found in a string?
    - [ ] How do you count a number of vowels and consonants in a given string?
    - [ ] How do you count the occurrence of a given character in a string?
    - [ ] How do you find all permutations of a string?
    - [ ] How do you reverse words in a given sentence without using any library method?
    - [ ] How do you check if two strings are a rotation of each other?
    - [ ] How do you check if a given string is a palindrome? 
  - Matrix
- Algorithm Design Problems
  - Dynamic programming
  - Divide and Conquer
  - Greedy
  - Backtracking
  - DFS/BFS
  - Randomized
  - Branch and Bound
- Others Algorithm Problems
  - [ ] Q: How do you swap two numbers without using the third variable?
  - [ ] Q: How do you check if two rectangles overlap with each other?
  - [ ] Q: How do you design a vending machine?

- References

## Main



## Fundamental Data Structures Problems

### Array

### Linked List

### Stack and Queue

### Tree (Binary Tree)

### Graph



## Common Algorithms Problems

### Sort

### Search



## Advanced Data Structures Problems

### Binary Search Tree, AVL Tree

### B-Tree, Red–black Tree

### Heap

### Trie

### Dictionary

### Hashing (Hash Table)

### Priority Queue

### String

### Matrix



## Algorithm Design Problems

### Recursion

Using recursion to print text like below

```
*
**
***
****
***
**
*
```

Solution 1:

```java
public static void main(String[] args) {
    print(1, 4, 1);
}

public static void print(int curr, int n, int flag) {
    if (curr == 0) {
        return;
    }
    for (int i = 0; i < curr; i++) {
        System.out.print("*");
    }
    System.out.println();
    if (curr == n) {
        flag = -1;
    }
    print(curr + flag, n, flag);
}
```

Solution 2:

```java
public static void main(String[] args) {
    print(1, 4);
}

public static void print(int curr, int n) {
    if (curr > n) {
        return;
    }
    for (int i = 0; i < curr; i++) {
        System.out.print("*");
    }
    System.out.println();
    print(curr + 1, n);
    if (curr < n) {
        for (int i = 0; i < curr; i++) {
            System.out.print("*");
        }
        System.out.println();
    }
}
```

### Dynamic programming

### Divide and Conquer

### Greedy

### Backtracking

### DFS/BFS

### Randomized

### Branch and Bound

## Others Algorithm Problems

## References

- [50+ Data Structure and Algorithms Interview Questions for Programmers](https://hackernoon.com/50-data-structure-and-algorithms-interview-questions-for-programmers-b4b1ac61f5b0)