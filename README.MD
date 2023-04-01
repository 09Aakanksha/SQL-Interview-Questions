# SQL Interview Questions

## Q. What is a database?
A database is a structured collection of data that is organized and stored in a way that allows efficient retrieval and 
manipulation of the data. A database typically contains one or more tables or files that are related to each other in 
some way.

## Q. What is DBMS?
A database management system (DBMS) is used to manage and manipulate data within a database. A DBMS is a software system 
that provides tools for creating, storing, retrieving, updating, and deleting data in a database. 

Examples of popular DBMSs include MySQL, Oracle, Microsoft SQL Server, and PostgreSQL.

## Q. What kind of data can be stored in databases?
Databases can be used to store various types of data, such as customer information, sales data, financial records, 
product catalogs, and so on. Databases can also be used for a wide range of applications, such as e-commerce, online 
banking, inventory management, and healthcare.

## Q. What are different types of databases?
There are a variety of database types, and which type you use will be dependent on the type of data you wish to store. 
Let’s look at a few popular database types:

### Relational databases
These databases are laid out in rows and columns, store and provide data in multiple tables, and allow you to identify 
and access the data in relation to one another. All relational databases use SQL. 
Microsoft SQL Server is an example of a relational database management system.

### NoSQL databases
Any database that does not use SQL as its primary language. These databases are better suited for those who do not want 
their data as structured. CouchDB is an example of a NoSQL database.

## Q. What is SQL?
In order to access and manipulate data in a database, users typically use a structured query language (SQL), which is a
programming language designed for managing data in a relational database. SQL is used to create, modify, and retrieve 
data in a database.

SQL also allows users to perform complex queries and analyze large volumes of data quickly and efficiently.

## Q. What is SQL used for?
Some of the most common uses of SQL include:

### Querying data
SQL is used to retrieve data from a database using various query techniques, such as SELECT, FROM, WHERE, and JOIN. 
This allows users to filter, sort, and aggregate data in a meaningful way. 
### Inserting and updating data
SQL is used to add new records to a database or update existing records. This is done using the INSERT, UPDATE, and DELETE commands.
### Creating and modifying database structures
SQL is used to create and modify database structures, such as tables, indexes, and constraints. This allows users to define 
the structure and relationships of the data in a database. 
### Managing user access and security
SQL is used to manage user access and security in a database, such as creating users, granting and revoking privileges, 
and setting up security policies. 
### Performing data analysis
SQL is used to perform complex data analysis tasks, such as aggregating and summarizing data, calculating statistics, and 
generating reports.

## Q. What are statements in SQL?
In SQL, a statement is a command or instruction that is used to interact with a database. SQL statements are used to
perform various operations on a database, such as querying data, inserting new records, updating existing records,
deleting records, creating tables, altering tables, and so on.

## Q. What are different kinds of SQL statements?
SQL statements are categorized into different types based on their functionality. Some common types of SQL statements include:

### Data Definition Language (DDL) statements
These statements are used to define the database schema, such as creating tables, altering tables, and dropping tables.
Examples: CREATE, ALTER, DROP, etc.
### Data Manipulation Language (DML) statements
These statements are used to manipulate data in the database, such as inserting data, updating data, deleting data, and querying data.
Examples: INSERT, UPDATE, DELETE, SELECT, etc. 
### Data Control Language (DCL) statements
These statements are used to control access to the database, such as granting and revoking permissions.
Examples: GRANT, LOCK, REVOKE, etc.
### Transaction Control Language (TCL) statements
These statements are used to control transactions in the database, such as committing transactions and rolling back transactions.
Examples: COMMIT, ROLLBACK, SAVEPOINT, etc.

## Q. What is RDBMS?
RDBMS stands for Relational Database Management System. The key difference here, compared to DBMS, is that RDBMS stores 
data in the form of a collection of tables, and relations can be defined between the common fields of these tables. 
Examples: MySQL, Microsoft SQL Server, Oracle, IBM DB2, etc.

