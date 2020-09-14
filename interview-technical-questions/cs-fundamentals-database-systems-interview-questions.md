# Database Systems Interview Questions

### Content

- Introduction to DBMS
  - [ ] Q: What is DBMS?
  - [ ] Q: What is a database system?
  - [ ] Q: What are the advantages of DBMS?
  - [ ] Q: What is RDBMS?
  - [ ] Q: What is data abstraction in DBMS?
  - [ ] Q: What are the three levels of data abstraction?
  - [ ] Q: What do you mean by transparent DBMS?
- Relational Model and SQL
  - Introduction to Relational Model
    - [ ] Q: What is a database?
    - [ ] Q: How many types of database languages are?
    - [ ] Q: What do you understand by Data Model?
    - [ ] Q: Define a Relation Schema and a Relation?
    - [ ] Q: What is a degree of Relation?
    - [ ] Q: What is the Relationship?
    - [ ] Q: What is DDL (Data Definition Language)?
    - [ ] Q: What is DML (Data Manipulation Language)?
  - introduction to SQL
  - Intermediate SQL
  - Advanced SQL
  - Formal Relational Query Languages (Relational Algebra, Tuple Relational Calculus, Domain Relational Calculus)
    - [ ] Q: What are the unary operations in Relational Algebra?
    - [ ] Q: What is Relational Algebra?
    - [ ] Q: What is Relational Calculus?
- Database Design
  - Database Design and E-R Model
  - Relational Database Design
    - [ ] Database Design Norm Forms
  - Application Design and Development
- Data Storage and Querying
  - Storage and File Structure
    - [ ] Q: What are the disadvantages of file processing systems?
  - Indexing and Hashing
  - Query Processing
    - [ ] Q: Explain Index Depth, Density and Selectivity factors and how these factors affect index performance?
  - Query Optimization
    - [ ] Q: What do you understand by query optimization?
- Transaction Management
  - Transaction
    - [ ] Q: What is a checkpoint in DBMS?
    - [ ] Q: When does checkpoint occur in DBMS?
  - Concurrency Control
    - [ ] Q: What are Optimistic locking and pessimistic locking
  - Recovery System
- System Architecture
- Advanced Topics
- References

## Main

## Introduction to DBMS

## Relational Model and SQL

## Database Design

## Data Storage and Querying

### Q: Explain Index Depth, Density and Selectivity factors and how these factors affect index performance?

- **Index depth** is the number of levels from the index root node to the leaf nodes. An index that is quite deep will suffer from performance degradation problem. In contrast, an index with a large number of nodes in each level can produce a very flat index structure. An index with only 3 to 4 levels is very common.
- **Index density** is a measure of the lack of uniqueness of the data in a table. A dense column is one that has a high number of duplicates.
- **Index selectivity** is a measure of how many rows scanned compared to the total number of rows. An index with high selectivity means a small number of rows scanned when related to the total number of rows.

## Transaction Management

## System Architecture

## Advanced Topics



## References