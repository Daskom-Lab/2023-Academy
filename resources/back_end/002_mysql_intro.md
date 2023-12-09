# MySQL Intro

Welcome to MySQL course. First of all, you must know what MySQL is

## What is MySQL???
MySQL is a very popular open-source relational database management system (RDBMS). Some huge websites uses MySQL as their database management system. We can create, read, update, and delete data or we usually hear as CRUD.

## What is RDBMS???
RDBMS stands for Relational Database Management System. RDBMS is a program used to maintain a relational database. RDBMS uses SQL queries to access the data in the database. 
<br>
<br>
RDBMS uses table to display data. A table is a collection of related data entries, and it consists of columns and rows. A column holds specific information about every record in the table. A row is each individual entry that exists in a table.
<br>
Look at a selection from the Northwind `Customers` table:

### Customer Table
 CustomerID  | CustomerName	                      | ContactName    | Address                       | City        | PostalCode | Country  
 ----------- | ---------------------------------- | -------------- | ----------------------------- | ----------- | ---------- | ------- 
1            | Alfreds Futterkiste                | Maria Anders   | Obere Str. 57                 | Berlin      | 12209      | Germany 
2	         | Ana Trujillo Emparedados y helados | Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  
3	         | Antonio Moreno Taquería            | Antonio Moreno | Mataderos 2312                | México D.F. | 05023      | Mexico  

The columns in the `Customers` table above are: CustomerID, CustomerName, ContactName, Address, City, PostalCode and Country. The table has 3 rows.
<br>
<br>
A relational database defines database relationships in the form of tables. The tables are related to each other - based on data common to each.
<br>
Look at the following three tables `Customers`, `Orders`, and `Shippers` from the Northwind database:

### Customer Table
 <span style="color:green;">CustomerID<span> | CustomerName	                      | ContactName    | Address                       | City        | PostalCode | Country  
 ------------------------------------------- | ---------------------------------- | -------------- | ----------------------------- | ----------- | ---------- | ------- 
 <span style="color:green;">1 <span>         | Alfreds Futterkiste                | Maria Anders   | Obere Str. 57                 | Berlin      | 12209      | Germany 
 <span style="color:green;">2<span>	         | Ana Trujillo Emparedados y helados | Ana Trujillo   | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  
 <span style="color:green;">3<span>	         | Antonio Moreno Taquería            | Antonio Moreno | Mataderos 2312                | México D.F. | 05023      | Mexico  

The relationship between the `Customers` table and the `Orders` table is the `CustomerID` column:

### Orders Table
 OrderID	| <span style="color:green;">CustomerID<span>	  | EmployeeID	  | OrderDate  | <span style="color:purple;">ShipperID<span> 
 ---------- | ----------------------------------------------- | ------------- | ---------- | ------------------------------------------
 10278      | <span style="color:green;">1<span>              | 8             | 1996-08-12 | <span style="color:purple;">2<span>         
 10280	    | <span style="color:green;">3<span>              | 2             | 1996-08-14 | <span style="color:purple;">1<span>
 10308	    | <span style="color:green;">2<span>              | 7             | 1996-09-18 | <span style="color:purple;">3<span>
 10355      | <span style="color:green;">1<span>              | 6             | 1996-11-15 | <span style="color:purple;">1<span>
 10365	    | <span style="color:green;">3<span>              | 3             | 1996-11-27 | <span style="color:purple;">2<span>
 10383	    | <span style="color:green;">2<span>              | 8             | 1996-12-16 | <span style="color:purple;">3<span>
 10384	    | <span style="color:green;">2<span>              | 3             | 1996-12-16 | <span style="color:purple;">3<span>

The relationship between the `Orders` table and the `Shippers` table is the `ShipperID` column:

### Shippers Table
<span style="color:purple;">ShipperID<span> |	ShipperName     | Phone
------------------------------------------- | ----------------- | -----
<span style="color:purple;">1<span>         | Speedy Express	| (503) 555-9831
<span style="color:purple;">2<span>         | United Package	| (503) 555-3199
<span style="color:purple;">3<span>         |Federal Shipping	| (503) 555-9931

## What is SQL Queries???
SQL is the standard language for dealing with Relational Databases. SQL is usually used to create, read, update, and delete data records.
For example if you want to read data from `Customers Table` you can use this query
```sql
SELECT * FROM Customers;
```
SQL query are not case-sensitive so `SELECT` and `select` are the same things.
<br>
<br>
Some of The Most Important SQL Commands:
- CREATE DATABASE
- DROP DATABASE
- CREATE TABLE
- ALTER TABLE
- DROP TABLE
- UNIQUE
- PRIMARY KEY
- FOREIGN KEY
- SELECT
- WHERE
- UPDATE
- DELETE
- INSERT INTO
- ORDER BY
- AND, OR, NOT
- JOINS

Alright, now you have to give it a try. First turn on your MySQL, then open the command prompt, type mysql and enter, so you can use MySQL command there.
<br>
GLHF!!!