## Q. What is a table in SQL?
In SQL, a table is a collection of data organized in rows and columns. Each row represents a single record, and each 
column represents a specific data element or attribute of that record. Tables are the basic building blocks of a 
relational database, and are used to store and organize data in a structured way.

For example, a table might be used to store customer data for an e-commerce website, with each row representing a single 
customer and each column representing a different attribute of that customer, such as their name, address, and email address.

Tables can be created using the CREATE TABLE statement in SQL, which allows users to specify the name of the table, the 
names and data types of the columns, and any constraints on the data. 
Once a table has been created, data can be inserted into the table using the INSERT statement, and queried using the SELECT statement.

Tables can be modified using the ALTER TABLE statement, which allows users to add, remove, or modify columns, change data 
types, and add or remove constraints. They can also be dropped using the DROP TABLE statement, which deletes the table 
and all of its data from the database.

## Q. What is a primary key in SQL?
In SQL, a primary key is a column or a set of columns in a table that uniquely identifies each record in the table. 
The primary key serves as a unique identifier for each row in the table and is used to enforce data integrity constraints.

Some key characteristics of a primary key include:
### Uniqueness
Each value in the primary key column(s) must be unique, meaning that no two rows can have the same value for the primary key.
### Non-nullability
Each value in the primary key column(s) must be non-null, meaning that no row can have a null value for the primary key.
### Permanence
The primary key value(s) must not change over the lifetime of the row, as this would cause data integrity issues.
### Minimality
The primary key should consist of as few columns as possible while still ensuring uniqueness.

In most SQL database management systems, a primary key is created by specifying the PRIMARY KEY constraint on one or more 
columns when creating a table. The primary key can also be added to an existing table using the ALTER TABLE statement.

The use of a primary key in SQL tables allows for efficient querying and manipulation of data, as well as enforcing 
referential integrity with other tables through the use of foreign keys.

## Q. What is a foreign key in SQL?
In SQL, a foreign key is a field or set of fields in a table that refers to the primary key of another table. 
A foreign key establishes a link between two tables, allowing data to be associated between them.

For example, consider two tables: **orders** and **customers**. The **orders** table might have a foreign key column called 
**customer_id**, which refers to the **id** primary key column in the **customers** table. This allows each order in the 
**orders** table to be associated with a specific customer in the **customers** table.

Some key characteristics of a foreign key include:
### Referential integrity
The foreign key establishes a referential integrity constraint between the two tables, ensuring that data in the 
**orders** table is consistent with data in the **customers** table.
### One-to-many relationships
A foreign key can be used to represent a one-to-many relationship between two tables, where one record in the parent 
table can have many associated records in the child table.
### Cascade actions
Cascade actions can be defined on foreign keys to specify what should happen when records in the parent table are deleted 
or updated. For example, a cascade delete action might delete all associated records in the child table when a record in 
the parent table is deleted.

Foreign keys can be defined using the FOREIGN KEY constraint when creating a table or using the ALTER TABLE statement to 
modify an existing table. Foreign keys can also be used in combination with indexes to improve the performance of queries 
that join multiple tables.

## Q. Explain CREATE TABLE statement with example.
This statement is used to create a new table in the database. 
For example, the following statement creates a new table called **customers** with columns for *customer ID*, *name*, and *email address*:

```roomsql
CREATE TABLE customers (
  id INT PRIMARY KEY,
  name VARCHAR(50),
  email VARCHAR(50)
);
```

## Q. Explain ALTER TABLE statement with example.
This statement is used to modify the structure of an existing table, such as adding a new column or changing the data type 
of column. 
For example, the following statement adds a new column called *phone* to the *customers* table:
```roomsql
ALTER TABLE customers
ADD COLUMN phone VARCHAR(20);
```

## Q. Explain DROP TABLE statement with example.
This statement is used to delete an entire table from the database. 
For example, the following statement deletes the *customers* table:
```roomsql
DROP TABLE customers;
```

