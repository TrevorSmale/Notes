## MySQL Functions

### 1. CONCAT
The `CONCAT` function is used to concatenate two or more strings together. It takes multiple string arguments and returns a single string that is the concatenation of all the input strings.

Example:
```sql
SELECT CONCAT('Hello', ' ', 'World') AS Result;
```
Output:
```
Hello World
```

### 2. SUBSTRING
The `SUBSTRING` function allows you to extract a substring from a given string. It takes three arguments: the input string, the starting position, and the length of the substring to be extracted.

Example:
```sql
SELECT SUBSTRING('Hello World', 7, 5) AS Result;
```
Output:
```
World
```

### 3. DATE_FORMAT
The `DATE_FORMAT` function is used to format a date or time value according to a specified format. It takes two arguments: the date or time value and the format string specifying the desired output format.

Example:
```sql
SELECT DATE_FORMAT(NOW(), '%Y-%m-%d') AS Result;
```
Output:
```
2023-05-24
```

### 4. COUNT
The `COUNT` function is used to count the number of rows in a result set or the number of occurrences of a specified expression. It can be used with the `*` wildcard or a specific column name.

Example:
```sql
SELECT COUNT(*) AS TotalRows FROM table;
```
Output:
```
TotalRows: 10
```

### 5. AVG
The `AVG` function calculates the average value of a numeric column in a table. It takes a column name as an argument and returns the average value.

Example:
```sql
SELECT AVG(column) AS AverageValue FROM table;
```
Output:
```
AverageValue: 25.5
```

### 6. MAX
The `MAX` function returns the maximum value from a specified column in a table. It can be used with numeric, string, or date/time columns.

Example:
```sql
SELECT MAX(column) AS MaxValue FROM table;
```
Output:
```
MaxValue: 100
```

### 7. MIN
The `MIN` function returns the minimum value from a specified column in a table. It is similar to the `MAX` function but returns the smallest value instead.

Example:
```sql
SELECT MIN(column) AS MinValue FROM table;
```
Output:
```
MinValue: 10
```

### 8. SUM
The `SUM` function calculates the sum of all values in a numeric column. It takes a column name as an argument and returns the total sum.

Example:
```sql
SELECT SUM(column) AS TotalSum FROM table;
```
Output:
```
TotalSum: 1000
```

### 9. ROUND
The `ROUND` function is used to round a numeric value to a specified number of decimal places. It takes two arguments: the input value and the number of decimal places.

Example:
```sql
SELECT ROUND(3.14159, 2) AS RoundedValue;
```
Output:
```
RoundedValue: 3.14
```

### 10. NOW
The `NOW` function returns the current date and time in the format 'YYYY-MM-DD HH:MM:SS'. It does not require any arguments.

Example:
```sql
SELECT NOW() AS CurrentDateTime;
```
Output:
```
CurrentDateTime: 2023-05-24 10:30:00
```

### 11. GROUP_CONCAT
The

 `GROUP_CONCAT` function concatenates the values of a specified column into a single string, separated by a specified delimiter. It can also apply an ordering to the concatenated values.

Example:
```sql
SELECT GROUP_CONCAT(column ORDER BY column ASC SEPARATOR ', ') AS ConcatenatedValues FROM table;
```
Output:
```
ConcatenatedValues: value1, value2, value3
```

### 12. IFNULL
The `IFNULL` function returns the first non-null expression in a list. It takes two arguments: the first expression and the second expression to be returned if the first one is null.

Example:
```sql
SELECT IFNULL(column, 'N/A') AS Result FROM table;
```
Output:
```
Result: value or N/A
```

### 13. LOWER
The `LOWER` function converts a string to lowercase. It takes a string as an argument and returns the lowercase version of the string.

Example:
```sql
SELECT LOWER('Hello World') AS Result;
```
Output:
```
Result: hello world
```

### 14. UPPER
The `UPPER` function converts a string to uppercase. It takes a string as an argument and returns the uppercase version of the string.

Example:
```sql
SELECT UPPER('Hello World') AS Result;
```
Output:
```
Result: HELLO WORLD
```

### 15. TRIM
The `TRIM` function removes leading and trailing spaces from a string. It takes a string as an argument and returns the string with leading and trailing spaces removed.

Example:
```sql
SELECT TRIM('   Hello World   ') AS Result;
```
Output:
```
Result: Hello World
```

## MySQL Actions

### 1. SELECT
The `SELECT` statement is used to retrieve data from one or more tables in a database. It allows you to specify the columns to be retrieved and the conditions for filtering the data.

Example:
```sql
SELECT column1, column2 FROM table WHERE condition;
```

### 2. INSERT
The `INSERT` statement is used to insert new rows into a table. It allows you to specify the table name, the column names, and the values to be inserted.

Example:
```sql
INSERT INTO table (column1, column2) VALUES (value1, value2);
```

### 3. UPDATE
The `UPDATE` statement is used to modify existing rows in a table. It allows you to set new values for one or more columns based on specified conditions.

Example:
```sql
UPDATE table SET column1 = value1, column2 = value2 WHERE condition;
```

### 4. DELETE
The `DELETE` statement is used to delete one or more rows from a table. It allows you to specify conditions to filter the rows to be deleted.

Example:
```sql
DELETE FROM table WHERE condition;
```

### 5. CREATE
The `CREATE` statement is used to create a new table, view, or index in a database. It allows you to specify the table structure, column names, data types, and constraints.

Example:
```sql
CREATE TABLE table (column1 datatype, column2 datatype, ...);
```

### 6. ALTER
The `ALTER` statement is used to modify the structure of an existing table. It allows you to add or drop columns, change column data types, and modify table constraints.

Example:
```sql
ALTER TABLE table ADD column datatype;
```

### 7. DROP
The `DROP` statement is used to delete an existing table, view, or index from a database. It permanently removes the specified object and all associated data.

Example:
```sql
DROP TABLE table;
```

### 8. TRUNCATE
The `TRUNCATE` statement is used to delete all rows from a table while keeping its structure intact. It is faster than the DELETE statement as it does not generate individual delete operations.

Example:
```sql
TRUNCATE TABLE table;
```

### 9. GRANT
The `GRANT` statement is used to grant specific privileges to a user or a user group in a database. It allows you to control access and permissions for different database objects.

Example:
```sql
GRANT privilege ON database.object TO user;
```

### 10. REVOKE
The `REVOKE` statement is used to revoke previously granted privileges from a user or a user group. It allows you to remove access and permissions for specific database objects.

Example:
```sql
REVOKE privilege ON database.object FROM user;
```

### 11. COMMIT
The `COMMIT` statement is used to save all the changes made in the current transaction. It makes the changes permanent and releases any locks held on the affected data.

Example:
```sql
COMMIT;
```

### 12. ROLLBACK
The `ROLLBACK` statement is used to undo all the changes made in the current transaction. It restores the data to its original state before the transaction began.

Example:
```sql
ROLLBACK;
```

### 13. SAVEPOINT
The `SAVEPOINT` statement is used to create a named point within a transaction. It allows you to mark a specific point to which you can roll back if needed.

Example:
```sql
SAVEPOINT savepoint_name;
```

### 14

. START TRANSACTION
The `START TRANSACTION` statement is used to begin a new transaction. It sets a starting point for a series of database operations that can be either committed or rolled back.

Example:
```sql
START TRANSACTION;
```

### 15. SET AUTOCOMMIT
The `SET AUTOCOMMIT` statement is used to control the automatic commit behavior for each SQL statement. It determines whether each statement is committed immediately or waits for an explicit commit.

Example:
```sql
SET AUTOCOMMIT = 0;
```

```
