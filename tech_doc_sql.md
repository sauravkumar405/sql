
# SQL

## Introduction

- Number of query languages in use - around 50 are popular, both commercially and for research purposes.

- The most popular and widely accepted query language is SQL (Structures Query Language).

- SQL is domain specific not general purpose, used in design and management of data held in RDBMS.

- SQL define structure of a database, modify can do much more than just query a database, it can define structure of a database, modify data in database, specify security constraints and number of other tasks.

- SQL is based on relational algebra and tuple relational calculus

## History

- IBM developed original varsion of SQL called  SEQUEL IN Project R in early 1970's.

- Named later changed to SQL because of trademark issues.

- In 1986, American National Standard Institute (ANSI) and ISO published SQL standard called SQL-86.

- Subsequent versions, 1989, 1996,1999, 2003, 2006, 2008, 2011 and most recently 2016 were released.

## Classification of SQl

***

These SQL commands are mainly categorized into four categories as:

- DDL – Data Definition Language
- DQl – Data Query Language
- DML – Data Manipulation Language
- DCL – Data Control Language

1. **Data Definition Language (DDL) -**

    DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema. It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.

    >CREATE – is used to create the database or its objects (like table, index, function, views, store procedure and triggers).

    >DROP – is used to delete objects from the database.

    >ALTER-is used to alter the structure of the database.

    >TRUNCATE–is used to remove all records from a table, including all spaces allocated for the records are removed.

2. **Data Query Language (DQL) -**

    DQL statements are used for performing queries on the data within schema objects. The purpose of the DQL Command is to get some schema relation based on the query passed to it.

    >SELECT – is used to retrieve data from the database.

3. **Data Manipulation Language (DML) -**

    The SQL commands that deals with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.

    >INSERT – is used to insert data into a table.

    >UPDATE – is used to update existing data within a table.

    >DELETE – is used to delete records from a database table.

4. **Data Control Language (DCL) -**

    DCL includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions and other controls of the database system.

    >GRANT-gives users access privileges to the database.

    >REVOKE-withdraw user’s access privileges given by using the GRANT command.

## Basic Queries in SQL

Let us first look at a sample table in which we will apply our upcoming queries

### **SELECT**

***
SELECT statement in SQL is used to select data from the database. Select statement is the most frequently used key word in an SQL command. It selects datafrom a table and presents it in the form of a table itself.

```SQL
SELECT column1, column2, ...
FROM table_name; 
```

### **SELECT DISTICT**

***

SELECT DISTINCT is used to select distinct and unique data from the database. In basic SELECT statement we select the particular column data which we want to get as an output, and this column may contain some dublicate data but when we use the DISTINCT keyword we get only the distinct column attributes.

```SQL
SELECT DISTINCT column1, column2, ...
FROM table_name; 
```

### **WHERE**

***

The WHERE clause in SQL used to filter out result from a database based on some condition given along with it. It is used along with the SELECT statement and is mentioned at the end of the SQL statement along with its condition.

```SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition; 
```

### **AND / OR /NOT**

***

AND and OR keywords are used to combine two or more conditions given in an SQL statement. AND keyword is used to combine two or more conditions and states that all the conditions should be true. OR keywords are used to state that any one of the given conditions needs to be true in a statement. Whereas NOT keyword is used to reverse the outcome of a condition.

```SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...; 
```

```SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...; 
```

```SQL
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition; 
```

### **ORDER BY**

***
The ORDER BY clause in SQL is used to sort the result-set table in ascending or descending order as per specifies in the SQL statement. ORDER BY clause is written at the last of a SQL statement after the WHERE clause.

```SQL
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC; 
```

### **INSERT INTO**

***
The INSERT INTO statement is used to insert new records in an existing table in a database. the INSERT INTO statements can be used in two forms.

1. Specify both the column names and the values to be inserted:

```SQL
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...); 
```

2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the INSERT INTO syntax would be as follows:

```SQL
INSERT INTO table_name
VALUES (value1, value2, value3, ...); 
```

### **UPDATE**

***
The UPDATE statement in SQL is used to update the data of an existing table in database. We can update single columns as well as multiple columns using UPDATE statement as per our requirement.

```SQL
UPDATE table_name SET column1 = value1, column2 = value2,... 
WHERE condition;
```

### **DELETE**

***

DELETE statements are used to delete records from an existing table in a Database. We should be very careful while using the DELETE and DROP commands in SQL, because these are used to remove permanently a record or table from a database.


```SQL
DELETE FROM table_name WHERE condition; 
```

### **MIN() / MAX()**

***
MIN and MAX are aggregate functions used in SQL to filter out the maximum or minimum value from a column in a database table. These are very useful commands and also the most frequent one because it is used in carrying out many statistical data calculations. The MIN() function returns the smallest value of the selected column. The MAX() function returns the largest value of the selected column.

```SQL
SELECT MIN(column_name)
FROM table_name
WHERE condition; 
```

```SQL
SELECT MAX(column_name)
FROM table_name
WHERE condition; 
```

### **COUNT / AVG / SUM**

***
There are some more aggregate functions in sql which are very useful and frequently used. Some of them are COUNT(), AVG() and SUM().

- COUNT() - This function is used to count the number of records that corresponds to a column in other words it outputs the number of attributes specifies in a given column.

- AVG() - This function is used to calculate the average of all the values present in a column.

- SUM() - Sum function is used to calculate the total sum of values present in a column.

The restriction for the SUM and AVG functions is that the value present in that column should be numeric.

```SQL
SELECT COUNT(column_name)
FROM table_name
WHERE condition; 
```

```SQL
SELECT AVG(column_name)
FROM table_name
WHERE condition; 
```

```SQL
SELECT SUM(column_name)
FROM table_name
WHERE condition; 
```

### **LIKE**

***
The SQL LIKE operator is primarily used to match substrings and pattern present in a column. It is used along with WHERE clause.
There are two wildcards often used in conjunction with the LIKE operator:

- The percent sign (%) represents zero, one, or multiple characters

- The underscore sign ( _ ) represents one, single character

```SQL
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```

### **IN**

***

The sql IN operator is used in place of OR operator in cases where we have a big dataset and to filter out similar values from the table which is also present in dataset using the OR  operator will be very tedious and non-practical.

```SQL
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...); 
```