## Q. Explain TRUNCATE TABLE statement with example.
This statement is used to delete all data from a table without deleting the table itself. 
For example, the following statement deletes all data from the *customers* table:
```roomsql
TRUNCATE TABLE customers;
```

## Q. Explain CREATE INDEX statement with example.
This statement is used to create an index on one or more columns of a table, which can improve the performance of queries 
that filter or sort data based on those columns. 
For example, the following statement creates an index on the *name* column of the *customers* table:
```roomsql
CREATE INDEX idx_customers_name ON customers(name);
```

## Q. Explain SELECT statement with example.
This statement is used to retrieve data from one or more tables in the database. 
For example, the following statement retrieves all columns from the *customers* table:
```roomsql
SELECT * FROM customers;
```
If we wish to select specific column(s) from the table then we need to specified those columns, separated by comma
```roomsql
SELECT name, email FROM customers;
```

## Q. Explain INSERT INTO statement with example.
This statement is used to insert new data into a table. 
For example, the following statement inserts a new record into the *customers* table:
```roomsql
INSERT INTO customers (name, email)
VALUES ('John Smith', 'john@example.com');
```

## Q. Explain UPDATE statement with example.
This statement is used to modify existing data in a table. 
For example, the following statement updates the email address of the customer with an ID of 1 in the "customers" table:
```roomsql
UPDATE customers
SET email = 'newemail@example.com'
WHERE id = 1;
```

## Q. Explain DELETE FROM statement with example.
This statement is used to delete data from a table. 
For example, the following statement deletes the record for the customer with an ID of 2 from the "customers" table:
```roomsql
DELETE FROM customers
WHERE id = 2;
```

## Q. Explain MERGE statement with example.
This statement is used to perform an *upsert* operation, which inserts a new row if it does not exist or updates an 
existing row if it does. 
For example, the following statement inserts a new record into the *customers* table if a record with the same email 
address does not exist, or updates the existing record if it does:
```roomsql
MERGE INTO customers AS target
USING (VALUES ('john@example.com', 'John Smith')) AS source (email, name)
ON target.email = source.email
WHEN NOT MATCHED THEN
  INSERT (email, name)
  VALUES (source.email, source.name)
WHEN MATCHED THEN
  UPDATE SET name = source.name;
```

## Q. Explain GRANT statement with example.
This statement is used to give users specific privileges to access objects in the database. 
For example, the following statement grants SELECT and INSERT privileges on the *customers* table to a user named *user1*:
```roomsql
GRANT SELECT, INSERT ON customers TO user1;
```

## Q. Explain REVOKE statement with example.
This statement is used to remove user privileges from objects in the database. 
For example, the following statement revokes the SELECT privilege on the *customers* table from the user named *user1*:
```roomsql
REVOKE SELECT ON customers FROM user1;
```

## Q. Explain DENY statement with example.
This statement is used to deny access to objects in the database, overriding any granted privileges. 
For example, the following statement denies the DELETE privilege on the *orders* table to the user named *user2*:
```roomsql
DENY DELETE ON orders TO user2;
```

## Q. Explain COMMIT statement with example.
This statement is used to permanently save changes made to the database since the last COMMIT or ROLLBACK statement. 
For example, the following statement commits all changes made in the current transaction:
```roomsql
COMMIT;
```

## Q. Explain ROLLBACK statement with example.
This statement is used to undo changes made to the database since the last COMMIT or ROLLBACK statement. 
For example, the following statement rolls back all changes made in the current transaction:
```roomsql
ROLLBACK;
```

## Q. How do you add primary key in a table?
- Create table with a single field as primary key in a new table
```roomsql
CREATE TABLE Students (
   ID INT NOT NULL
   Name VARCHAR(255)
   PRIMARY KEY (ID)
);
```
- Create table with multiple fields as primary key in a new table
```roomsql
CREATE TABLE Students (
   ID INT NOT NULL
   LastName VARCHAR(255)
   FirstName VARCHAR(255) NOT NULL,
   CONSTRAINT PK_Student
   PRIMARY KEY (ID, FirstName)
);
```
- Set a column as primary key in already existing table
```roomsql
ALTER TABLE Students   
ADD PRIMARY KEY (ID);
```
- Set multiple columns as primary key in already existing table
```roomsql
ALTER TABLE Students   
ADD CONSTRAINT PK_Student   /* Naming a Primary Key */
PRIMARY KEY (ID, FirstName);
```

