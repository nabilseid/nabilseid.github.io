---
draft: true 
date: 2024-01-15
authors:
  - almightyPush
categories:
  - Note
  - SQL
  - Big Data
---

# Notes: Big Data Analysis in SQL

This note consists of fundamental of data, fundamental of SQL, traditional databases, big data and distributed cloud storages and query engines.

<!-- more -->

!!! note 

    This is my personal note of [Modern Big Data Analysis with SQL Specialization](https://www.coursera.org/specializations/cloudera-big-data-analysis-sql). This is only intended as a personal reference.


## Fundamentals of Data

Data is a representation of something that capture some features and ignore others. What this means is that there is a selective representation based on a context, purpose, complexity, managabiluty, etc... 

- Analog Data: a continuous representation of something. It has infinite values. At any given instance or point, it has a unique continuous value.
- Digital Data: a discrete representation of something. It has finite values. It is a sample representation of analog data.

For instance, a mechanical clock has a unique value at any given instance but a digital clock has a finite values that represent a section of time duration like 1 sec to 2 sec but analog clock has infinite values between 1 sec and 2 sec.

Data is store unorganized in a data store. In order to make sense of the data and easily retrieved, data is organized. Databases are used to store organized data.

## DBMS

- Is a software that lets you organize and manage your data. It gives you an interface to store and retrieve data to and from a database and share your data.

- A DBMS should have at list these four functionalities
    - **Design** how your data is stored in the database. Different data sources will be separated and have their own features.
    - **Update/Add** records into the database.
    - **Retrieve** data from the database base to answer various questions.
    - **Control access/Manage** your data. You need to be able to create accounts and manage who has access to a particular data.

## RDBMS

- In 1970 F.E CODD's paper on relational models laid the foundation for relational databases.

- In 1974 IBM created SQL to interact with relational databases. It was originally called SEQUEL hence the ambiguous pronunciation.

- In 2000s the big data era start the rise of NoSQL for non-relational datasets. For structured data relational databases are still in high demand.

In RDBMS data is being stored in a table, collection of tables is a database. SQL is used to interact with the database. Based on the four functionalities SQL commands are categorized into 4.

**Data Definition Language(DDL)**

- CREATE - create a table
- ALTER - change table property
- DROP - remove a table

**Data Manipulation Language(DML)**

- INSERT - add record
- UPDATE - update record
- DELETE - remove record

**Data Query Language(DQL) Or Query**

- SELECT - retrieve data

**Data Control Language(DCL)**

- GRANT - give data access control
- REVOKE - take away access control

Apart from this 4 major categories there are other SQL commands. Since SQL is constantly evolving there are other commands that are not in the standard sql. Due to various reasons like competition, different RDBMS have their own SQL dialect. Although for the most part they are alike.

SQL has gain a huge acceptance even non-relational data/big data management systems and query engines use it as their primary language to interact with data. System like Hive, Impala and Athena.
