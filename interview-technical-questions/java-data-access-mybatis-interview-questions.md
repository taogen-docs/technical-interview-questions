# MyBatis Interview Questions

**Content**

- Introduction to MyBatis
  - [x] [What is MyBatis?](#What is MyBatis)
  - [x] [MyBatis' Advantages and Disadvantages?](#MyBatis' Advantages and Disadvantages)
  - [x] [MyBatis' Applicability?](#MyBatis' Applicability)
  - [x] [MyBatis vs Hibernate?](#MyBatis vs Hibernate)
- Building SqlSessionFactory from XML or Java
- Mapped SQL Statements by XML or Annotations
  - [x] [What differences between #{} and ${}?](#What differences between #{} and ${})
  - [x] [How to map columns to object's fields?](#How to map columns to object's fields?)
  - [ ] [How to Write MyBatis Paging SQL?](#How to Write MyBatis Paging SQL) (TODO)
  - [x] [How to get auto-generate primary key when insert an entity?](#How to get auto-generate primary key when insert an entity?)
  - [x] [How to Pass Multiple Parameters in a Mapper Interface?](#How to Pass Multiple Parameters in a Mapper Interface?)
  - [x] [How to Write One-to-One, One-to-Many Query?](#How to Write One-to-One, One-to-Many Query?)
  - [Mapper Implementation Ways?](#Mapper Implementation Ways)
- Dynamic SQL
  - [x] [What is Dynamic SQL?](#What is Dynamic SQL?)
- Implementations
  - [How Mapper Interface Bind XML Mapping File?](#[How Mapper Interface Bind XML Mapping File?) (**TODO**)
  - [How Maper Interface Bind SQL Annotations?](#How Maper Interface Bind SQL Annotations?) (**TODO**)
  - [How MyBatis Convert ResultSet to Entity Objects?](#How MyBatis Convert ResultSet to Entity Objects?) (**TODO**)
  - [How Dynamic SQL works?](#How Dynamic SQL works?)
- MyBatis APIs (SqlSessionFactory, SqlSession, SQL Builder, Scope and Lifecycle)
- Stored Procedure Support
- Advanced Topics
  - [How MyBatis Lazy Load works?](#How MyBatis Lazy Load works?)
  - [What is MyBatis One-Level Cache and Second-Level Cache?](#What is MyBatis One-Level Cache and Second-Level Cache?)
- Plugins
  - [What are Paging Plugins?](#What are Paging Plugins? ) 
  - [How MyBatis Plugin works?](#How MyBatis Plugin works?)
  - [How to Write a MyBatis Plugin?](#How to Write a MyBatis Plugin?)

## Introduction to MyBatis

### What is MyBatis?

MyBatis is **a persistence framework** with **support** for custom SQL, stored procedures and advanced mappings. MyBatis **eliminates** almost all of the JDBC code and manual setting of parameters and retrieval of results. MyBatis can **use** simple XML or Annotations for configuration and map primitives, Map interfaces and Java POJOs (Plain Old Java Objects) to database records.

### MyBatis' Advantages and Disadvantages?

MyBatis' advantages:

- Simplify JDBC API operations.
- Support object relational mapping(ORM).
- Base SQL statements programming, it's flexible. Support dynamic SQL.

MyBatis's disadvantages:

- The writing workload of SQL statements is large.
- SQL statements dependency database. It has low compatibility.

### MyBatis' Applicability?

- Flexible DAO solutions.
- Require high performance, or requirements are often changed.

### MyBatis vs Hibernate?

1. MyBatis is half-ORM framework, it needs write SQL. But Hibernate is full-ORM framework.
2. MyBatis needs to write SQL that has high flexibility and high performance, but SQL is bound a database, it has low compatibility. Hibernate needn't to write SQL, it doesn't dependency any database type.  

## Building SqlSessionFactory from XML or Java

## Mapped SQL Statements by XML or Annotations

### What differences between `#{}` and `${}`?

${} and #{} are both string substitution.

the `${column}` will be substituted directly and the `#{value}` will be "prepared". #{} can prevent SQL injection. For example:

```sql
select * from user where ${column} = #{value}
```

### How to map columns to object's fields?

1. Using `as` to set column aliases in select SQL statements. Let columns have alias that the same with fields name.
2. Using `<resultMap>` in `EntityMapper.xml`.

### How to get auto-generate primary key when insert an entity?

xxxMapper.xml

```xml
<insert id="saveSelective" parameterType="com.taogen.example.mybatis.sqlmap.xml.entity.Employee"
        useGeneratedKeys="true" keyProperty="id" keyColumn="id">
    sql_statement...
</insert>
```

xxxMapper.java

```java
@InsertProvider(type = DepartmentSqlProvider.class, method = "saveSelective")
@Options(useGeneratedKeys = true, keyProperty = "id", keyColumn = "id")
int saveSelective(Department entity);
```

### How to Pass Multiple Parameters in a Mapper Interface?

Use `@param` in mapper interface methods.

```java
List<Department> findPage(@Param("page") Page page, @Param("entity") Department entity);
```

### How to Write One-to-One, One-to-Many Query?

Implemented Ways for One-to-One, One-to-Many Query

- One-to-one
  - One-to-one by aliases and `resultType="entity_classname"` (Need Joins Table)
  - One-to-one by Nested Results with `<association> `of `<resultMap>` (Need Joins Table)
  - One-to-one by Nested select with `<association select="">` of `<resultMap>` (Needn't Joins Table, don't recommend)
- One-to-many
  - One-to-many by Nested Results with `<collection>` of `<resultMap>` (Need Joins Table)
  - One-to-many by Nested Results with `<collection select="">` of `<resultMap>` (Need Joins Table, Don't Recommend)

One-to-one by aliases and `resultType="entity_classname"` (Need Joins Table)

```xml
<sql id="One_To_One_Column_List">
    a.id,
    a.name,
    a.nickname,
    a.age,
    a.delete_flag as "deleteFlag",
    a.create_time as "createTime",
    a.modify_time as "modifyTime",
    b.id as "department.id",
    b.name as "department.name",
    b.delete_flag as "department.deleteFlag",
    b.create_time as "department.createTime",
    b.modify_time as "department.modifyTime"
</sql>
<sql id="Joins">
    LEFT JOIN t_department b ON a.dept_id = b.id
</sql>

<select id="getById" parameterType="java.lang.Integer" resultType="Employee">
    select
    <include refid="One_To_One_Column_List"/>
    from t_employee as a
    <include refid="Joins"/>
    where a.id = #{id,jdbcType=INTEGER}
</select>
```

One-to-one by Nested Results with `<association> `of `<resultMap>` (Need Joins Table)

```xml
<sql id="One_To_One_Column_List_2">
      a.id as emp_id,
      a.name as emp_name,
      a.nickname as emp_nickname,
      a.age as emp_age,
      a.delete_flag as emp_delete_flag,
      a.create_time as emp_create_time,
      a.modify_time as emp_modify_time,
      b.id as dept_id,
      b.name as dept_name,
      b.delete_flag as dept_delete_flag,
      b.create_time as dept_create_time,
      b.modify_time as dept_modify_time
</sql>
<sql id="Joins">
    LEFT JOIN t_department b ON a.dept_id = b.id
</sql>

<resultMap id="OneToOneResultMap_2" type="Employee">
  <id column="emp_id" jdbcType="INTEGER" property="id"/>
  <result column="emp_name" jdbcType="VARCHAR" property="name"/>
  <result column="emp_nickname" jdbcType="VARCHAR" property="nickname"/>
  <result column="emp_age" jdbcType="INTEGER" property="age"/>
  <result column="emp_delete_flag" jdbcType="BIT" property="deleteFlag"/>
  <result column="emp_create_time" jdbcType="TIMESTAMP" property="createTime"/>
  <result column="emp_modify_time" jdbcType="TIMESTAMP" property="modifyTime"/>
  <association property="department" javaType="Department">
      <id column="dept_id" jdbcType="INTEGER" property="id"/>
      <result column="dept_name" jdbcType="VARCHAR" property="name"/>
      <result column="dept_delete_flag" jdbcType="BIT" property="deleteFlag"/>
      <result column="dept_create_time" jdbcType="TIMESTAMP" property="createTime"/>
      <result column="dept_modify_time" jdbcType="TIMESTAMP" property="modifyTime"/>
  </association>
</resultMap>

<select id="getById2" parameterType="java.lang.Integer" resultMap="OneToOneResultMap_2">
  select
  <include refid="One_To_One_Column_List_2"/>
  from t_employee as a
  <include refid="Joins"/>
  where a.id = #{id,jdbcType=INTEGER}
</select>
```

One-to-one by Nested select with `<association select="">` of `<resultMap>` (Needn't Joins Table, don't recommend)

```xml
<resultMap id="OneToOneResultMap_NestedSelect" type="Employee">
    <id column="id" jdbcType="INTEGER" property="id"/>
    <result column="name" jdbcType="VARCHAR" property="name"/>
    <result column="nickname" jdbcType="VARCHAR" property="nickname"/>
    <result column="age" jdbcType="INTEGER" property="age"/>
    <result column="delete_flag" jdbcType="BIT" property="deleteFlag"/>
    <result column="create_time" jdbcType="TIMESTAMP" property="createTime"/>
    <result column="modify_time" jdbcType="TIMESTAMP" property="modifyTime"/>
    <association property="department" column="dept_id" javaType="Department" select="selectAssociationDepartment"/>
</resultMap>

<resultMap id="OneToOneResultMap_NestedSelect_Association" type="com.taogen.example.mybatis.sqlmap.xml.entity.Department">
    <id column="id" jdbcType="INTEGER" property="id"/>
    <result column="name" jdbcType="VARCHAR" property="name"/>
    <result column="delete_flag" jdbcType="BIT" property="deleteFlag"/>
    <result column="create_time" jdbcType="TIMESTAMP" property="createTime"/>
    <result column="modify_time" jdbcType="TIMESTAMP" property="modifyTime"/>
</resultMap>

<select id="getByIdWithNestedSelect" parameterType="java.lang.Integer" resultMap="OneToOneResultMap_NestedSelect">
    select *
    from t_employee
    where id = #{id,jdbcType=INTEGER}
</select>

<select id="selectAssociationDepartment" parameterType="java.lang.Integer" resultMap="OneToOneResultMap_NestedSelect_Association">
    select *
    from t_department
    where id = #{id,jdbcType=INTEGER}
</select>
```

One-to-many by Nested Results with `<collection>` of `<resultMap>` (Need Joins Table)

```xml
<resultMap id="OneToManyResultMap_NestedResults" type="Department">
    <id column="id" jdbcType="INTEGER" property="id"/>
    <result column="name" jdbcType="VARCHAR" property="name"/>
    <result column="delete_flag" jdbcType="BIT" property="deleteFlag"/>
    <result column="create_time" jdbcType="TIMESTAMP" property="createTime"/>
    <result column="modify_time" jdbcType="TIMESTAMP" property="modifyTime"/>
    <collection property="employees" ofType="Employee">
        <id column="employee.id" jdbcType="INTEGER" property="id"/>
        <result column="employee.name" jdbcType="VARCHAR" property="name"/>
        <result column="employee.nickname" jdbcType="VARCHAR" property="nickname"/>
        <result column="employee.age" jdbcType="INTEGER" property="age"/>
        <result column="employee.deleteFlag" jdbcType="BIT" property="deleteFlag"/>
        <result column="employee.createTime" jdbcType="TIMESTAMP" property="createTime"/>
        <result column="employee.modifyTime" jdbcType="TIMESTAMP" property="modifyTime"/>
    </collection>
</resultMap>

<sql id="One_To_Many_Column_List_Nested_Results">
    a.id,
    a.name,
    a.delete_flag,
    a.create_time,
    a.modify_time,
    b.id as "employee.id",
    b.name as "employee.name",
    b.nickname as "employee.nickname",
    b.age as "employee.age",
    b.delete_flag as "employee.deleteFlag",
    b.create_time as "employee.createTime",
    b.modify_time as "employee.modifyTime"
</sql>

<sql id="Joins">
    LEFT JOIN t_employee as b on a.id=b.dept_id
</sql>

<select id="getById" parameterType="Department" resultMap="OneToManyResultMap_NestedResults">
    select
    <include refid="One_To_Many_Column_List_Nested_Results"/>
    from t_department as a
    <include refid="Joins"/>
    where a.id = #{id,jdbcType=INTEGER}
</select>
```

One-to-many by Nested Results with `<collection select="">` of `<resultMap>` (Need Joins Table, Don't Recommend)

```xml
<resultMap id="OneToManyResultMap_NestedSelect" type="Department">
    <id column="id" jdbcType="INTEGER" property="id"/>
    <result column="name" jdbcType="VARCHAR" property="name"/>
    <result column="delete_flag" jdbcType="BIT" property="deleteFlag"/>
    <result column="create_time" jdbcType="TIMESTAMP" property="createTime"/>
    <result column="modify_time" jdbcType="TIMESTAMP" property="modifyTime"/>
    <collection property="employees" javaType="ArrayList" column="id"
                ofType="Employee" select="selectAssociationEmployees"/>
</resultMap>

<resultMap id="OneToManyResultMap_NestedSelect_Association" type="Employee">
    <id column="id" jdbcType="INTEGER" property="id"/>
    <result column="name" jdbcType="VARCHAR" property="name"/>
    <result column="nickname" jdbcType="VARCHAR" property="nickname"/>
    <result column="age" jdbcType="INTEGER" property="age"/>
    <result column="delete_flag" jdbcType="BIT" property="deleteFlag"/>
    <result column="create_time" jdbcType="TIMESTAMP" property="createTime"/>
    <result column="modify_time" jdbcType="TIMESTAMP" property="modifyTime"/>
</resultMap>

<select id="getByIdWithNestedSelect" parameterType="Department" resultMap="OneToManyResultMap_NestedSelect">
    select *
    from t_department
    where id = #{id,jdbcType=INTEGER}
</select>

<select id="selectAssociationEmployees" resultMap="OneToManyResultMap_NestedSelect_Association">
    select *
    from t_employee
    where dept_id = #{id}
</select>
```



### How Mapper Interface Bind XML Mapping File?

> Fully-qualified name: A class's fully-qualified name is the package name followed class name, separated by a period (.).

Configuration in `mybatis-config.xml` and entity-mapping xml

- The mapper interface class' fully-qualified name is the same with namespace property value in entity-mapping xml.
- The mapper interface class' method names are the same as `<insert id="">`, `<select id="">` and so on elements' id property values in entity-mapping xml. 
- The mapper interface class' method parameters can pass to SQL statement in entity-mapping xml.
- The entity-mapping XMLs are configure in `mybatis-config.xml`.

Programming Implementations

- ```java
  SqlSession sqlSession = sqlSessionFactory.openSession();
  MyMapper mapper = sqlSession.getMapper(MyMapper.class);
  mapper.save(T entity);
  sqlSession.commit();
  sqlSession.close();
  ```

- Every mapper interface methods map to CRUD SQL statement elements in entity-mapping xml. Every CURD SQL statement element is parsed to a `MappedStatement` object.

- MyBatis using JDK dynamic proxy to create objects of Mapper Interfaces. When you call mapper proxy object methods, the method call will dispatch to the `MappedStatement` object to execute its SQL statement.

### How to Write MyBatis Paging SQL?

### How MyBatis Convert ResultSet to Entity Objects?

### How Maper Interface Bind SQL Annotations?

### Mapper Implementation Ways?



## MyBatis APIs

## Dynamic SQL

### What is Dynamic SQL?

Dynamic SQL can deal with:

- to conditionally concatenate strings of SQL together.
- making sure not to forget spaces or to omit a comma at the end of a list of columns. 

The Dynamic SQL elements should be familiar to anyone who has used JSTL or any similar XML based text processors. In previous versions of MyBatis, there were a lot of elements to know and understand. MyBatis 3 greatly improves upon this, and now there are less than half of those elements to work with. MyBatis employs powerful OGNL based expressions to eliminate most of the other elements:

- if
- choose (when, otherwise)
- trim (where, set)
- foreach

Example of `foreach`:

```xml
<delete id="deleteAll">
    delete from t_department
    where id in
    <foreach item="item" index="index" collection="entities"
             open="(" separator="," close=")">
        #{item.id}
    </foreach>
</delete>
```

Example of `trim` and `if`

```xml
<update id="updateSelective" parameterType="com.taogen.example.mybatis.sqlmap.xml.entity.Department">
    update t_department
    <trim prefix="SET" suffixOverrides=",">
        modify_time = NOW(),
        <if test="name != null">
            name = #{name,jdbcType=VARCHAR},
        </if>
        <if test="deleteFlag != null">
            delete_flag = #{deleteFlag,jdbcType=BIT},
        </if>
    </trim>
    where id = #{id,jdbcType=INTEGER}
</update>
```



## Stored Procedure Support

## Advanced Topics

### How MyBatis Lazy Load works?

### What is MyBatis One-Level Cache and Second-Level Cache?

## Plugins

### What are Paging Plugins? 

### How MyBatis Plugin works?

### How to Write a MyBatis Plugin?

## References

[1] [面试官都会问的Mybatis面试题，你会这样回答吗？](https://juejin.im/post/6844903847270449160)