## Q. How do you add foreign key in a table?
- Adding a foreign key to a new table. In this example, a new table *orders* is created with a foreign key constraint that 
references the *customer_id* column in the *customers* table.
```roomsql
CREATE TABLE orders (
   order_id INT PRIMARY KEY,
   customer_id INT,
   order_date DATE,
   FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
);
```
- Adding a foreign key to an already existing table. In this example, an existing *orders* table is altered to add a 
foreign key constraint named *fk_customer_id* that references the *customer_id* column in the *customers* table.
```roomsql
ALTER TABLE orders
ADD CONSTRAINT fk_customer_id
FOREIGN KEY (customer_id) REFERENCES customers(customer_id);
```

## Q. What are CONSTRAINTS in SQL?
Constraints are used to specify the rules concerning data in the table. It can be applied for single or multiple fields 
in an SQL table during the creation of the table or after creating using the ALTER TABLE command. The constraints are:

- NOT NULL - Restricts NULL value from being inserted into a column.
- CHECK - Verifies that all values in a field satisfy a condition.
- DEFAULT - Automatically assigns a default value if no value has been specified for the field.
- UNIQUE - Ensures unique values to be inserted into the field.
- INDEX - Indexes a field providing faster retrieval of records.
- PRIMARY KEY - Uniquely identifies each record in a table.
- FOREIGN KEY - Ensures referential integrity for a record in another table.

## Q. What is a UNIQUE constraint?
A UNIQUE constraint ensures that all values in a column are different. This provides uniqueness for the column(s) and 
helps identify each row uniquely. 

Unlike primary key, there can be multiple unique constraints defined per table. The code syntax for UNIQUE is quite similar
to that of PRIMARY KEY and can be used interchangeably.

## Q. Write some examples of adding UNIQUE constraint in a table
- Create table with a single field as unique

```roomsql
CREATE TABLE Students (
ID INT NOT NULL UNIQUE
Name VARCHAR(255)
);
```
- Create table with multiple fields as unique
```roomsql
CREATE TABLE Students (
ID INT NOT NULL
LastName VARCHAR(255)
FirstName VARCHAR(255) NOT NULL
CONSTRAINT PK_Student
UNIQUE (ID, FirstName)
);
```
- Set a column as unique
```roomsql
ALTER TABLE Students   
ADD UNIQUE (ID);
```
- Set multiple columns as unique
```roomsql
ALTER TABLE Students
ADD CONSTRAINT PK_Student   /* Naming a unique constraint */
UNIQUE (ID, FirstName);
```

## Q. What is a join in SQL?
In SQL, a join is a way of combining rows from two or more tables based on a related column between them.

The basic syntax of a join statement is as follows:
```roomsql
SELECT column_name(s)
FROM table1
JOIN table2
ON table1.column_name = table2.column_name;
```
Here, `table1` and `table2` are the names of the tables being joined, and `column_name` is the name of the column used 
to join the tables.

## Q. What are types of joins in SQL?
The JOIN keyword is used to specify the type of join being performed. The most common types of joins are INNER JOIN, 
LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN.
- INNER JOIN returns only the rows where there is a match in both tables based on the specified join condition.
- LEFT JOIN returns all the rows from the left table and the matching rows from the right table. If there is no match in the right table, the result will contain null values.
- RIGHT JOIN returns all the rows from the right table and the matching rows from the left table. If there is no match in the left table, the result will contain null values.
- FULL OUTER JOIN returns all the rows from both tables, with null values where there is no match in either table.

## Q. Explain INNER JOIN with example
INNER JOIN is a type of SQL join used to combine rows from two or more tables based on a related column between them. 
An INNER JOIN returns only the rows that have matching values in both tables, and the result set only includes the 
columns that are specified in the SELECT statement.

