# summury 
## What is SQL?
![img](https://cdn.educba.com/academy/wp-content/uploads/2019/03/What-is-SQL-1.jpg)
#### SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

## Relational databases
Before learning the SQL syntax, it's important to have a model for what a relational database actually is. A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

For example, if the Department of Motor Vehicles had a database, you might find a table containing all the known vehicles that people in the state are driving. This table might need to store the model name, type, number of wheels, and number of doors of each vehicle for example.
## About the lessons
#### Since most users will be learning SQL to interact with an existing database, the lessons begin by introducing you to the various parts of an SQL query. The later lessons will then show you how to alter a table (or schema) and create new tables from scratch.
## SELECT queries 101
#### To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries. A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. It has a specific syntax though, which is what we are going to learn in the following exercises.
` Select query for a specific columns
SELECT column, another_column, …
FROM mytable `
#### and 
` Select query for all columns
SELECT * 
FROM mytable; `
![img2](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSE3YHV-QmszCAzc9buApNf_RgUosRmcdwDVQ&usqp=CAU)
## Queries with constraints
#### Now we know how to select for specific columns of data from a table, but if you had a table with a hundred million rows of data, reading through all the rows would be inefficient and perhaps even impossible.

In order to filter certain results from being returned, we need to use a ` WHERE ` clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.
` Select query with constraints
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …; `
    
##### example :
###### Find the first 5 Pixar movies and their release year
` SELECT title, year FROM movies
WHERE year <= 2003; `


## Filtering and sorting Query results
#### Even though the data in a database may be unique, the results of any particular query may not be – take our Movies table for example, many different movies can be released the same year. In such cases, SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.
` Select query with unique results
SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s); `
 ` Select query with limited rows
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset; ` 
#### example :
##### ist the next five Pixar movies sorted alphabetically 
` SELECT title FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 5; `




