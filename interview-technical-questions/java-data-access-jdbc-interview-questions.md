# JDBC Interview questions

### Content

- [Introduction to JDBC](#Introduction to JDBC)
  - [x] [Q: What is JDBC?](#Q: What is JDBC?)
  - [x] [Q: What is JDBC Driver?](#Q: What is JDBC Driver?)
  - [x] [Q: What are the steps to connect to the database in java?](#Q: What are the steps to connect to the database in java?)
  - [x] [Q: What are the JDBC API components?](#Q: What are the JDBC API components?)
  - [x] [Q: What is the role of the JDBC DriverManager class?](#Q: What is the role of the JDBC DriverManager class?)
- [JDBC API](#JDBC API)
  - [Connection and DataSource](#Connection and DataSource)
    - [x] [Q: What are the functions of the JDBC Connection interface?](#Q: What are the functions of the JDBC Connection interface?)
  - [Statement](#Statement)
    - [x] [Q: What are the JDBC statements?](#Q: What are the JDBC statements?)
    - [x] [Q: What are the differences between Statement and PreparedStatement interface?](#Q: What are the differences between Statement and PreparedStatement interface?)
    - [x] [Q: How can we set null value in JDBC PreparedStatement?](#Q: How can we set null value in JDBC PreparedStatement?)
    - [x] [Q: What are the benefits of PreparedStatement over Statement?](#Q: What are the benefits of PreparedStatement over Statement?)
    - [x] [Q: What are the differences between execute, executeQuery, and executeUpdate?](#Q: What are the differences between execute, executeQuery, and executeUpdate?)
    - [x] [Q: What is batch processing and how to perform batch processing in JDBC?](#Q: What is batch processing and how to perform batch processing in JDBC?)
  - [ResultSet and RowSet](#ResultSet and RowSet)
    - [x] [Q: What are the different types of ResultSet?](#Q: What are the different types of ResultSet?)
    - [x] [Q: What are the differences between ResultSet and RowSet?](#Q: What are the differences between ResultSet and RowSet?)
    - [x] [Q: What does the JDBC ResultSet interface?](#Q: What does the JDBC ResultSet interface?)
    - [x] [Q: What is the JDBC RowSet?](#Q: What is the JDBC RowSet?)
    - [x] [Q: What does JDBC RowSet's setMaxRows method do?](#Q: What does JDBC RowSet's setMaxRows method do?)
  - [Transactions](#Transactions)
    - [x] [Q: What is Transaction?](#Q: What is Transaction?)
    - [x] [Q: Which interface is responsible for transaction management in JDBC?](#Q: Which interface is responsible for transaction management in JDBC?)
    - [x] [Q: How can we maintain the integrity of a database by using JDBC?](#Q: How can we maintain the integrity of a database by using JDBC?)
  - [Advanced Data Types](#Advanced Data Types)
    - [x] [Q: What are CLOB and BLOB data types in JDBC?](#Q: What are CLOB and BLOB data types in JDBC?)
    - [x] [Q: What is the major difference between java.util.Date and java.sql.Date data type?](#Q: What is the major difference between java.util.Date and java.sql.Date data type?)
    - [x] [Q: How can we store and retrieve images from the database?](#Q: How can we store and retrieve images from the database?)
    - [x] [Q: How can we store and retrieve the text file in the Oracle database?](#Q: How can we store and retrieve the text file in the Oracle database?)
  - [Stored Procedures](#Stored Procedures)
    - [x] [Q: How can we execute stored procedures using CallableStatement?](#Q: How can we execute stored procedures using CallableStatement?)
    - [x] [Q: What are the differences between stored procedure and functions?](#Q: What are the differences between stored procedure and functions?)
- [Advanced Topics](#Advanced Topics)
  - [x] [Q: What are the different types of lockings in JDBC?](#Q: What are the different types of lockings in JDBC?)
- [JDBC Connection Pools](#JDBC Connection Pools)
- [References](#References)

## Introduction to JDBC

### Q: What is JDBC?

JDBC is a Java API that is used to connect and execute the query to the database. JDBC API uses JDBC drivers to connect to the database. JDBC API can be used to access tabular data stored into any relational database.

### Q: What is JDBC Driver?

JDBC Driver is a software component that enables Java application to interact with the database. There are 4 types of JDBC drivers:

1. **JDBC-ODBC bridge driver:** The JDBC-ODBC bridge driver uses the ODBC driver to connect to the database. The JDBC-ODBC bridge driver converts JDBC method calls into the ODBC function calls. This is now discouraged because of the thin driver. It is easy to use and can be easily connected to any database.
2. **Native-API driver (partially java driver):** The Native API driver uses the client-side libraries of the database. The driver converts JDBC method calls into native calls of the database API. It is not written entirely in Java. Its performance is better than JDBC-ODBC bridge driver. However, the native driver must be installed on each client machine.
3. **Network Protocol driver (fully java driver):** The Network Protocol driver uses middleware (application server) that converts JDBC calls directly or indirectly into the vendor-specific database protocol. It is entirely written in Java. There is no requirement of the client-side library because of the application server that can perform many tasks like auditing, load balancing, logging, etc.
4. **Thin driver (fully java driver):** The thin driver converts JDBC calls directly into the vendor-specific database protocol. That is why it is known as the thin driver. It is entirely written in Java language. Its performance is better than all other drivers however these drivers depend upon the database.

### Q: What are the steps to connect to the database in java?

- Registering the driver class
- Creating connection
- Creating the statement
- Executing the queries
- Closing connection

```java
try (
        Connection connection = DriverManager.getConnection(url, user, password);
        Statement statement = connection.createStatement()
) {
    logger.debug("connection is {}", connection);
    statement.execute("drop table if exists user");
    statement.execute("create table if not exists user(id int not null primary key auto_increment, name varchar(64) not null, age int null)");
    int insertCount = statement.executeUpdate("insert into user (name, age) values ('Tom', 18), ('John', 21)");
    logger.debug("insert {} row(s)", insertCount);
    try (
            ResultSet resultSet = statement.executeQuery("select * from user");
    ) {
        while (resultSet.next()) {
            logger.debug("name is {}, age is {}", resultSet.getString(2), resultSet.getString(3));
        }
    }
    return true;
} catch (Exception e) {
    LoggerUtil.loggerError(logger, e);
}
```

When you are done with using your `Connection`, you need to explicitly close it by calling its `close()` method in order to release any other database resources (cursors, handles, etc) the connection may be holding on to.

Actually, the safe pattern in Java is to close your `ResultSet`, `Statement`, and `Connection` (in that order) in a `finally` block when you are done with them.

### Q: What are the JDBC API components?

The java.sql package contains following interfaces and classes for JDBC API.

**Interfaces:**

- **Connection:** The Connection object is created by using getConnection() method of DriverManager class. DriverManager is the factory for connection.
- **Statement:** The Statement object is created by using createStatement() method of Connection class. The Connection interface is the factory for Statement.
- **PreparedStatement:** The PrepareStatement object is created by using prepareStatement() method of Connection class. It is used to execute the parameterized query.
- **ResultSet:** The object of ResultSet maintains a cursor pointing to a row of a table. Initially, cursor points before the first row. The executeQuery() method of Statement interface returns the ResultSet object.
- **ResultSetMetaData:** The object of ResultSetMetaData interface cotains the information about the data (table) such as numer of columns, column name, column type, etc. The getMetaData() method of ResultSet returns the object of ResultSetMetaData.
- **DatabaseMetaData:** DatabaseMetaData interface provides methods to get metadata of a database such as the database product name, database product version, driver name, name of the total number of tables, the name of the total number of views, etc. The getMetaData() method of Connection interface returns the object of DatabaseMetaData.
- **CallableStatement:** CallableStatement interface is used to call the stored procedures and functions. We can have business logic on the database through the use of stored procedures and functions that will make the performance better because these are precompiled. The prepareCall() method of Connection interface returns the instance of CallableStatement.

**Classes:**

- **DriverManager:** The DriverManager class acts as an interface between the user and drivers. It keeps track of the drivers that are available and handles establishing a connection between a database and the appropriate driver. It contains several methods to keep the interaction between the user and drivers.
- **Blob:** Blob stands for the binary large object. It represents a collection of binary data stored as a single entity in the database management system.
- **Clob:** Clob stands for Character large object. It is a data type that is used by various database management systems to store character files. It is similar to Blob except for the difference that BLOB represent binary data such as images, audio and video files, etc. whereas Clob represents character stream data such as character files, etc.
- **SQLException** It is an Exception class which provides information on database access errors.

### Q: What is the role of the JDBC DriverManager class?

The DriverManager class acts as an interface between user and drivers. It keeps track of the drivers that are available and handles establishing a connection between a database and the appropriate driver. The DriverManager class maintains a list of Driver classes that have registered themselves by calling the method DriverManager.registerDriver().

## JDBC API

### Connection and DataSource

### Q: What are the functions of the JDBC Connection interface?

The **Connection interface** maintains a session with the database. It can be used for transaction management. It provides factory methods that return the instance of Statement, PreparedStatement, CallableStatement, and DatabaseMetaData.

### Statement

### Q: What are the JDBC statements?

In JDBC, Statements are used to send SQL commands to the database and receive data from the database. There are various methods provided by JDBC statements such as execute(), executeUpdate(), executeQuery, etc. which helps you to interact with the database.

There is three type of JDBC statements given in the following table.

| Statements        | Explanation                                                  |
| :---------------- | :----------------------------------------------------------- |
| Statement         | Statement is the factory for resultset. It is used for general purpose access to the database. It executes a static SQL query at runtime. |
| PreparedStatement | The PreparedStatement is used when we need to provide input parameters to the query at runtime. |
| CallableStatement | CallableStatement is used when we need to access the database stored procedures. It can also accept runtime parameters. |

### Q: What are the differences between Statement and PreparedStatement interface?

| Statement                                                    | PreparedStatement                                            |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| The Statement interface provides methods to execute queries with the database. The statement interface is a factory of ResultSet; i.e., it provides the factory method to get the object of ResultSet. | The PreparedStatement interface is a subinterface of Statement. It is used to execute the parameterized query. |
| In the case of Statement, the query is compiled each time we run the program. | In the case of PreparedStatement, the query is compiled only once. |
| The Statement is mainly used in the case when we need to run the static query at runtime. | PreparedStatement is used when we need to provide input parameters to the query at runtime. |

### Q: How can we set null value in JDBC PreparedStatement?

By using setNull() method of PreparedStatement interface, we can set the null value to an index. The syntax of the method is given below.

```java
void setNull(int parameterIndex, int sqlType) throws SQLException
```

### Q: What are the benefits of PreparedStatement over Statement?

The benefits of using PreparedStatement over Statement interface is given below.

- The PreparedStatement performs faster as compare to Statement because the Statement needs to be compiled everytime we run the code whereas the PreparedStatement compiled once and then execute only on runtime.
- PreparedStatement can execute Parameterized query that can prevent SQL injection whereas Statement can only run static queries.
- The query used in PreparedStatement is appeared to be similar every time. Therefore, the database can reuse the previous access plan whereas, Statement inline the parameters into the String, therefore, the query doesn't appear to be same everytime which prevents cache reusage.

### Q: What are the differences between execute, executeQuery, and executeUpdate?

| execute                                                      | executeQuery                                                 | executeUpdate                                                |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| The execute method can be used for any SQL statements(Select and Update both). | The executeQuery method can be used only with the select statement. | The executeUpdate method can be used to update/delete/insert operations in the database. |
| The execute method returns a boolean type value where true indicates that the ResultSet s returned which can later be extracted and false indicates that the integer or void value is returned. | The executeQuery() method returns a ResultSet object which contains the data retrieved by the select statement. | The executeUpdate() method returns an integer value representing the number of records affected where 0 indicates that query returns nothing. |

### Q: What is batch processing and how to perform batch processing in JDBC?

By using the batch processing technique in JDBC, we can execute multiple queries. It makes the performance fast. The java.sql.Statement and java.sql.PreparedStatement interfaces provide methods for batch processing. The batch processing in JDBC requires the following steps.

- Load the driver class
- Create Connection
- Create Statement
- Add query in the batch
- Execute the Batch
- Close Connection

Consider the following example to perform batch processing using the Statement interface.

```java
Class.forName("oracle.jdbc.driver.OracleDriver");
Connection con=DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe","system","oracle");
con.setAutoCommit(false);

Statement stmt=con.createStatement();
stmt.addBatch("insert into user420 values(190,'abhi',40000)");
stmt.addBatch("insert into user420 values(191,'umesh',50000)");

stmt.executeBatch();//executing the batch

con.commit();
con.close();
```



### ResultSet and RowSet

### Q: What are the different types of ResultSet?

ResultSet is categorized by the direction of the reading head and sensitivity or insensitivity of the result provided by it. There are three general types of ResultSet.

| Type                              | Description                                                  |
| --------------------------------- | ------------------------------------------------------------ |
| ResultSet.TYPE_Forward_ONLY       | The cursor can move in the forward direction only.           |
| ResultSet.TYPE_SCROLL_INSENSITIVE | The cursor can move in both the direction (forward and backward). The ResultSet is not sensitive to the changes made by the others to the database. |
| ResultSet.TYPE_SCROLL_SENSITIVE   | The cursor can move in both the direction. The ResultSet is sensitive to the changes made by the others to the database. |

### Q: What are the differences between ResultSet and RowSet?

| ResultSet                                                    | RowSet                                                       |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ResultSet cannot be serialized as it maintains the connection with the database. | RowSet is disconnected from the database and can be serialized. |
| ResultSet object is not a JavaBean object                    | ResultSet Object is a JavaBean object.                       |
| ResultSet is returned by the executeQuery() method of Statement Interface. | Rowset Interface extends ResultSet Interface and returned by calling the RowSetProvider.newFactory().createJdbcRowSet() method. |
| ResultSet object is non-scrollable and non-updatable by default. | RowSet object is scrollable and updatable by default.        |

### Q: What does the JDBC ResultSet interface?

The ResultSet object represents a row of a table. It can be used to change the cursor pointer and get the information from the database. By default, ResultSet object can move in the forward direction only and is not updatable. However, we can make this object to move the forward and backward direction by passing either TYPE_SCROLL_INSENSITIVE or TYPE_SCROLL_SENSITIVE in createStatement(int, int) method.

### Q: What is the JDBC RowSet?

JDBC Rowset is the wrapper of ResultSet. It holds tabular data like ResultSet, but it is easy and flexible to use. The implementation classes of RowSet interface are as follows:

- JdbcRowSet
- CachedRowSet
- WebRowSet
- JoinRowSet
- FilteredRowSet

### Q: What does JDBC RowSet's setMaxRows method do?

The setMaxRows(int i) method limits the number of rows the database can return by using the query. This can also be done within the query as we can use the limit cause in MySQL.

### Transactions

### Q: What is Transaction?

Transaction represents **a single unit of work**.

The ACID properties describes the transaction management well. ACID stands for Atomicity, Consistency, isolation and durability.

**Atomicity** means either all successful or none.

**Consistency** ensures bringing the database from one consistent state to another consistent state.

**Isolation** ensures that transaction is isolated from other transaction.

**Durability** means once a transaction has been committed, it will remain so, even in the event of errors, power loss etc.

### Q: Which interface is responsible for transaction management in JDBC?

In JDBC, **Connection interface** provides methods to manage transaction.

| Method                             | Description                                                  |
| :--------------------------------- | :----------------------------------------------------------- |
| void setAutoCommit(boolean status) | It is true bydefault means each transaction is committed bydefault. |
| void commit()                      | commits the transaction.                                     |
| void rollback()                    | cancels the transaction.                                     |

### Q: How can we maintain the integrity of a database by using JDBC?

To maintain the integrity of a database, we need to ensure the ACID properties. ACID properties mean Atomicity, Consistency, Isolation, and durability. In JDBC, Connection interface provides methods like setAutoCommit(), commit(), and rollback() which can be used to manage transaction. Let's see an example of transaction management in JDBC.

```java
Class.forName("oracle.jdbc.driver.OracleDriver");
Connection con=DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe","system","oracle");
con.setAutoCommit(false);
  
Statement stmt=con.createStatement();
stmt.executeUpdate("insert into user420 values(190,'abhi',40000)");
stmt.executeUpdate("insert into user420 values(191,'umesh',50000)");
  
con.commit();
con.close();
```



### RowSet

### Advanced Data Types

### Q: What are CLOB and BLOB data types in JDBC?

**BLOB:** Blob can be defined as the variable-length, binary large object which is used to hold the group of Binary data such as voice, images, and mixed media. It can hold up to 2GB data on MySQL database and 128 GB on Oracle database. BLOB is supported by many databases such as MySQL, Oracle, and DB2 to store the binary data (images, video, audio, and mixed media).

**CLOB:** Clob can be defined as the variable-length, character-large object which is used to hold the character-based data such as files in many databases. It can hold up to 2 GB on MySQL database, and 128 GB on Oracle Database. A CLOB is considered as a character string.

### Q: What is the major difference between java.util.Date and java.sql.Date data type?

The major difference between java.util.Date and java.sql.Date is that, java.sql.Date represents date without time information whereas, java.util.Date represents both date and time information.

### Q: How can we store and retrieve images from the database?

By using the PreparedStatement interface, we can store and retrieve images.

Create a table which contains two columns namely NAME and PHOTO.

```sql
CREATE TABLE  "IMGTABLE" 
   (    "NAME" VARCHAR2(4000),
    "PHOTO" BLOB
   )
```

The following example to store the image in the database.

```java
Class.forName("oracle.jdbc.driver.OracleDriver");
Connection con=DriverManager.getConnection(  
"jdbc:oracle:thin:@localhost:1521:xe","system","oracle");
              
PreparedStatement ps=con.prepareStatement("insert into imgtable values(?,?)");
ps.setString(1,"sonoo");
  
FileInputStream fin=new FileInputStream("d:\\g.jpg");
ps.setBinaryStream(2,fin,fin.available());
int i=ps.executeUpdate();
System.out.println(i+" records affected");
          
con.close();
```

The following example to retrieve the image from the table.

```java
Class.forName("oracle.jdbc.driver.OracleDriver");  
Connection con=DriverManager.getConnection(  
"jdbc:oracle:thin:@localhost:1521:xe","system","oracle");
      
PreparedStatement ps=con.prepareStatement("select * from imgtable");
ResultSet rs=ps.executeQuery();
if(rs.next()){//now on 1st row
              
Blob b=rs.getBlob(2);//2 means 2nd column data
byte barr[]=b.getBytes(1,(int)b.length());//1 means first image

FileOutputStream fout=new FileOutputStream("d:\\sonoo.jpg");
fout.write(barr);
              
fout.close();
```



### Q: How can we store and retrieve the text file in the Oracle database?

The setCharacterStream() method of PreparedStatement interface is used to set character information into the parameterIndex. For storing the file into the database, CLOB (Character Large Object) datatype is used in the table. For example:

```sql
CREATE TABLE  "FILETABLE" 
   (    "ID" NUMBER,
    "NAME" CLOB
   )
```

Store to database

```java
Class.forName("oracle.jdbc.driver.OracleDriver");
Connection con=DriverManager.getConnection(  
"jdbc:oracle:thin:@localhost:1521:xe","system","oracle");
              
PreparedStatement ps=con.prepareStatement(  
"insert into filetable values(?,?)");
              
File f=new File("d:\\myfile.txt");
FileReader fr=new FileReader(f);
              
ps.setInt(1,101);
ps.setCharacterStream(2,fr,(int)f.length());
int i=ps.executeUpdate();
System.out.println(i+" records affected");
              
con.close();  
```

Retrieve from database

```java
Class.forName("oracle.jdbc.driver.OracleDriver");
Connection con=DriverManager.getConnection(  
"jdbc:oracle:thin:@localhost:1521:xe","system","oracle");
              
PreparedStatement ps=con.prepareStatement("select * from filetable");
ResultSet rs=ps.executeQuery();
rs.next();//now on 1st row
              
Clob c=rs.getClob(2);
Reader r=c.getCharacterStream();
              
FileWriter fw=new FileWriter("d:\\retrivefile.txt");
              
int i;
while((i=r.read())!=-1)
fw.write((char)i);
              
fw.close();
con.close();
```



### Stored Procedures

### Q: How can we execute stored procedures using CallableStatement?

Define stored procedure

```sql
create or replace procedure "INSERTR"  
(id IN NUMBER,  
name IN VARCHAR2)  
is  
begin  
insert into user420 values(id,name);  
end;
```

Call stored procedure

```java
CallableStatement stmt=con.prepareCall("{call insertR(?,?)}");
stmt.setInt(1,1011);
stmt.setString(2,"Amit");
stmt.execute();
```



### Q: What are the differences between stored procedure and functions?

The differences between stored procedures and functions are given below:

| Stored Procedure                                             | Function                                                     |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| Is used to perform business logic.                           | Is used to perform the calculation.                          |
| Must not have the return type.                               | Must have the return type.                                   |
| May return 0 or more values.                                 | May return only one value.                                   |
| The procedure supports input and output parameters.          | The function supports only input parameter.                  |
| Exception handling using try/catch block can be used in stored procedures. | Exception handling using try/catch can't be used in user-defined functions. |

## Advanced Topics

### Q: What are the different types of lockings in JDBC?

A lock is a certain type of software mechanism by using which, we can restrict other users from using the data resource. There are four type of locks given in JDBC that are described below.

- **Row and Key Locks:** These type of locks are used when we update the rows.
- **Page Locks:** These type of locks are applied to a page. They are used in the case, where a transaction remains in the process and is being updated, deleting, or inserting some data in a row of the table. The database server locks the entire page that contains the row. The page lock can be applied once by the database server.
- **Table locks:** Table locks are applied to the table. It can be applied in two ways, i.e., shared and exclusive. Shared lock lets the other transactions to read the table but not update it. However, The exclusive lock prevents others from reading and writing the table.
- **Database locks:** The Database lock is used to prevent the read and update access from other transactions when the database is open.





## JDBC Connection Pools

## References

- [JDBC Interview Questions - javatpoint](https://www.javatpoint.com/jdbc-interview-questions)
- [Closing Database Connections in Java - StackOverflow](https://stackoverflow.com/questions/2225221/closing-database-connections-in-java)