Here's an example of how to use INNER JOIN to join two tables:

Suppose we have two tables, `orders` and `customers`, with the following columns:

`orders` table:
```roomsql
order_id | order_date | customer_id | order_total
```
`customers` table:
```roomsql
customer_id | first_name | last_name | email
```
We can use INNER JOIN to join these tables on the `customer_id` column and select certain columns from both tables, like this:
```roomsql
SELECT orders.order_id, orders.order_date, customers.first_name, customers.last_name
FROM orders
INNER JOIN customers
ON orders.customer_id = customers.customer_id;
```
In this example, we are selecting the `order_id`, `order_date`, `first_name`, and `last_name` columns from both the orders 
and customers tables. We use the ON keyword to specify the join condition, which is that the `customer_id` column in the 
`orders` table must match the `customer_id` column in the `customers` table.

The result of this query will be a table that contains only the rows where there is a matching value in both tables, 
with the specified columns from each table. This can be useful when we need to combine data from two or more tables 
to get a more complete picture of the data we are working with.

Note that if there are rows in one table that do not have matching values in the other table, those rows will not appear 
in the result set when using INNER JOIN. If you want to include all the rows from one table, even if there are no 
matching values in the other table, you can use LEFT JOIN or RIGHT JOIN instead.

## Q. Explain LEFT (OUTER) JOIN with example.
LEFT OUTER JOIN is a type of SQL join used to combine rows from two or more tables based on a related column between them. 
A LEFT OUTER JOIN returns all the rows from the left table and the matching rows from the right table, and if there is no 
match in the right table, the result set will contain NULL values for the right table columns.

Here's an example of how to use LEFT OUTER JOIN to join two tables:

Suppose we have two tables, `orders` and `customers`, with the following columns:

`orders` table:
```roomsql
order_id | order_date | customer_id | order_total
```
`customers` table:
```roomsql
customer_id | first_name | last_name | email
```
We can use LEFT OUTER JOIN to join these tables on the `customer_id` column and select certain columns from both tables, 
like this:
```roomsql
SELECT orders.order_id, orders.order_date, customers.first_name, customers.last_name
FROM orders
LEFT OUTER JOIN customers
ON orders.customer_id = customers.customer_id;
```
In this example, we are selecting the `order_id`, `order_date`, `first_name`, and `last_name` columns from both the `orders` 
and `customers` tables. We use the ON keyword to specify the join condition, which is that the `customer_id` column in the 
`orders` table must match the `customer_id` column in the `customers` table.

The result of this query will be a table that contains all the rows from the `orders` table, and only the matching rows 
from the `customers` table, with NULL values for the `first_name` and `last_name` columns of the `customers` table if 
there is no match. This can be useful when we want to include all the rows from one table, even if there are no matching 
values in the other table.

## Q. Explain RIGHT (OUTER) JOIN with example.
A RIGHT OUTER JOIN, also known as a right join or right outer join, is a type of database join that returns all the rows 
from the right table and only the matching rows from the left table. If there is no match in the left table, then NULL 
values are returned.

Here's an example to illustrate how a RIGHT OUTER JOIN works:

Suppose you have two tables: a `students` table and a `grades` table. The `students` table has the following columns: 
`student_id`, `first_name`, and `last_name`. The `grades` table has the following columns: `student_id`, `grade`.

`students` table:
```roomsql
|------------|------------|-----------|
| student_id | first_name | last_name |
|------------|------------|-----------|
| 1          | John       | Doe       |
| 2          | Jane       | Smith     |
| 3          | Bob        | Johnson   |
```

