# Database Systems Interview Questions

### Content

- [Introduction to DBMS](#Introduction to DBMS)
  - [x] [Q: What is DBMS?](#Q: What is DBMS?)
  - [x] [Q: What is a database system?](#Q: What is a database system?)
  - [x] [Q: What are the advantages of DBMS?](#Q: What are the advantages of DBMS?)
  - [x] [Q: What is RDBMS?](#Q: What is RDBMS?)
  - [x] [Q: What is data abstraction in DBMS?](#Q: What is data abstraction in DBMS?)
  - [x] [Q: What are the three levels of data abstraction?](#Q: What are the three levels of data abstraction?)
  - [x] [Q: What do you mean by transparent DBMS?](#Q: What do you mean by transparent DBMS?)
  - [x] [Q: What do you understand by Data Model?](#Q: What do you understand by Data Model?)
- [Relational Model and SQL](#Relational Model and SQL)
  - [Introduction to Relational Model](#Introduction to Relational Model) (DB structure, schema, keys, operations)
    - [x] [Q: What is a database?](#Q: What is a database?)
    - [x] [Q: Define a Relation Schema and a Relation?](#Q: Define a Relation Schema and a Relation?)
    - [x] [Q: What is a degree of Relation?](#Q: What is a degree of Relation?)
    - [x] [Q: Describe the types of keys?](#Q: Describe the types of keys?)
  - [Introduction to SQL](#Introduction to SQL)
    - [x] [Q: How many types of database languages are?](#Q: How many types of database languages are?)
    - [x] [Q: What is DDL (Data Definition Language)?](#Q: What is DDL (Data Definition Language)?)
    - [x] [Q: What is DML (Data Manipulation Language)?](#Q: What is DML (Data Manipulation Language)?)
    - [x] [Q: What is the difference between a DELETE command and TRUNCATE command?](#Q: What is the difference between a DELETE command and TRUNCATE command?)
  - [Intermediate SQL](#Intermediate SQL) (Join)
    - [x] [Q: What is Join?](#Q: What is Join?)
  - [Advanced SQL](#Advanced SQL) (procedures, triggers)
    - [x] [Q: What is stored procedure?](#Q: What is stored procedure?)
  - [Formal Relational Query Languages](#Formal Relational Query Languages) (Relational Algebra, Tuple Relational Calculus, Domain Relational Calculus)
    - [x] [Q: What are the unary operations in Relational Algebra?](#Q: What are the unary operations in Relational Algebra?)
    - [x] [Q: What is Relational Algebra?](#Q: What is Relational Algebra?)
    - [x] [Q: What is Relational Calculus?](#Q: What is Relational Calculus?)
- [Database Design](#Database Design)
  - [Database Design and E-R Model](#Database Design and E-R Model) (design process, ER model, constraints, diagrams)
    - [x] [Q: What is the E-R model?](#Q: What is the E-R model?)
    - [x] [Q: What is an entity?](#Q: What is an entity?)
    - [x] [Q: What is an Entity type?](#Q: What is an Entity type?)
    - [x] [Q: What is an Entity set?](#Q: What is an Entity set?)
    - [x] [Q: What is an Extension of entity type?](#Q: What is an Extension of entity type?)
    - [x] [Q: What is Weak Entity set?](#Q: What is Weak Entity set?)
    - [x] [Q: What is the Relationship?](#Q: What is the Relationship?)
    - [x] [Q: What is an attribute?](#Q: What is an attribute?)
    - [x] [Q: What are the integrity rules in DBMS?](#Q: What are the integrity rules in DBMS?)
    - [x] [Q: What do you mean by extension and intension?](#Q: What do you mean by extension and intension?)
  - [Relational Database Design](#Relational Database Design)
    - [x] [Q: What is normalization?](#Q: What is normalization?)
    - [x] [Q: 1NF vs 2NF vs 3NF vs BCNF?](#Q: 1NF vs 2NF vs 3NF vs BCNF?)
    - [x] [Q: What is Denormalization?](#Q: What is Denormalization?)
    - [x] [Q: What is functional Dependency?](#Q: What is functional Dependency?)
  - Application Design and Development
- [Data Storage and Querying](#Data Storage and Querying)
  - [Storage and File Structure](#Storage and File Structure)
    - [x] [Q: What are the disadvantages of file processing systems?](#Q: What are the disadvantages of file processing systems?)
  - [Indexing and Hashing](#Indexing and Hashing)
    - [x] [Q: Explain Index Depth, Density and Selectivity factors and how these factors affect index performance?](#Q: Explain Index Depth, Density and Selectivity factors and how these factors affect index performance?)
  - [Query Processing](#Query Processing)
  - [Query Optimization](#Query Optimization)
    - [x] [Q: What do you understand by query optimization?](#Q: What do you understand by query optimization?)
- [Transaction Management](#Transaction Management)
  - [Transaction](#Transaction)
    - [x] [Q: What is a checkpoint in DBMS?](#Q: What is a checkpoint in DBMS?)
    - [x] [Q: When does checkpoint occur in DBMS?](#Q: When does checkpoint occur in DBMS?)
    - [x] [Q: What do you mean by durability in DBMS?](#Q: What do you mean by durability in DBMS?)
    - [x] [Q: Explain ACID properties?](#Q: Explain ACID properties?)
  - [Concurrency Control](#Concurrency Control)
    - [x] [Q: Optimistic locking vs pessimistic locking?](#Q: Optimistic locking vs pessimistic locking?)
    - [x] [Q: What is the difference between a shared lock and exclusive lock?](#Q: What is the difference between a shared lock and exclusive lock?)
  - [Recovery System](#Recovery System)
- [System Architecture](#System Architecture)
  - [x] [Q: What is 2-Tier architecture?](#Q: What is 2-Tier architecture?)
  - [x] [Q: What is the 3-Tier architecture?](#Q: What is the 3-Tier architecture?)
- [Advanced Topics](#Advanced Topics)
- [References](#References)

## Main

## Introduction to DBMS

### Q: What is DBMS?

DBMS is a collection of programs that facilitates users to create and maintain a database. In other words, DBMS provides us an interface or tool for performing different operations such as the creation of a database, inserting data into it, deleting data from it, updating the data, etc. DBMS is a software in which data is stored in a more secure way as compared to the file-based system. Using DBMS, we can overcome many problems such as- data redundancy, data inconsistency, easy access, more organized and understandable, and so on. There is the name of some popular Database Management System- MySQL, Oracle, SQL Server, Amazon simple DB (Cloud-based), etc.

### Q: What is a database system?

The collection of database and DBMS software together is known as a database system. Through the database system, we can perform many activities such as-

The data can be stored in the database with ease, and there are no issues of data redundancy and data inconsistency.

The data will be extracted from the database using DBMS software whenever required. So, the combination of database and DBMS software enables one to store, retrieve and access data with considerate accuracy and security.

### Q: What are the advantages of DBMS?

- Redundancy control
- Restriction for unauthorized access
- Provides multiple user interfaces
- Provides backup and recovery
- Enforces integrity constraints
- Ensure data consistency
- Easy accessibility
- Easy data extraction and data processing due to the use of queries

### Q: What is RDBMS?

RDBMS stands for Relational Database Management Systems. It is used to maintain the data records and indices in tables. RDBMS is the form of DBMS which uses the structure to identify and access data concerning the other piece of data in the database. RDBMS is the system that enables you to perform different operations such as- update, insert, delete, manipulate and administer a relational database with minimal difficulties. Most of the time RDBMS use SQL language because it is easily understandable and is used for often.

### Q: What is data abstraction in DBMS?

Data abstraction in DBMS is a process of hiding irrelevant details from users. Because database systems are made of complex data structures so, it makes accessible the user interaction with the database.

**For example**: We know that most of the users prefer those systems which have a simple GUI that means no complex processing. So, to keep the user tuned and for making the access to the data easy, it is necessary to do data abstraction. In addition to it, data abstraction divides the system in different layers to make the work specified and well defined.

### Q: What are the three levels of data abstraction?

Following are three levels of data abstraction:

**Physical level**: It is the lowest level of abstraction. It describes how data are stored.

**Logical level**: It is the next higher level of abstraction. It describes what data are stored in the database and what the relationship among those data is.

**View level**: It is the highest level of data abstraction. It describes only part of the entire database.

**For example-** User interacts with the system using the GUI and fill the required details, but the user doesn't have any idea how the data is being used. So, the abstraction level is entirely high in VIEW LEVEL.

Then, the next level is for PROGRAMMERS as in this level the fields and records are visible and the programmers have the knowledge of this layer. So, the level of abstraction here is a little low in VIEW LEVEL.

And lastly, physical level in which storage blocks are described.

### Q: What do you mean by transparent DBMS?

The transparent DBMS is a type of DBMS which keeps its physical structure hidden from users. Physical structure or physical storage structure implies to the memory manager of the DBMS, and it describes how the data stored on disk.

### Q: What do you understand by Data Model?

The Data model is specified as a collection of conceptual tools for describing data, data relationships, data semantics and constraints. These models are used to describe the relationship between the entities and their attributes.

There is the number of data models:

- Hierarchical data model
- network model
- relational model
- Entity-Relationship model and so on.

## Relational Model and SQL

### Introduction to Relational Model

### Q: What is a database?

A Database is a logical, consistent and organized collection of data that it can easily be accessed, managed and updated. Databases, also known as electronic databases are structured to provide the facility of creation, insertion, updating of the data efficiently and are stored in the form of a file or set of files, on the magnetic disk, tapes and another sort of secondary devices. Database mostly consists of the objects (tables), and tables include of the records and fields. Fields are the basic units of data storage, which contain the information about a particular aspect or attribute of the entity described by the database. DBMS is used for extraction of data from the database in the form of the queries.

### Q: Define a Relation Schema and a Relation?

A Relation Schema is specified as a set of attributes. It is also known as table schema. It defines what the name of the table is. Relation schema is known as the blueprint with the help of which we can explain that how the data is organized into tables. This blueprint contains no data.

A relation is specified as a set of tuples. A relation is the set of related attributes with identifying key attributes

**See this example:**

Let r be the relation which contains set tuples (t1, t2, t3, ..., tn). Each tuple is an ordered list of n-values t=(v1,v2, ...., vn).

### Q: What is a degree of Relation?

The degree of relation is a number of attribute of its relation schema. A degree of relation is also known as Cardinality it is defined as the number of occurrence of one entity which is connected to the number of occurrence of other entity. There are three degree of relation they are one-to-one(1:1), one-to-many(1:M), many-to-one(M:M).

### Q: Describe the types of keys?

**There are following types of keys:**

**Primary key**: The Primary key is an attribute in a table that can uniquely identify each record in a table. It is compulsory for every table.

**Candidate key**: The Candidate key is an attribute or set of an attribute which can uniquely identify a tuple. The Primary key can be selected from these attributes.

**Super key**: The Super key is a set of attributes which can uniquely identify a tuple. Super key is a superset of the candidate key.

**Foreign key**: The Foreign key is a primary key from one table, which has a relationship with another table. It acts as a cross-reference between tables.

### Introduction to SQL

### Q: How many types of database languages are?

here are four types of database languages:

- **Data Definition Language (DDL)** e.g., CREATE, ALTER, DROP, TRUNCATE, RENAME, etc. All these commands are used for updating the data that?s why they are known as Data Definition Language.
- **Data Manipulation Language (DML)** e.g., SELECT, UPDATE, INSERT, DELETE, etc. These commands are used for the manipulation of already updated data that's why they are the part of Data Manipulation Language.
- **DATA Control Language (DCL)** e.g., GRANT and REVOKE. These commands are used for giving and removing the user access on the database. So, they are the part of Data Control Language.
- **Transaction Control Language (TCL)** e.g., COMMIT, ROLLBACK, and SAVEPOINT. These are the commands used for managing transactions in the database. TCL is used for managing the changes made by DML.

Database language implies the queries that are used for the update, modify and manipulate the data.

### Q: What is DDL (Data Definition Language)?

Data Definition Language (DDL) is a standard for commands which defines the different structures in a database. Most commonly DDL statements are CREATE, ALTER, and DROP. These commands are used for updating data into the database.

### Q: What is DML (Data Manipulation Language)?

DData Manipulation Language (DML) is a language that enables the user to access or manipulate data as organized by the appropriate data model. For example- SELECT, UPDATE, INSERT, DELETE.

**There is two type of DML:**

**Procedural DML or Low level DML:** It requires a user to specify what data are needed and how to get those data.

**Non-Procedural DML or High level DML:**It requires a user to specify what data are needed without specifying how to get those data.

### Q: What is the difference between a DELETE command and TRUNCATE command?

**DELETE command**: DELETE command is used to delete rows from a table based on the condition that we provide in a WHERE clause.

- DELETE command delete only those rows which are specified with the WHERE clause.
- DELETE command can be rolled back.
- DELETE command maintain a log, that's why it is slow.
- DELETE use row lock while performing DELETE function.

**TRUNCATE command**: TRUNCATE command is used to remove all rows (complete data) from a table. It is similar to the DELETE command with no WHERE clause.

- The TRUNCATE command removes all the rows from the table.
- The TRUNCATE command cannot be rolled back.
- The TRUNCATE command doesn't maintain a log. That's why it is fast.
- TRUNCATE use table log while performing the TRUNCATE function.

### Intermediate SQL

### Q: What is Join?

The Join operation is one of the most useful activities in relational algebra. It is most commonly used way to combine information from two or more relations. A Join is always performed on the basis of the same or related column. Most complex queries of SQL involve JOIN command.

There are following types of join:

- Inner joins: Inner join is of 3 categories. They are:
  - Theta join
  - Natural join
  - Equi join
- Outer joins: Outer join have three types. They are:
  - Left outer join
  - Right outer join
  - Full outer join

### Advanced SQL

### Q: What is stored procedure?

A stored procedure is a group of SQL statements that have been created and stored in the database. The stored procedure increases the reusability as here the code or the procedure is stored into the system and used again and again that makes the work easy, takes less time in processing and decreases the complexity of the system. So, if you have a code which you need to use again and again then save that code and call that code whenever it is required.

### Formal Relational Query Languages

### Q: What are the unary operations in Relational Algebra?

PROJECTION and SELECTION are the unary operations in relational algebra. Unary operations are those operations which use single operands. Unary operations are SELECTION, PROJECTION, and RENAME.

As in SELECTION relational operators are used for example - =,<=,>=, etc.

### Q: What is Relational Algebra?

Relational Algebra is a Procedural Query Language which contains a set of operations that take one or two relations as input and produce a new relationship. Relational algebra is the basic set of operations for the relational model. The decisive point of relational algebra is that it is similar to the algebra which operates on the number.

There are few fundamental operations of relational algebra:

- select
- project
- set difference
- union
- rename,etc.

### Q: What is Relational Calculus?

Relational Calculus is a Non-procedural Query Language which uses mathematical predicate calculus instead of algebra. Relational calculus doesn't work on mathematics fundamentals such as algebra, differential, integration, etc. That's why it is also known as predicate calculus.

There is two type of relational calculus:

- Tuple relational calculus
- Domain relational calculus

## Database Design

### Database Design and E-R Model

### Q: What is the E-R model?

E-R model is a short name for the Entity-Relationship model. This model is based on the real world. It contains necessary objects (known as entities) and the relationship among these objects. Here the primary objects are the entity, attribute of that entity, relationship set, an attribute of that relationship set can be mapped in the form of E-R diagram.

In E-R diagram, entities are represented by rectangles, relationships are represented by diamonds, attributes are the characteristics of entities and represented by ellipses, and data flow is represented through a straight line.

### Q: What is an entity?

The Entity is a set of attributes in a database. An entity can be a real-world object which physically exists in this world. All the entities have their attribute which in the real world considered as the characteristics of the object.

For example: In the employee database of a company, the employee, department, and the designation can be considered as the entities. These entities have some characteristics which will be the attributes of the corresponding entity.

### Q: What is an Entity type?

An entity type is specified as a collection of entities, having the same attributes. Entity type typically corresponds to one or several related tables in the database. A characteristic or trait which defines or uniquely identifies the entity is called entity type.

For example, a student has student_id, department, and course as its characteristics.

### Q: What is an Entity set?

The entity set specifies the collection of all entities of a particular entity type in the database. An entity set is known as the set of all the entities which share the same properties.

For example, a set of people, a set of students, a set of companies, etc.

### Q: What is an Extension of entity type?

An extension of an entity type is specified as a collection of entities of a particular entity type that are grouped into an entity set.

### Q: What is Weak Entity set?

An entity set that doesn't have sufficient attributes to form a primary key is referred to as a weak entity set. The member of a weak entity set is known as a subordinate entity. Weak entity set does not have a primary key, but we need a mean to differentiate among all those entries in the entity set that depend on one particular strong entity set.

### Q: What is the Relationship?

The Relationship is defined as an association among two or more entities. There are three type of relationships in DBMS-

**One-To-One**: Here one record of any object can be related to one record of another object.

**One-To-Many (many-to-one)**: Here one record of any object can be related to many records of other object and vice versa.

**Many-to-many**: Here more than one records of an object can be related to n number of records of another object.

### Q: What is an attribute?

An attribute refers to a database component. It is used to describe the property of an entity. An attribute can be defined as the characteristics of the entity. Entities can be uniquely identified using the attributes. Attributes represent the instances in the row of the database.

For example: If a student is an entity in the table then age will be the attribute of that student.

### Q: What are the integrity rules in DBMS?

Data integrity is one significant aspect while maintaining the database. So, data integrity is enforced in the database system by imposing a series of rules. Those set of integrity is known as the integrity rules.

**There are two integrity rules in DBMS:**

**Entity Integrity** : It specifies that "Primary key cannot have a NULL value."

**Referential Integrity**: It specifies that "Foreign Key can be either a NULL value or should be the Primary Key value of other relation

### Q: What do you mean by extension and intension?

**Extension:** The Extension is the number of tuples present in a table at any instance. It changes as the tuples are created, updated and destroyed. The actual data in the database change quite frequently. So, the data in the database at a particular moment in time is known as extension or database state or snapshot. It is time dependent.

**Intension:** Intension is also known as Data Schema and defined as the description of the database, which is specified during database design and is expected to remain unchanged. The Intension is a constant value that gives the name, structure of tables and the constraints laid on it.

### Relational Database Design

### Q: What is normalization?

Normalization is a process of analysing the given relation schemas according to their functional dependencies. It is used to minimize redundancy and also used to minimize insertion, deletion and update distractions. Normalization is considered as an essential process as it is used to avoid data redundancy, insertion anomaly, updation anomaly, deletion anomaly.

There most commonly used normal forms are:

- First Normal Form(1NF)
- Second Normal Form(2NF)
- Third Normal Form(3NF)
- Boyce & Codd Normal Form(BCNF)

### Q: 1NF vs 2NF vs 3NF vs BCNF?

**1NF** is the **First Normal Form**. It is the simplest type of normalization that you can implement in a database. The primary objectives of 1NF are to:

- Every column must have atomic (single value)
- To Remove duplicate columns from the same table
- Create separate tables for each group of related data and identify each row with a unique column

**2NF** is the **Second Normal Form**. A table is said to be 2NF if it follows the following conditions:

- The table is in 1NF, i.e., firstly it is necessary that the table should follow the rules of 1NF.
- Every non-prime attribute is fully functionally dependent on the primary key, i.e., every non-key attribute should be dependent on the primary key in such a way that if any key element is deleted, then even the non_key element will still be saved in the database.

**3NF** stands for **Third Normal Form**. A database is called in 3NF if it satisfies the following conditions:

- It is in second normal form.
- There is no transitive functional dependency.
- For example: X->Z

**Where:**
X->Y
Y does not -> X
Y->Z so, X->Z

**BCMF** stands for **Boyce-Codd Normal Form**. It is an advanced version of 3NF, so it is also referred to as 3.5NF. BCNF is stricter than 3NF.

A table complies with BCNF if it satisfies the following conditions:

- It is in 3NF.
- For every functional dependency X->Y, X should be the super key of the table. It merely means that X cannot be a non-prime attribute if Y is a prime attribute.

### Q: What is Denormalization?

Denormalization is the process of boosting up database performance and adding of redundant data which helps to get rid of complex data. Denormalization is a part of database optimization technique. This process is used to avoid the use of complex and costly joins. Denormalization doesn't refer to the thought of not to normalize instead of that denormalization takes place after normalization. In this process, firstly the redundancy of the data will be removed using normalization process than through denormalization process we will add redundant data as per the requirement so that we can easily avoid the costly joins.

### Q: What is functional Dependency?

Functional Dependency is the starting point of normalization. It exists when a relation between two attributes allow you to determine the corresponding attribute's value uniquely. The functional dependency is also known as database dependency and defines as the relationship which occurs when one attribute in a relation uniquely determines another attribute. It is written as A->B which means B is functionally dependent on A.

## Data Storage and Querying

### Storage and File Structure

### Q: What are the disadvantages of file processing systems?

- Inconsistent
- Not secure
- Data redundancy
- Difficult in accessing data
- Data isolation
- Data integrity
- Concurrent access is not possible
- Limited data sharing
- Atomicity problem

### Indexing and Hashing

### Q: Explain Index Depth, Density and Selectivity factors and how these factors affect index performance?

- **Index depth** is the number of levels from the index root node to the leaf nodes. An index that is quite deep will suffer from performance degradation problem. In contrast, an index with a large number of nodes in each level can produce a very flat index structure. An index with only 3 to 4 levels is very common.
- **Index density** is a measure of the lack of uniqueness of the data in a table. A dense column is one that has a high number of duplicates.
- **Index selectivity** is a measure of how many rows scanned compared to the total number of rows. An index with high selectivity means a small number of rows scanned when related to the total number of rows.

### Query Processing

### Query Optimization

### Q: What do you understand by query optimization?

The term query optimization specifies an efficient execution plan for evaluating a query that has the least estimated cost. The concept of query optimization came into the frame when there were a number of methods, and algorithms existed for the same task then the question arose that which one is more efficient and the process of determining the efficient way is known as query optimization.

There are many benefits of query optimization:

- It reduces the time and space complexity.
- More queries can be performed as due to optimization every query comparatively takes less time.
- User satisfaction as it will provide output fast

## Transaction Management

### Transaction

### Q: What is a checkpoint in DBMS?

The Checkpoint is a type of mechanism where all the previous logs are removed from the system and permanently stored in the storage disk.

There are two ways which can help the DBMS in recovering and maintaining the ACID properties, and they are- maintaining the log of each transaction and maintaining shadow pages. So, when it comes to log based recovery system, checkpoints come into existence. Checkpoints are those points to which the database engine can recover after a crash as a specified minimal point from where the transaction log record can be used to recover all the committed data up to the point of the crash.

### Q: When does checkpoint occur in DBMS?

A checkpoint is like a snapshot of the DBMS state. Using checkpoints, the DBMS can reduce the amount of work to be done during a restart in the event of subsequent crashes. Checkpoints are used for the recovery of the database after the system crash. Checkpoints are used in the log-based recovery system. When due to a system crash we need to restart the system then at that point we use checkpoints. So that, we don't have to perform the transactions from the very starting.

### Q: What do you mean by durability in DBMS?

Once the DBMS informs the user that a transaction has completed successfully, its effect should persist even if the system crashes before all its changes are reflected on disk. This property is called durability. Durability ensures that once the transaction is committed into the database, it will be stored in the non-volatile memory and after that system failure cannot affect that data anymore.

### Q: Explain ACID properties?

ACID properties are some basic rules, which has to be satisfied by every transaction to preserve the integrity. These properties and rules are:

**ATOMICITY:** Atomicity is more generally known as ?all or nothing rule.' Which implies all are considered as one unit, and they either run to completion or not executed at all.

**CONSISTENCY:** This property refers to the uniformity of the data. Consistency implies that the database is consistent before and after the transaction.

**ISOLATION:** This property states that the number of the transaction can be executed concurrently without leading to the inconsistency of the database state.

**DURABILITY:** This property ensures that once the transaction is committed it will be stored in the non-volatile memory and system crash can also not affect it anymore.

### Concurrency Control

### Q: Optimistic locking vs pessimistic locking?

The point is that Optimistic Locking is not a database feature, not for MySQL nor for others: optimistic locking is a practice that is applied using the DB with standard instructions.

| Optimistic Locking                                           | Pessimistic locking                                          |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Optimistic Locking is when you check if the record was updated by someone else before you commit the transaction. | Pessimistic locking is when you take an exclusive lock so that no one else can start modifying the record. |
| All thread to race for a lock and no transaction (can't rollback), must have one thread will get the lock and execute update, other threads will execute no affect rows. | All thread to race for a lock and have transaction, one thread get the lock, then execute it or rollback it. It may cause every threads don't execute update. |
| UPDATE test SET data = 'winner A', version = version + 1 WHERE id = 1 AND version = 0;<br>UPDATE test SET data = 'winner B', version = version + 1 WHERE id = 1 AND version = 0; | START TRANSACTION; <br>UPDATE test SET data = 'winner A', version = version + 1 WHERE id = 1 AND version = 0;<br>{If affectRows == 1}<br>commit transaction<br>{else}<br>rollback transaction |



**Pessimistic Locking**

Pessimistic Lock is where you assume that all the users are trying to access the same record and it literally locks the record exclusively for the first started transaction until it is completed successfully or failed. Then the lock is released and the next transaction on the record is handled in the same way.

Pessimistic Lock provides better integrity on the data however management of the lock is harder and if you fail to manage that, your application may encounter **deadlocks**.

1. In our case, if we apply Pessimistic Lock, the first user to come and buy the last item in the stock will click on “Purchase”.
2. This will lock the object until the payment is completed or failed.
3. Let’s say User A was able to pay for it and the stock value for that item is set to 0 now.
4. All the other users have to wait during this process.
5. Now all the other users will see that the item went out of stocks, and cannot do anything with the item.

**Optimistic Locking**

Optimistic Lock is where you manage your data by checking a special value in the database — it is often a version number, timestamp, date, etc.— before you read/write to the data to make sure that the data you are dealing with is not stale/old/changed since you’ve last viewed. If the data is stale, the transaction is not completed successfully and an error is thrown to indicate that. Something like: *“The record you attempted to edit was modified by another user after you got the original value”.*

1. In our case, if we apply Optimistic Lock, the first user to come and buy the last item in the stock will click on “Purchase”.
2. Let’s say User A was able to pay for it and before the payment step the stock value is checked before committing to change it from 1 to 0.
3. If the version numbers match the operation is committed and the item goes out of stock.
4. Now all the other users that try to purchase that the item will be warned about that the item is no longer available, right at the moment they try to buy, pay or add it to their baskets.

### Q: What is the difference between a shared lock and exclusive lock?

**Shared lock**: Shared lock is required for reading a data item. In the shared lock, many transactions may hold a lock on the same data item. When more than one transaction is allowed to read the data items then that is known as the shared lock.

**Exclusive lock**: When any transaction is about to perform the write operation, then the lock on the data item is an exclusive lock. Because, if we allow more than one transaction then that will lead to the inconsistency in the database.

### Recovery System

## System Architecture

### Q: What is 2-Tier architecture?

The **2-Tier architecture** is the same as basic client-server. In the two-tier architecture, applications on the client end can directly communicate with the database at the server side.

### Q: What is the 3-Tier architecture?

The 3-Tier architecture contains another layer between the client and server. Introduction of 3-tier architecture is for the ease of the users as it provides the GUI, which, make the system secure and much more accessible. In this architecture, the application on the client-end interacts with an application on the server which further communicates with the database system.

## Advanced Topics



## References

- [DBMS Interview Questions - javatpoint](https://www.javatpoint.com/dbms-interview-questions)
- [TIL-9: Optimistic vs. Pessimistic Locking](https://medium.com/@recepinancc/til-9-optimistic-vs-pessimistic-locking-79a349b76dc8)
- [Optimistic locking in MySQL](https://stackoverflow.com/questions/17431338/optimistic-locking-in-mysql)
- [How to correctly implement optimistic locking in MySQL](https://dba.stackexchange.com/questions/28879/how-to-correctly-implement-optimistic-locking-in-mysql)