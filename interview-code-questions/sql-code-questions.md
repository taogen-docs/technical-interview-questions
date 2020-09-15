# SQL Interview Code Questions

### Content

- SQL Query
  - [x] [Q: Write an SQL query to fetch duplicate records from a EmployeeDetails?](#Q: Write an SQL query to fetch duplicate records from a EmployeeDetails?)
  - [x] [Q: Write an SQL query to remove duplicates from a table without using a temporary table?](#Q: Write an SQL query to remove duplicates from a table without using a temporary table?)
  - [x] [Q: Write an SQL query to fetch only odd rows from the table?](#Q: Write an SQL query to fetch only odd rows from the table?)
  - [x] [Q: Write an SQL query to fetch only even rows from the table?](#Q: Write an SQL query to fetch only even rows from the table?)
  - [x] [Q: Write an SQL query to create a new table with data and structure copied from another table?](#Q: Write an SQL query to create a new table with data and structure copied from another table?)
  - [x] [Q: Write an SQL query to create an empty table with the same structure as some other table?](#Q: Write an SQL query to create an empty table with the same structure as some other table?)
  - [x] [Q: Write an SQL query to fetch top n records?](#Q: Write an SQL query to fetch top n records?)
  - [x] [Q: Write an SQL query to find the Second highest salary from table?](#Q: Write an SQL query to find the Second highest salary from table?)
  - [x] [Q: Write an SQL query to find the nth highest salary from table?](#Q: Write an SQL query to find the nth highest salary from table?)
  - [x] [Q: Write SQL query to find the 3rd highest salary from a table without using TOP/limit keyword?](#Q: Write SQL query to find the 3rd highest salary from a table without using TOP/limit keyword?)

## SQL Query

### Q: Write an SQL query to fetch duplicate records from a EmployeeDetails?

```sql
SELECT FullName, ManagerId, DateOfJoining, City, COUNT(*)
FROM EmployeeDetails
GROUP BY FullName, ManagerId, DateOfJoining, City
HAVING COUNT(*) > 1;
```

### Q: Write an SQL query to remove duplicates from a table without using a temporary table?

```sql
DELETE E1 FROM EmployeeDetails E1
INNER JOIN EmployeeDetails E2 
WHERE E1.EmpId > E2.EmpId 
AND E1.FullName = E2.FullName 
AND E1.ManagerId = E2.ManagerId
AND E1.DateOfJoining = E2.DateOfJoining
AND E1.City = E2.City;
```

### Q: Write an SQL query to fetch only odd rows from the table?

In case we have an auto-increment field e.g. EmpId then we can simply use the below query:

```sql
SELECT * FROM EmployeeDetails 
WHERE MOD (EmpId, 2) <> 0;
```

In case we don’t have such a field then we can use the below queries.

Using Row_number in SQL server and checking that the remainder when divided by 2 is 1

```sql
SELECT E.EmpId, E.Project, E.Salary
FROM (
    SELECT *, Row_Number() OVER(ORDER BY EmpId) AS RowNumber
    FROM EmployeeSalary
) E
WHERE E.RowNumber % 2 = 1;
```

Using a user defined variable in MySQL

```sql
SELECT *
FROM (
      SELECT *, @rowNumber := @rowNumber+ 1 rn
      FROM EmployeeSalary
      JOIN (SELECT @rowNumber:= 0) r
     ) t 
WHERE rn % 2 = 1;
```



### Q: Write an SQL query to fetch only even rows from the table?

```sql
SELECT * FROM EmployeeDetails 
WHERE MOD (EmpId, 2) = 0;
```



### Q: Write an SQL query to create a new table with `data and structure` copied from another table?

```sql
CREATE TABLE NewTable 
SELECT * FROM EmployeeSalary;
```



### Q: Write an SQL query to create an empty table with the same `structure` as some other table?

```sql
CREATE TABLE NewTable 
SELECT * FROM EmployeeSalary where 1=0;
```



### Q: Write an SQL query to fetch top n records?

In MySql, top 50 rows are displayed by using this following query:

```sql
SELECT * FROM <table_name> LIMIT 0,50;
```

```sql
SELECT * FROM <table_name> LIMIT 50;
```

```sql
SELECT TOP 50 *
FROM <tablename>;
```



### Q: Write an SQL query to find the Second highest salary from table?

There are some other ways to find the second highest salary with MAX().

This statement uses subquery and IN clause to get the second highest salary:

```sql
SELECT MAX(salary)
FROM employees
WHERE salary NOT IN ( SELECT Max(salary) FROM employees);
```

This query uses subquery and < operator to return the second highest salary: (**Recommend**)

```sql
SELECT MAX(salary) From employees
WHERE salary < ( SELECT Max(salary) FROM employees);
```



### Q: Write an SQL query to find the nth highest salary from table?

Find nth highest salary from a table in a MySQL query

```sql
select distinct salary from employee order by salary DESC limit N-1,1
```

```sql
SELECT salary
FROM (SELECT distinct salary FROM employees ORDER BY salary DESC LIMIT N) AS Emp ORDER BY salary ASC LIMIT 1;
```



### Q: Write SQL query to find the 3rd highest salary from a table without using TOP/limit keyword?

This is one of the most commonly asked interview questions. For this, we will use a correlated subquery. 

In order to find the 3rd highest salary, we will find the salary value until the inner query returns a count of 2 rows having the salary greater than other distinct salaries.

```sql
SELECT Salary
FROM EmployeeSalary Emp1
WHERE 2 = (
                SELECT COUNT( DISTINCT ( Emp2.Salary ) )
                FROM EmployeeSalary Emp2
                WHERE Emp2.Salary > Emp1.Salary
            )
```

For nth highest salary: 

```sql
SELECT Salary
FROM EmployeeSalary Emp1
WHERE N-1 = (
                SELECT COUNT( DISTINCT ( Emp2.Salary ) )
                FROM EmployeeSalary Emp2
                WHERE Emp2.Salary > Emp1.Salary
            )
```



## References

[SQL Query Interview Questions and Answers - for Experienced](https://artoftesting.com/sql-queries-for-interview)

