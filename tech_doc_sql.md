
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

## SQL Database

1. SQL CREATE Database

The SQL CREATE DATABASE statement is used by a developer to create a database.

```SQL
    CREATE DATABASE database_name;  
```

2. DROP Database

SQL DROP statement is used to delete or remove indexes from a table in the database.

If you want to delete or drop an existing database in a SQL schema, you can use SQL DROP DATABASE

Let's see the syntax of SQL DROP DATABASE:

```SQL
    DROP DATABASE database_name;  
```

3. SQL RENAME Database

In some situations, database users and administrators want to change the name of the database for some technical reasons. So, the Rename Database statement in SQL is used to change the name of the existing database.

Sometimes, the Rename Database statement is used because the developers think that the original name is not more relevant to the data of the database, or they want to give a temporary name to that database.

Syntax of Rename Database in SQL.

```SQL
    ALTER DATABASE old_database_name MODIFY NAME = new_database_name;  
```

4. SQL SELECT Database

Suppose database users and administrators want to perform some operations on tables, views, and indexes on the specific existing database in SQL. Firstly, they have to select the database on which they want to run the database queries.

Any database user and administrator can easily select the particular database from the current database server using the USE statement in SQL.

Syntax of USE statement in SQL

```SQL
    USE database_name;   
```

5. SQL Table 

Table is a collection of data, organized in terms of rows and columns. In DBMS term, table is known as relation and row as tuple.

Table is the simple form of data storage. A table is also considered as a convenient representation of relations.

Let's see an example of an employee table: