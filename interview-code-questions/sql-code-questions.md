# SQL Interview Code Questions

### Content

- Q: How to display top 50 rows?
- Q: How to find the second highest salary in MySQL?



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

**Find nth highest salary from a table in a MySQL query**

```sql
select distinct(salary) from employee order by salary desc limit n-1,1
```



## References



