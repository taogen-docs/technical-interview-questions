# MySQL Optimization Interview Questions

### Content

- Optimizing Schema
  - [x] [Q: General Principles for optimizing schema?](#Q: General Principles for optimizing schema?)
  - [x] [Q: How to choosing a specific data type from a kind of data type?](#Q: How to choosing a specific data type from a kind of data type?)
- Indexing
  - [x] [Q: General Principles for Choose Indexes?](#Q: General Principles for Choose Indexes?)
  - [x] [Q: General Process for Choosing Indexes?](#Q: General Process for Choosing Indexes?)
  - [x] [Q: Difference between Index Types in MySQL?](#Q: Difference between Index Types in MySQL?)
- Optimizing Query
  - [x] [Q: How to Optimizing Query?](#Q: How to Optimizing Query?)

## Optimizing Schema

### Q: General Principles for optimizing schema?

The **general principles** for choosing a data type are introduced earlier in this article. They are “smaller is usually better”, “simple is good”, and “avoid NULL if possible”.

- Sometimes, the data type of a column doesn’t limit one kind of data type, so we can use the principle “simple is good” to determine what kind of data type we use.
- When we determine what kind of data type for the column, we can follow the principle of “smaller is usually better” to choose a specific data type. Then, we also can follow the principle “avoid NULL if possible” to determine does the column allows NULL.

### Q: How to choosing a specific data type from a kind of data type?

The kinds of data types are whole numbers, real numbers, strings (text), binary, temporal (time), and others. For **choosing a specific data type** from a kind of data type, you can use the following methods.

- For choosing **a data type of whole numbers**. 
  1. First, you should choose the **less** length of integer type if possible.
  2. If you don’t there are no negative numbers, you should set it to be **unsigned** (that makes values range larger).
  3. For storing **bool data**, the better choice is BOOL(TINYINT) data type, others choices are BIT(1), CHAR(0).
  4. There are many common usage scenarios of whole numbers. For example, table’s identifiers, counter numbers. For **identifiers** of tables, integers are the best choice for identifiers, and all tables’ identifiers should be the same integer type.
- For choosing **a data type of real numbers**. 
  1. If you need **exact calculations** you should choose the DECIMAL type.
  2. If you can accept **approximate calculations** you can choose the FLOAT and DOUBLE data type by different precisions.
  3. Note that you should use DECIMAL only when you need exact results for fractional numbers because it needs more cost than floating numbers.
  4. There are many common usage scenarios of real numbers, for example, financial data. For **financial data**, the DECIMAL type is a better choice for representing financial data, but if the financial data have small limit precision you can convert all data to integer values and use BIGINTEGER to store them.
- For choosing **a data type of temporal types**. 
  1. Sometimes you can use integers to replace temporal types because integer types are simpler and faster than temporal types, but you will lose lots of very convenient built-in functions with temporal types, such as `WEEK()`, `ADDDATE()`. 
  2. In the choice of temporal types, the most common question is how to choose a data type that contains both date and time types from DATETIME and TIMESTAMP. The main differences between DATETIME and TIMESTAMP are representing range, space cost, and affect by time zone.
- For choosing a specific **string type**. 
  - 1. The most choice are VARCHAR and CHAR. When your column values limit by small length, you can use CHAR to store it, otherwise use VARCHAR.
    2. When you need to store large amounts of characters, you can choose a text type from text family types according to your range of characters of text.
    3. For binary data, the basic choices are BINARY and VARBINARY that same with CHAR and VARCHAR, but store binary.
    4. When you want to store large amounts of binary, you can choose a binary type from blob family types.
    5. There are some special data types in string types, such as ENUM, SET, and JSON.
    6. There are many common usage scenarios of string types, for example, ID card No., account number, name, URI, and so on.
    7. Note that sometimes you can use integers to replace strings it has much performance improvement, such as IPv4 address can use BIGINTEGER to represent.

## Indexing

### Q: General Principles for Choose Indexes?

Indexing is a very complex topic. There are no fixed rules to guide how to indexing. It depends on many factors, such as what are your data structures, how did you use the data in your application, what results are you want, how did storage engines implement the index, properties of each type of index.

If you want to improve a slow query, you can profiling the query that lets you see which subtask costs the most time, or using the EXPLAIN command. Whatever you use what ways to analyze, but you always need to find the reasons for the cause slow to query. There are some methods that may be helpful to improve a query, such as update the table’s schema, add or extend indexes, and rewrite the query statement. Remember that indexing is part of improving a query. **Note that Indexes are good for queries, but too many indexes may slow to write operations.**

There are some basic principles to choose indexes:

- General using of index is the B-Tree index, and the other types of indexes are rather more suitable for special purposes.
- Reads data from index files are faster than reads from physical data files.
- Single-row access is slow. You better to read in a block that contains lots of rows you need.
- Accessing ranges of rows in order is fast. First, sequential I/O doesn’t require disk seek, so it is faster than random I/O. Secondly, it doesn’t need to perform any follow-up work to sort it.
- Index-only access is fast. If an index contains all the columns that the query needs, the storage engine don’t need to find the other columns by looking up rows in the table. This avoids lots of single-row access.

It’s very important to be able to reason through how indexes work, and to choose them based on that understanding, not on rules of thumb or heuristics such as “place the most selective columns first in multicolumn indexes” or “you should index all of the columns that appear in the WHERE clause”.

If you find a query that doesn’t benefit from all of these possible advantages of indexes, see if a better index can be created to improve performance. If not, perhaps a rewrite can transform the query so that it can use an index.

### Q: General Process for Choosing Indexes?

General process for choosing indexes:

1. Choosing a type of index
2. Determining what properties of the index to use.
   - prefix indexes and compressed indexes
   - multicolumn indexes (like B-Tree index, hash index) and covering indexes (like B-Tree index), also consider indexes columns order)
3. Avoid to add redundant and duplicate indexes, and remove unused indexes.

### Q: Difference between Index Types in MySQL?

Indexes contrast Table

| Index Type   | Indexed Columns | Time Complexity | Equality Query                | Range Query                                           | Order and Group Query | Covering Index |
| :----------- | :-------------- | :-------------- | :---------------------------- | :---------------------------------------------------- | :-------------------- | :------------- |
| B-Tree Index | Multiple        | O(log n)        | Yes. (Leftmost indexed value) | Yes                                                   | Yes                   | Yes            |
| Hash Index   | Multiple        | O(1)            | Yes. (Entire indexed value)   | No                                                    | No                    | No             |
| Bitmap Index | One             | O(1)            | Yes                           | No. Indexing on a column that has small range values. | No                    | No             |



## Optimizing Query

### Q: How to Optimizing Query?

For query optimization, we should understanding query execution basic such as what is a general query execution process in MySQL.

Before we to optimize a query, we must find the reason of slow to a query. We can use EXPLAIN to see how the query to execute. However a slow query may cause by many reasons which are schema of table, indexes of table, and the query statement. We need to combine these aspects to optimize.

We know query optimization that is part of optimization. In theory, MySQL will execute some queries almost identically. In reality, measuring is the only way to tell which approach is really faster. For query optimization, There are some advice on how to optimize certain kinds of queries. Most of the advice is version-dependent, and it might not hold for future versions of MySQL.



## References

- High Performance MySQL by Baron Schwartz, Vadim Tkachenko, Peter Zaitsev, Derek J. Balling