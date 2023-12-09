# MySQL Operators

MySQL operators are kind of similar with boolean operators in C. There are `AND`, `OR`, and `NOT`. 
<br>

## AND
The `AND` operator displays a record if all the conditions separated by `AND` are TRUE.
<br>
For example, you want the students that registered in `class` 04 with `name` Vincent to be shown, you can execute the following syntax:

```sql
SELECT * FROM students WHERE name = 'Vincent' AND class = '04';
```
The output will be like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
4  | Vincent   | 1102211234 | 04
## OR

The `OR` operator displays a record if any of the conditions separated by `OR` is TRUE.
<br>
For example, you want students that registered in `class` 04 or 05 to be shown, you can execute the following syntax:

```sql
SELECT * FROM students WHERE class = '04' OR class = '05';
```
The output will be like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
4  | Vincent   | 1102211234 | 04
2  | Svendson  | 1102213061 | 05
## NOT
The `NOT` operator displays a record if the condition(s) is `NOT` TRUE.
<br>
For example, you do not want the students that registered in `class` 05 to be shown, you can execute the following syntax:

```sql
SELECT * FROM students WHERE NOT class = '05';
```
The output will be like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
4  | Vincent   | 1102211234 | 04
3  | Pettersen | 1102213062 | 06