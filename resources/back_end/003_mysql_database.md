# Database

## Create Database
Before you start to doing CRUD, you must create a database first by this command:
```sql
CREATE DATABASE databasename;
```
For example, you want to create database named students. You can use this command:
```sql
CREATE DATABASE schoolDB;
```
## Drop Database
If you want to drop an existing database, you can use this command:
```sql
DROP DATABASE databasename;
```
For example:
```sql
DROP DATABASE schoolDB;
```

# Table
Now you have a database, before you want to query the data, you should create a table first.

## Create Table 
The `CREATE TABLE` statement is used to create a new table in a database.
<br>
<br>
For example, if you want a table contains `id`, `name`, `student_id`, `class`, you can use this command:

```sql
CREATE TABLE students (
    id int,
    name varchar(255),
    student_id varchar(255),
    class varchar(255),
);
```
`students` means the name of the table, `id` means name of the column 1, `int` means the data type of `id`, and so on.
<br>
<br>

If you run the command, you have created an empty table named `students`. The empty `students` table will now look like this:
id | name | student_id | class
-- | ---- | ---------- | -----

## Drop Table
If you want to drop an existing table, you can use this command:
```sql
DROP TABLE table_name;
```
For example, you want to drop the `students` table, you can use this command:
```sql
DROP TABLE students;
```
But if you want to delete the data inside a table, but not the table itself, you can use `truncate table`, the command looks like this:
```sql
TRUNCATE TABLE students;
```

## Alter Table
So now you have an existing table. But somehow you want to restructure the existing table. You can use `alter table` to add, delete, or modify columns in an existing table.

### Add Column
To add a column in a table, use the following command:
```sql
ALTER TABLE table_name
ADD column_name datatype;
```

### Drop Column
To delete a column in a table, use the following command:
```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

### Modify Column
To change the data type of a column in a table, use the following command:
```sql
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
```
And that's all for MySQL Database, next we are going to talk about MySQL Constraint.
<br>
GLHF!!!