`grades` table:
```roomsql

|------------|-------|
| student_id | grade |
|------------|-------|
| 1          | 90    |
| 2          | 85    |
| 4          | 95    |
```
To get a list of all students and their grades (if they have any), you can use a RIGHT OUTER JOIN with the `students` 
table as the right table and the `grades` table as the left table:
```roomsql
SELECT students.first_name, students.last_name, grades.grade
FROM students
RIGHT OUTER JOIN grades
ON students.student_id = grades.student_id;
```
This would produce the following result:
```roomsql
|------------|-----------|-------|
| first_name | last_name | grade |
|------------|-----------|-------|
| John       | Doe       | 90    |
| Jane       | Smith     | 85    |
| NULL       | NULL      | 95    |
```
Notice that all the rows from the `grades` table are included in the result, even though there is no matching student in 
the `students` table for the third row. In that case, NULL values are returned for the `first_name` and `last_name` columns.

## Q. Explain FULL (OUTER) JOIN with example.
A FULL OUTER JOIN, also known as a full join, is a type of database join that returns all the rows from both tables and 
combines them into a single result set. If there is no match in either the left or the right table, then NULL values are returned.

Here's an example to illustrate how a FULL OUTER JOIN works:

Suppose you have two tables: a `students` table and a `grades` table. The `students` table has the following columns: 
`student_id`, `first_name`, and `last_name`. The `grades` table has the following columns: `student_id`, `grade`.

`students` table:
```roomsql
+------------+------------+-----------+
| student_id | first_name | last_name |
+------------+------------+-----------+
| 1          | John       | Doe       |
| 2          | Jane       | Smith     |
| 3          | Bob        | Johnson   |
+------------+------------+-----------+
```
`grades` table:
```roomsql
+------------+-------+
| student_id | grade |
+------------+-------+
| 1          | 90    |
| 2          | 85    |
| 4          | 95    |
+------------+-------+
```
To get a list of all students and their grades (if they have any), you can use a FULL OUTER JOIN:
```roomsql
SELECT students.first_name, students.last_name, grades.grade
FROM students
FULL OUTER JOIN grades
ON students.student_id = grades.student_id;
```
This would produce the following result:
```roomsql
+------------+-----------+-------+
| first_name | last_name | grade |
+------------+-----------+-------+
| John       | Doe       | 90    |
| Jane       | Smith     | 85    |
| Bob        | Johnson   | NULL  |
| NULL       | NULL      | 95    |
+------------+-----------+-------+
```
Notice that all the rows from both tables are included in the result, even though there is no matching student in the 
`students` table for the fourth row and no matching grade in the `grades` table for the third row. In those cases, 
NULL values are returned for the columns that do not have matching values.

## Q. Explain SELF JOIN with example.
A self join is a type of join in which a table is joined with itself. In other words, a self join is a way to combine 
rows from the same table based on a related column.

To perform a self join, we need to give two different aliases to the same table in the SQL statement. Each alias represents 
a separate instance of the table, and we can use them to reference the different columns within the table.

Here's an example of a self join:

Suppose we have a table named `employees` with the following columns:
```roomsql
employee_id | first_name | last_name | manager_id
```
The `manager_id` column contains the ID of the employee's manager. We can use a self join to find the names of all employees 
and their managers:
```roomsql
SELECT e.first_name AS employee_name, m.first_name AS manager_name
FROM employees e
JOIN employees m
ON e.manager_id = m.employee_id;
```

In this query, we are joining the employees table with itself using the `manager_id` and `employee_id` columns. We are using 
aliases e and m to represent the two instances of the `employees` table.

The result of this query will be a list of all employees and their managers, with the names of the employees in one column 
and the names of their managers in another column.

Self joins are particularly useful when working with hierarchical data, such as organizational charts or family trees, 
where a parent or ancestor can be represented by a row in the same table as its children or descendants.

## Q. Explain CROSS JOIN with example.
A CROSS JOIN is a type of join operation in a relational database that returns the Cartesian product of the two tables. 
In other words, it returns all possible combinations of rows from both tables.

Here's an example to illustrate how a CROSS JOIN works:

Suppose you have two tables: a `colors` table and a `sizes` table. The `colors` table has the following rows: red, blue, 
and green. The `sizes` table has the following rows: small, medium, and large. A CROSS JOIN between these two tables 
would return all possible combinations of rows:

