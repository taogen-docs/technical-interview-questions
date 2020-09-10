# MySQL Interview Questions

### Content

- [Introduction to MySQL](#Introduction to MySQL)
  - [x] [Q: What is MySQL?](#Q: What is MySQL?)
  - [x] [Q: What are the technical features of MySQL?](#Q: What are the technical features of MySQL?)
  - [x] [Q: Why MySQL is used?](#Q: Why MySQL is used?)
  - [x] [Q: What are the advantages of MySQL when compared with Oracle?](#Q: What are the advantages of MySQL when compared with Oracle?)
  - [x] [Q: What are the disadvantages of MySQL?](#Q: What are the disadvantages of MySQL?)
  - [x] [Q: In which language MySQL has been written?](#Q: In which language MySQL has been written?)
- [MySQL Basics](#MySQL Basics)
  - How to get Information of MySQL
    - [x] [Q: How to get current MySQL version?](#Q: How to get current MySQL version?)
    - [x] [Q: How to get the current date in MySQL?](#Q: How to get the current date in MySQL?)
  - DBMS Basics
    - [x] [Q: What is the difference between primary key and candidate key?](#Q: What is the difference between primary key and candidate key?)
  - MySQL Basics
    - [x] [Q: What are the different tables present in MySQL?](#Q: What are the different tables present in MySQL?)
    - [x] [Q: Are table names in MySQL case sensitive?](#Q: Are table names in MySQL case sensitive?)
    - [x] [Q: What is the default port for MySQL Server?](#Q: What is the default port for MySQL Server?)
    - [x] [Q: How do you login to MySql using Unix shell?](#Q: How do you login to MySql using Unix shell?)
    - [x] [Q: How does indexing works in MySQL?](#Q: How does indexing works in MySQL?)
    - [x] [Q: How many columns can you create for an index?](#Q: How many columns can you create for an index?)
    - [x] [Q: What is the save point in MySQL?](#Q: What is the save point in MySQL?)
    - [x] [Q: What is MySQL data directory?](#Q: What is MySQL data directory?)
    - [x] [Q: How do you determine the location of MySQL data directory?](#Q: How do you determine the location of MySQL data directory?)
- [General MySQL Use](#General MySQL Use)
  - [SQL Statement](#SQL Statement)
    - [x] [Q: What are DDL, DML, and DCL?](#Q: What are DDL, DML, and DCL?)
    - [DDL](#DDL)
      - [x] [Q: What happens when the column is set to AUTO INCREMENT and if you reach maximum value in the table?](#Q: What happens when the column is set to AUTO INCREMENT and if you reach maximum value in the table?)
      - [x] [Q: How can you see all indexes defined for a table?](#Q: How can you see all indexes defined for a table?)
      - [x] [Q: What are the objects can be created using CREATE statement?](#Q: What are the objects can be created using CREATE statement?)
      - [x] [Q: How to add columns in MySQL?](#Q: How to add columns in MySQL?)
      - [x] [Q: How to import a CSV file in MySQL?](#Q: How to import a CSV file in MySQL?)
      - [x] [Q: How to check database size in MySQL?](#Q: How to check database size in MySQL?)
      - [x] [Q: What is the difference between TRUNCATE and DELETE in MySQL?](#Q: What is the difference between TRUNCATE and DELETE in MySQL?)
    - [DML](#DML)
      - [x] [Q: What is the usage of the "i-am-a-dummy" flag in MySQL?](#Q: What is the usage of the "i-am-a-dummy" flag in MySQL?)
    - [DQL](#DQL)
      - [x] [Q: What is the difference between the LIKE and REGEXP operators?](#Q: What is the difference between the LIKE and REGEXP operators?)
      - [x] [Q: How MySQL Optimizes DISTINCT?](#Q: How MySQL Optimizes DISTINCT?)
      - [x] [Q: How to display top 50 rows?](#Q: How to display top 50 rows?)
      - [x] [Q: How to find the second highest salary in MySQL?](#Q: How to find the second highest salary in MySQL?)
  - [Character Sets, Collations, Unicode](#Character Sets, Collations, Unicode)
  - [Language Structure](#Language Structure)
    - [x] [Q: What are the column comparisons operators?](#Q: What are the column comparisons operators? ) 
  - [Data Types](#Data Types)
    - [x] [Q: What are Data Types in MySQL?](#Q: What are Data Types in MySQL?)
    - [x] [Q: What are string types?](#Q: What are string types?)
    - [x] [Q: How to represent ENUMs and SETs internally?](#Q: How to represent ENUMs and SETs internally?)
    - [x] [Q: What is the usage of ENUMs in MySQL?](#Q: What is the usage of ENUMs in MySQL?)
    - [x] [Q: What does a TIMESTAMP do on UPDATE CURRENT_TIMESTAMP data type?](#Q: What does a TIMESTAMP do on UPDATE CURRENT_TIMESTAMP data type?)
    - [x] [Q: How can we convert between Unix & MySQL timestamps?](#Q: How can we convert between Unix & MySQL timestamps?)
    - [x] [Q: How to enter Characters as HEX Numbers?](#Q: How to enter Characters as HEX Numbers?)
    - [x] [Q: What are the nonstandard string types?](#Q: What are the nonstandard string types?)
    - [Data Types Comparation](#Data Types Comparation)
      - [x] [Q: Differentiate between FLOAT and DOUBLE?](#Q: Differentiate between FLOAT and DOUBLE?)
      - [x] [Q: Differentiate CHAR_LENGTH and LENGTH?](#Q: Differentiate CHAR_LENGTH and LENGTH?)
      - [x] [Q: Difference between CHAR and VARCHAR?](#Q: Difference between CHAR and VARCHAR?)
      - [x] [Q: What is the difference between BLOB AND TEXT?](#Q: What is the difference between BLOB AND TEXT?)
      - [x] [Q: What is the difference between UNIX timestamps and MySQL timestamps?](#Q: What is the difference between UNIX timestamps and MySQL timestamps?)
  - [Functions and Operations](#Functions and Operations)
    - [x] [Q: What are all the Common SQL Function?](#Q: What are all the Common SQL Function?)
    - [x] [Q: What is REGEXP?](#Q: What is REGEXP? ) 
    - [x] [Q: What is the different between NOW() and CURRENT_DATE()?](#Q: What is the different between NOW() and CURRENT_DATE()?)
  - [Stored Programs](#Stored Programs)
    - [x] [Q: What is a trigger in MySQL?](#Q: What is a trigger in MySQL?)
    - [x] [Q: How many TRIGGERS are allowed in MySql table?](#Q: How many TRIGGERS are allowed in MySql table? )
    - [x] [Q: How to create a Stored Procedure in MySQL?](#Q: How to create a Stored Procedure in MySQL?)
    - [x] [Q: How to execute a stored procedure in MySQL?](#Q: How to execute a stored procedure in MySQL?)
    - [x] [Q: How to create a View in MySQL?](#Q: How to create a View in MySQL?)
    - [x] [Q: How to create a Trigger in MySQL?](#Q: How to create a Trigger in MySQL?)
  - [Query Optimization](#Query Optimization)
  - [Storage Engines](#Storage Engines)
    - [x] [Q: What storage engines are used in MySQL?](#Q: What storage engines are used in MySQL? ) 
    - [x] [Q: What is InnoDB Storage Engine?](#Q: What is InnoDB Storage Engine?)
    - [x] [Q: What is MyISAM Storage Engine?](#Q: What is MyISAM Storage Engine?)
    - [ ] [Q: What is MEMORY Storage Engine?](#Q: What is MEMORY Storage Engine?)
    - [x] [Q: What are Heap tables?](#Q: What are Heap tables?)
    - [x] [Q: What is the difference between the heap table and the temporary table?](#Q: What is the difference between the heap table and the temporary table?)
    - [x] [Q: How do you control the max size of a HEAP table?](#Q: How do you control the max size of a HEAP table?)
  - [InnoDB Cluster](#InnoDB Cluster)
  - [Partitioning](#Partitioning)
- [MySQL Programming Interfaces](#MySQL Programming Interfaces)
  - [x] [Q: What are the drivers in MySQL?](#Q: What are the drivers in MySQL?) 
- [MySQL Administration](#MySQL Administration)
  - [General MySQL Administration](#General MySQL Administration)
  - [The MySQL Data Directory](#The MySQL Data Directory)
  - [Access Control and Security](#Access Control and Security)
    - [x] [Q: Explain Access Control Lists?](#Q: Explain Access Control Lists?)
  - [Database Maintenance, Backup/Recovery, and Republication](#Database Maintenance, Backup/Recovery, and Republication)
- [References](#References)

## Main

## Introduction to MySQL

### Q: What is MySQL?

MySQL is an open source DBMS which is built, supported and distributed by MySQL AB (now acquired by Oracle).

Other Answer 1

MySQL is a multithreaded, multi-user SQL database management system which has more than 11 million installations. It is the world's second most popular and widely-used open source database. It is interesting how MySQL name was given to this query language. The term My is coined by the name of the daughter of co-founder Michael Widenius's daughter, and SQL is the short form of Structured Query Language. Using MySQL is free of cost for the developer, but enterprises have to pay a license fee to Oracle.

Formerly MySQL was initially owned by a for-profit firm MySQL AB, then Sun Microsystems bought it, and then Oracle bought Sun Microsystems, so Oracle currently owns MySQL.

[MySQL](https://www.javatpoint.com/mysql-tutorial) is an Oracle-supported Relational Database Management System (RDBMS) based on structured query language. MySQL supports a wide range of operating systems, most famous of those include Windows, Linux & UNIX. Although it is possible to develop a wide range of applications with MySQL, it is only used for web applications & online publishing. It is a fundamental part of an open-source enterprise known as Lamp.

### Q: What are the technical features of MySQL?

MySQL database software is a client or server system which includes

- Multithreaded SQL server supporting various client programs and libraries
- Different backend
- Wide range of application programming interfaces and
- Administrative tools.

Other Answer 1

MySQL has the following technical specifications -

- Flexible structure
- High performance
- Manageable and easy to use
- Replication and high availability
- Security and storage management
- Drivers
- Graphical Tools
- MySQL Enterprise Monitor
- MySQL Enterprise Security
- JSON Support
- Replication & High-Availability
- Manageability and Ease of Use
- OLTP and Transactions
- Geo-Spatial Support

### Q: Why MySQL is used?

MySQL database server is reliable, fast and very easy to use.  This software can be downloaded as freeware and can be downloaded from the internet.

Other Answer 1

- First of all, the MYSQL server is free to use for developers and small enterprises.
- MySQL server is open source.
- MySQL's community is tremendous and supportive; hence any help regarding MySQL is resolved as soon as possible.
- MySQL has very stable versions available, as MySQL has been in the market for a long time. All bugs arising in the previous builds have been continuously removed, and a very stable version is provided after every update.
- The MySQL database server is very fast, reliable, and easy to use. You can easily use and modify the software. MySQL software can be downloaded free of cost from the internet.

### Q: What are the advantages of MySQL when compared with Oracle? 

- MySQL is open source software which is available at any time and has no cost involved.
- MySQL is portable
- GUI with command prompt.
- Administration is supported using MySQL Query Browser

### Q: What are the disadvantages of MySQL?

1. MySQL is not so efficient for large scale databases.
2. It does not support COMMIT and STORED PROCEDURES functions version less than 5.0.
3. Transactions are not handled very efficiently.
4. The functionality of MySQL is highly dependent on other addons.
5. Development is not community-driven.

### Q: In which language MySQL has been written?

MySQL is written in C and C++, and its SQL parser is written in yacc.

## MySQL Basics

### Q: What are the different tables present in MySQL?

Total 5 types of tables are present:

- MyISAM
- Heap
- Merge
- INNO DB
- ISAM

InnoDB is the default storage engine as of MySQL 8 .

### Q: Are table names in MySQL case sensitive?

> In MySQL, databases correspond to directories within the data directory. Each table within a database corresponds to at least one file within the database directory (and possibly more, depending on the storage engine). Triggers also correspond to files. **Consequently, the case sensitivity of the underlying operating system plays a part in the case sensitivity of database, table, and trigger names.** This means such names are not case-sensitive in Windows, but are case-sensitive in most varieties of Unix. One notable exception is macOS, which is Unix-based but uses a default file system type (HFS+) that is not case-sensitive. However, macOS also supports UFS volumes, which are case-sensitive just as on any Unix. See [Section 1.7.1, “MySQL Extensions to Standard SQL”](https://dev.mysql.com/doc/refman/8.0/en/extensions-to-ansi.html). The [`lower_case_table_names`](https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_lower_case_table_names) system variable also affects how the server handles identifier case sensitivity, as described later in this section.
>
> -- MySQL 8.0 Reference Manual - 9.2.3 Identifier Case Sensitivity

Database and table names are not **case sensitive** in Windows, and **case sensitive** in most varieties of Unix or **Linux**.

To resolve the issue, set the lower_case_table_names to 1:

```sql
lower_case_table_names=1
```

This will make all your tables lowercase, no matter how you write them.

### Q: What is the default port for MySQL Server?

The default port for MySQL server is 3306.

### Q: What is the difference between primary key and candidate key?

Every row of a table is identified uniquely by primary key. There is only one primary key for a table.

Primary Key is also a candidate key. By common convention, candidate key can be designated as primary and which can be used for any foreign key references.

### Q: How do you login to MySql using Unix shell?

We can login through this command:

```
mysql -h hostname -u <UserName> -p <password>
```



### Q: How to get current MySQL version?

Method 1: 

```sql
mysql> SELECT VERSION ();
```

Output

````
+-----------+
| version() |
+-----------+
| 8.0.19    |
+-----------+
1 row in set (0.00 sec)
````

Method 2:

```
$ mysql --version
```

Output

```
mysql  Ver 8.0.19 for Win64 on x86_64 (MySQL Community Server - GPL)
```

### Q: How to get the current date in MySQL?

To get current date, use the following syntax:

```sql
SELECT CURRENT_DATE();
```



### Q: How does indexing works in MySQL?

Indexing is a process to find an unordered list into an ordered list. It helps in maximizing the query's efficiency while searching on tables in MySQL. The working of MySQL indexing is similar to the book index.

Suppose we have a book and want to get information about, say, searching. Without indexing, it is required to go through all pages one by one, until the specific topic was not found. On the other hand, an index contains a list of keywords to find the topic mentioned on pages. Then, we can flip to those pages directly without going through all pages.

### Q: How many columns can you create for an index?

You can a create maximum of 16 indexed columns for a standard table.

### Q: What is the save point in MySQL?

A defined point in any transaction is known as savepoint.

SAVEPOINT is a statement in MySQL, which is used to set a named transaction savepoint with the name of the identifier.

### Q: What is MySQL data directory?

MySQL data directory is a place where MySQL stores its data. Each subdirectory under this data dictionary represents a MySQL database. By default, the information managed my MySQL server mysqld is stored in the data directory.

### Q: How do you determine the location of MySQL data directory?

The default location of MySQL data directory in windows is C:\mysql\data or C:\Program Files\MySQL\MySQL Server 5.0 \data.

## General MySQL Use

### SQL Statement

### Q: What are DDL, DML, and DCL?

Majorly SQL commands can be divided into three categories, i.e., DDL, DML & DCL. 

Data Definition Language (DDL) deals with all the database schemas, and it defines how the data should reside in the database. Commands like CreateTABLE and ALTER TABLE are part of DDL.

Data Manipulative Language (DML) deals with operations and manipulations on the data. The commands in DML are Insert, Select, etc.

Data Control Languages (DCL) are related to the Grant and permissions. In short, the authorization to access any part of the database is defined by these.

#### DDL

### Q: What happens when the column is set to AUTO INCREMENT and if you reach maximum value in the table?

It stops incrementing. Any further inserts are going to produce an error, since the key has been used already.

### Q: How can you see all indexes defined for a table?

Indexes are defined for the table by:

```sql
SHOW INDEX FROM <tablename>;
```

### Q: What are the objects can be created using CREATE statement?

Following objects are created using CREATE statement:

- DATABASE
- EVENT
- FUNCTION
- INDEX
- PROCEDURE
- TABLE
- TRIGGER
- USER
- VIEW

### Q: How to add columns in MySQL?

A column is a series of cells in a table that stores one value for each row in a table. We can add columns in an existing table using the ALTER TABLE statement as follows:

```sql
ALTER TABLE table_name     
    ADD COLUMN column_name column_definition [FIRST|AFTER existing_column];
```

### Q: How to import a CSV file in MySQL?

MySQL allows us to import the CSV (comma separated values) file into a database or table. A CSV is a plain text file that contains the list of data and can be saved in a tabular format. MySQL provides the LOAD DATA INFILE statement to import a CSV file. This statement is used to read a text file and import it into a database table very quickly. The full syntax to import a CSV file is given below:

```sql
LOAD DATA INFILE 'C:/ProgramData/MySQL/MySQL Server 8.0/Uploads/filename.csv'
INTO TABLE tablename
FIELDS TERMINATED BY ','
OPTIONALLY ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 ROWS;
```

### Q: How to check database size in MySQL?

MySQL allows us to query the information_schema.tables table to get the information about the tables and databases. It will return the information about the data length, index length, collation, creation time, etc. We can check the size of the database on the server using the below syntax:

```sql
SELECT table_schema AS 'Database Name',
SUM(data_length + index_length) 'Size in Bytes',
ROUND(SUM(data_length + index_length) / 1024 / 1024, 2) 'Size in MB'
FROM information_schema.tables
WHERE table_schema = 'testdb'
GROUP BY table_schema;
```

If we want to check the size of the table in a specific database, use the following statement:

```sql
SELECT table_name AS 'Table Name',
ROUND(((data_length + index_length) / 1024 / 1024), 2) AS 'Size in MB'
FROM information_schema.TABLES
WHERE table_schema = 'testdb'
ORDER BY (data_length + index_length) DESC;
```

### Q: What is the difference between TRUNCATE and DELETE in MySQL?

| TRUNCATE                                                     | DELETE                                |
| ------------------------------------------------------------ | ------------------------------------- |
| It is only use to delete all rows of a relation (table) in one go | It deletes rows                       |
| RUNCATE is a DDL command                                     | DELETE is a DML command               |
| TRUNCATE cannot be used with indexed views                   | DELETE can be used with indexed views |
| It is comparatively faster than delete command as it deletes all the rows | It is slower than TRUNCATE            |
| We can’t restore the tuples of the table by using the “ROLLBACK” command | can using ROLLBACK                    |



#### DML

### Q: What is the usage of the "i-am-a-dummy" flag in MySQL?

In MySQL, the "i-am-a-dummy" flag makes the MySQL engine to deny the UPDATE and DELETE commands unless the WHERE clause is present.

#### DQL

### Q: What is the difference between the LIKE and REGEXP operators?

LIKE operator is used to express with %, whereas REGEXP use  ^. 

```sql
SELECT * FROM employee WHERE emp_name LIKE "%b";
SELECT * FROM employee WHERE emp_name REGEXP "^b";
```

### Q: How MySQL Optimizes DISTINCT?

DISTINCT is converted to a GROUP BY on all columns and it will be combined with ORDER BY clause.

```sql
SELECT DISTINCT t1.a FROM t1,t2 where t1.a=t2.a;
```

### Q: How to display top 50 rows?

In MySql, top 50 rows are displayed by using this following query:

```sql
SELECT * FROM LIMIT 0,50;
```

### Q: How to find the second highest salary in MySQL?

MySQL uses the LIMIT keyword, which can be used to limit the result set. It will allow us to get the first few rows, last few rows, or range of rows. It can also be used to find the second, third, or nth highest salary. It ensures that you have use order by clause to sort the result set first and then print the output that provides accurate results. The following query is used to get the second highest salary in MySQL:

```sql
SELECT salary
FROM (SELECT salary FROM employees ORDER BY salary DESC LIMIT 2) AS Emp ORDER BY salary LIMIT 1;
```

There are some other ways to find the second highest salary in MySQL, which are given below:

This statement uses subquery and IN clause to get the second highest salary:

```sql
SELECT MAX(salary)
FROM employees
WHERE salary NOT IN ( SELECT Max(salary) FROM employees);
```

This query uses subquery and < operator to return the second highest salary:

```sql
SELECT MAX(salary) From employees
WHERE salary < ( SELECT Max(salary) FROM employees);
```

Find nth highest salary from a table in a MySQL query?

```sql
select distinct(salary) from employee order by salary desc limit n-1,1
```



### Character Sets, Collations, Unicode

### Language Structure

### Q: What are the column comparisons operators? 

The = , <>, <=, <, >=, >,<<,>>, <=>, AND, OR, or LIKE operators are used in column comparisons in SELECT statements.

### Data Types

### Q: What are Data Types in MySQL?

Numeric Data Types

- **bit** - A bit-value type. M indicates the number of bits per value, from 1 to 64. The default is 1 if M is omitted. Insert by int value convert from M bits binary value, binary value b'', or one bit by true or false. Get by boolean value(when it's M=1 or bit(1)) or int value(when M > 1). For example, when column is BIT(2), You can insert int value 3(represent 11), or insert b'11'.
* **bool**, boolean - These types are synonyms for TINYINT(1). A value of zero is considered false. Nonzero values are considered true.
* **tinyint** - 1 byte, A very small integer. The signed range is -128 to 127. The unsigned range is 0 to 255.
* **smallint** - 2 bytes, A small integer. The signed range is -32768 to 32767. The unsigned range is 0 to 65535.
* **mediumint** - 3 bytes, A medium-sized integer. The signed range is -8388608 to 8388607. The unsigned range is 0 to 16777215.
* **integer** (int) - 4 bytes, A normal-size integer. The signed range is -2147483648 to 2147483647. The unsigned range is 0 to 4294967295.
* **bigint** - 8 bytes, A large integer. The signed range is -9223372036854775808 to 9223372036854775807. The unsigned range is 0 to 18446744073709551615.
* **decimal(M, D)** (dec, fixed, numeric) - A packed “exact” fixed-point number. M is the total number of digits (the precision) and D is the number of digits after the decimal point (the scale). The decimal point and (for negative numbers) the - sign are not counted in M.
* **float** - A small (single-precision) floating-point number. Permissible values are -3.402823466E+38 to -1.175494351E-38, 0, and 1.175494351E-38 to 3.402823466E+38. These are the theoretical limits, based on the IEEE standard. The actual range might be slightly smaller depending on your hardware or operating system.
* **double** precision (double) - A normal-size (double-precision) floating-point number. Permissible values are -1.7976931348623157E+308 to -2.2250738585072014E-308, 0, and 2.2250738585072014E-308 to 1.7976931348623157E+308.
* **real** - default a synonym for DOUBLE. If the REAL_AS_FLOAT SQL mode is enabled, REAL is a synonym for FLOAT rather than DOUBLE.

String Data Types

- Character Strings
  * **CHAR** - A fixed-length string that is always right-padded with spaces to the specified length when stored. M represents the column length in characters. The range of M is 0 to 255(2^8-1). If M is omitted, the length is 1.
  * VARCHAR - A variable-length string. M represents the maximum column length in characters. The range of M is 0 to 65,535(2^16-1).
  * **TINYTEXT** - A TEXT column with a maximum length of 255 (28 − 1) characters.
  * **TEXT** - A TEXT column with a maximum length of 65,535 (2^16 − 1) characters. The effective maximum length is less if the value contains multibyte characters. Each TINYTEXT value is stored using a 1-byte length prefix that indicates the number of bytes in the value.
  * **MEDIUMTEXT** - A TEXT column with a maximum length of 16,777,215 (2^24 − 1) characters.
  * **LONGTEXT** - A TEXT column with a maximum length of 4,294,967,295 or 4GB (2^32 − 1) characters.
- Binary Strings
  * **BINARY** - Max bytes 255, The BINARY type is similar to the CHAR type, but stores binary byte strings rather than nonbinary character strings. An optional length M represents the column length in bytes. If omitted, M defaults to 1.
  * **VARBINARY** - The VARBINARY type is similar to the VARCHAR type, but stores binary byte strings rather than nonbinary character strings. M represents the maximum column length in bytes.
  * **TINYBLOB**
  * **BLOB(M)** - A BLOB column with a maximum length of 65,535 (2^16 − 1) bytes. Each BLOB value is stored using a 2-byte length prefix that indicates the number of bytes in the value. An optional length M can be given for this type.
  * MEDIUMBLOB
  * **LONGBLOB**
- Other Strings
  * **ENUM** - An enumeration. A string object that can have only one value, chosen from the list of values 'value1', 'value2', ..., NULL or the special '' error value. ENUM values are represented internally as integers.
  * SET - A set. A string object that can have zero or more values, each of which must be chosen from the list of values 'value1', 'value2', ... SET values are represented internally as integers.

Date Time Data Types

- **DATE** - A date. The supported range is '1000-01-01' to '9999-12-31'. MySQL displays DATE values in 'YYYY-MM-DD' format, but permits assignment of values to DATE columns using either strings or numbers.
* **DATETIME** - A date and time combination. The supported range is '1000-01-01 00:00:00.000000' to '9999-12-31 23:59:59.999999'. MySQL displays DATETIME values in 'YYYY-MM-DD hh:mm:ss[.fraction]' format, but permits assignment of values to DATETIME columns using either strings or numbers.
* **TIMESTAMP** - A timestamp. The range is '1970-01-01 00:00:01.000000' UTC to '2038-01-19 03:14:07.999999' UTC.
* **TIME** - A time. The range is '-838:59:59.000000' to '838:59:59.000000'. MySQL displays TIME values in 'hh:mm:ss[.fraction]' format, but permits assignment of values to TIME columns using either strings or numbers.
* **YEAR** - A year in 4-digit format. MySQL displays YEAR values in YYYY format, but permits assignment of values to YEAR columns using either strings or numbers. Values display as 1901 to 2155, or 0000.

JSON Data Types

Array Data Types

XML Data Types

### Q: What are string types?

The string types are:

- SET
- BLOB
- ENUM
- CHAR
- TEXT
- VARCHAR

### Q: How to represent ENUMs and SETs internally? 

ENUMs and SETs are used to represent powers of two because of storage optimizations.

### Q: What is the usage of ENUMs in MySQL?

ENUM is a string object used to specify set of predefined values and that can be used during table creation.

```sql
Create table size(name ENUM('Small', 'Medium','Large');
```



### Q: What does a TIMESTAMP do on UPDATE CURRENT_TIMESTAMP data type?

TIMESTAMP column is updated with Zero when the table is created.  UPDATE CURRENT_TIMESTAMP modifier updates the timestamp field to current time whenever there is a change in other fields of the table.

### Q: How can we convert between Unix & MySQL timestamps?

UNIX_TIMESTAMP is the command which converts from MySQL timestamp to Unix timestamp

FROM_UNIXTIME is the command which converts from Unix timestamp to MySQL timestamp.

### Q: How to enter Characters as HEX Numbers?

If you want to enter characters as HEX numbers, you can enter HEX numbers with single quotes and a prefix of (X), or just prefix HEX numbers with (Ox).

A HEX number string will be automatically converted into a character string, if the expression context is a string.

### Q: What are the nonstandard string types?

Following are Non-Standard string types:

- TINYTEXT
- TEXT
- MEDIUMTEXT
- LONGTEXT

#### Data Types Comparation

### Q: Differentiate between FLOAT and DOUBLE?

Following are differences for FLOAT and DOUBLE:

- Floating point numbers are stored in FLOAT with eight place accuracy and it has four bytes.

- Floating point numbers are stored in DOUBLE with accuracy of 18 places and it has eight bytes.

### Q: Differentiate CHAR_LENGTH and LENGTH?

CHAR_LENGTH  is character count whereas the LENGTH is byte count. The numbers are same for Latin characters but they are different for Unicode and other encodings.

### Q: Difference between CHAR and VARCHAR? 

Following are the differences between CHAR and VARCHAR:

- CHAR and VARCHAR types differ in storage and retrieval
- CHAR column length is fixed to the length that is declared while creating table. The length value ranges from 1 and 255
- When CHAR values are stored then they are right padded using spaces to specific length. Trailing spaces are removed when CHAR values are retrieved.

Other Answer

- CHAR and VARCHAR have differed in storage and retrieval.
- CHAR column length is fixed, while VARCHAR length is variable.
- The maximum no. of character CHAR data types can hold is 255 characters, while VARCHAR can hold up to 4000 characters.
- CHAR is 50% faster than VARCHAR.
- CHAR uses static memory allocation, while VARCHAR uses dynamic memory allocation.

### Q: What is the difference between BLOB AND TEXT?

A BLOB is a binary large object that can hold a variable amount of data. There are four types of BLOB –

- TINYBLOB
- BLOB
- MEDIUMBLOB and
- LONGBLOB

They all differ only in the maximum length of the values they can hold.

TEXT is a case-insensitive BLOB. TEXT values are non-binary strings (character string). They have a character set, and values are stored and compared based on the collation of the character set. The four TEXT types

- TINYTEXT
- TEXT
- MEDIUMTEXT and
- LONGTEXT

They all correspond to the four BLOB types and have the same maximum lengths and storage requirements.

The only difference between BLOB and TEXT types is that sorting and comparison is performed in case-**sensitive** for BLOB values and case-**insensitive** for TEXT values.

### Q: What is the difference between UNIX timestamps and MySQL timestamps?

Actually, both Unix timestamp and MySQL timestamp are stored as 32-bit integers, but MySQL timestamp is represented in the readable format of YYYY-MM-DD HH:MM:SS format.

### Functions and Operations

### Q: What are all the Common SQL Function?

CONCAT(A, B) – Concatenates two string values to create a single string output. Often used to combine two or more fields into one single field.

FORMAT(X, D) – Formats the number X to D significant digits.

CURRDATE(), CURRTIME() – Returns the current date or time.

NOW() – Returns the current date and time as one value.

MONTH(), DAY(), YEAR(), WEEK(), WEEKDAY() – Extracts the given data from a date value.

HOUR(), MINUTE(), SECOND() – Extracts the given data from a time value.

DATEDIFF(A, B) – Determines the difference between two dates and it is commonly used to calculate age

SUBTIMES(A, B) – Determines the difference between two times.

FROMDAYS(INT) – Converts an integer number of days into a date value.

### Q: What is REGEXP? 

REGEXP is a pattern match in which  matches pattern anywhere in the search value.

### Q: What is the different between NOW() and CURRENT_DATE()?

NOW () command is used to show current year,month,date with hours,minutes and seconds.

CURRENT_DATE() shows current year,month and date only.

### Stored Programs

### Q: What is a trigger in MySQL?

A trigger is a set of codes that executes in response to some events.

### Q: How many TRIGGERS are allowed in MySql table? 

SIX triggers are allowed in MySql table. They are as follows:

- BEFORE INSERT
- AFTER INSERT
- BEFORE UPDATE
- AFTER UPDATE
- BEFORE DELETE and
- AFTER DELETE

### Q: How to create a Stored Procedure in MySQL?

A stored procedure is a group of SQL statements that we save in the database. The SQL queries, including INSERT, UPDATE, DELETE, etc. can be a part of the stored procedure. A procedure allows us to use the same code over and over again by executing a single statement. It stores in the database data dictionary.

We can create a stored procedure using the below syntax:

```sql
CREATE PROCEDURE procedure_name [ (parameter datatype [, parameter datatype]) ]
BEGIN
    Body_section of SQL statements
END;
```

This statement can return one or more value through parameters or may not return any result. The following example explains it more clearly:

```sql
DELIMITER $$
CREATE PROCEDURE get_student_info()
BEGIN
SELECT * FROM Student_table;
END$$
```

### Q: How to execute a stored procedure in MySQL?

We can execute a stored procedure in MySQL by simply CALL query. This query takes the name of the stored procedure and any parameters we need to pass to it. The following is the basic syntax to execute a stored procedure:

```sql
CALL stored_procedure_name (argument_list);
```

For example: 

```sql
CALL Product_Pricing (@pricelow, @pricehigh);
```

### Q: How to create a View in MySQL?

A view is a database object whose values are based on the base table. It is a **virtual table** created by a query by joining one or more tables. It is operated similarly to the base table but does not contain any data of its own. If any changes occur in the underlying table, the same changes reflected in the View also.

Following is the general syntax of creating a VIEW in MySQL:

```sql
CREATE [OR REPLACE] VIEW view_name AS
SELECT columns
FROM tables
[WHERE conditions];
```



### Q: How to create a Trigger in MySQL?

A trigger is a procedural code in a database that automatically invokes whenever certain events on a particular table or view in the database occur. It can be executed when records are inserted into a table, or any columns are being updated. We can create a trigger in MySQL using the syntax as follows:

```sql
CREATE TRIGGER trigger_name
    [before | after]
   {insert | update | delete}
    ON table_name [FOR EACH ROW]
    BEGIN
        --variable declarations
        --trigger code
    END;
```



### Query Optimization

### Storage Engines

### Q: What storage engines are used in MySQL? 

Storage engines are called table types and data is stored in files using various techniques.

Technique involves:

- Storage mechanism
- Locking levels
- Indexing
- Capabilities and functions.

### Q: What is InnoDB Storage Engine?

lnnoDB is a transaction safe storage engine developed by Innobase Oy which is a Oracle Corporation now.

### Q: What is MyISAM Storage Engine?

ISAM is abbreviated as Indexed Sequential Access Method. It was developed by IBM to store and retrieve data on secondary storage systems like tapes.

### Q: What is MEMORY Storage Engine?

The **MEMORY storage engine** (formerly known as HEAP ) creates special-purpose tables with contents that are **stored** in **memory**. Because the **data** is vulnerable to crashes, hardware issues, or power outages, only use these tables as temporary work areas or read-only caches for **data** pulled from other tables.

### Q: What are Heap tables?

HEAP tables are present in memory and they are used for high speed storage on temporary

basis.

- BLOB or TEXT fields are not allowed
- Only comparison operators can be used =, <,>, = >,=<
- AUTO_INCREMENT is not supported by HEAP tables
- Indexes should be NOT NULL

### Q: What is the difference between the heap table and the temporary table?

**Heap tables:**

Heap tables are found in memory that is used for high-speed storage temporarily. They do not allow BLOB or TEXT fields.

Heap tables do not support AUTO_INCREMENT.

Indexes should be NOT NULL.

**Temporary tables:**

The temporary tables are used to keep the transient data. Sometimes it is beneficial in cases to hold temporary data. The temporary table is deleted after the current client session terminates.

**Main differences:**

The heap tables are shared among clients, while temporary tables are not shared.

Heap tables are just another storage engine, while for temporary tables, you need a special privilege (create temporary table).

### Q: How do you control the max size of a HEAP table?

Maximum size of Heal table can be controlled by MySQL config variable called max_heap_table_size.

### InnoDB Cluster

### Partitioning

## MySQL Programming Interfaces

### Q: What are the drivers in MySQL?

Following are the drivers available in MySQL:

- PHP Driver
- JDBC Driver
- ODBC Driver
- C WRAPPER
- PYTHON Driver
- PERL Driver
- RUBY Driver
- CAP11PHP Driver
- Ado.net5.mxj

## MySQL Administration

### General MySQL Administration

### The MySQL Data Directory

### Access Control and Security

### Q: Explain Access Control Lists?

An ACL (Access Control List) is a list of permissions that is associated with an object. This list is the basis for MySQL server’s security model and it helps in troubleshooting problems like users not being able to connect.

MySQL keeps the ACLs (also called grant tables) cached in memory. When a user tries to authenticate or run a command, MySQL checks the authentication information and permissions against the ACLs, in a predetermined order.

### Database Maintenance, Backup/Recovery, and Republication



## References

- [Top 50 MySQL Interview Questions & Answers](https://career.guru99.com/top-50-mysql-interview-questions-answers/)
- [MySQL Interview Questions - Javatpoint](https://www.javatpoint.com/mysql-interview-questions)