`colors` table:
```roomsql
+-------+
| color |
+-------+
| red   |
| blue  |
| green |
+-------+
```
`sizes` table:
```roomsql
+--------+
| size   |
+--------+
| small  |
| medium |
| large  |
+--------+
```
To perform a CROSS JOIN, you would execute the following SQL query:
```roomsql
SELECT * FROM colors CROSS JOIN sizes;
```
This would produce the following result:
```roomsql
+-------+--------+
| color | size   |
+-------+--------+
| red   | small  |
| red   | medium |
| red   | large  |
| blue  | small  |
| blue  | medium |
| blue  | large  |
| green | small  |
| green | medium |
| green | large  |
+-------+--------+
```
Notice that all possible combinations of rows from the `colors` and `sizes` tables are returned, resulting in a total of 
9 rows. This can be useful for generating test data or for finding all possible combinations of two sets of data. 
However, it can also be computationally expensive, especially for large tables.

## Q. What is an index?
In SQL, an index is a database object that can speed up the retrieval of data from a table. An index is similar to an 
index in a book, in that it provides a way to quickly locate specific information within a table.

An index is created on one or more columns of a table, and it stores a copy of the indexed columns in a separate structure. 
When a query is executed that involves the indexed column(s), the database engine uses the index to quickly locate the 
relevant rows, rather than scanning the entire table. This can greatly improve the performance of queries that involve 
large tables or that require frequent searches for specific values.

Here's an example to illustrate how an index works:

Suppose you have a `students` table with the following columns: `student_id`, `first_name`, `last_name`, and `age`. 
If you frequently need to search for students by their last name, you can create an index on the `last_name` column:
```roomsql
CREATE INDEX idx_last_name ON students(last_name);
```
This creates an index named `idx_last_name` on the `last_name` column of the `students` table. The index contains a copy 
of the last name values from each row in the table, along with a pointer to the corresponding row in the table.

When you execute a query that involves the `last_name` column, such as:
```roomsql
SELECT * FROM students WHERE last_name = 'Smith';
```
The database engine can use the index to quickly locate all the rows in the `students` table where the last name is 'Smith', 
without scanning the entire table. This can significantly improve the performance of the query, especially if the table 
contains a large number of rows.

However, it's important to note that creating too many indexes or indexing the wrong columns can actually degrade 
performance, as it can increase the overhead of maintaining the indexes and may cause the database engine to use 
inefficient query plans. 

Therefore, it's important to carefully consider which columns to index and to monitor the performance of queries after 
creating indexes to ensure they are actually improving performance.

## Q. What is data integrity in SQL?
Data integrity refers to the accuracy and consistency of data stored in a database. In SQL, data integrity is maintained 
through the use of various constraints and rules that ensure that data in a database remains valid, consistent, and reliable. 
The following are some key aspects of data integrity in SQL:
### Entity integrity 
This ensures that each row in a table has a unique identifier (i.e., primary key) that distinguishes it from all other rows 
in the table.
### Referential integrity
This ensures that relationships between tables are maintained correctly. It involves enforcing constraints on foreign keys 
to ensure that they match the primary keys of the related tables.
### Domain integrity
This ensures that data values stored in a table are valid and consistent. It involves enforcing data type constraints, 
range checks, and other rules to ensure that data values are within acceptable limits.
### Check constraints
These are rules that limit the values that can be entered in a specific column. For example, a check constraint might 
limit the range of values that can be entered into a date column, or it might ensure that a column can only contain 
certain values.
### Null constraints
These are rules that specify whether a column can have a null value. For example, a column with a NOT NULL constraint 
cannot have null values.

Maintaining data integrity is crucial for ensuring the accuracy and reliability of data stored in a database. It helps to 
prevent data inconsistencies, errors, and other issues that can lead to incorrect results, data corruption, and other 
problems. Therefore, it's important to define and enforce data integrity rules in SQL databases to ensure that data remains 
consistent and reliable over time.