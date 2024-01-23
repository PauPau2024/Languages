# **<span style="font-size: 21px">SQL (Standard Language for Storing)</span>** 

```
SELECT * FROM Customers;    //Print ths Entier DataBase Named "Customer"
```

- <span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">MySQL, SQL Server, MS Access, Oracle, Sybase, Informix, Postgres, and other database systems are Subparts of SQL.</span>

## <span style="font-size: 15px">What Can SQL do?</span>

- <span style="font-size: 14px">SQL can execute queries against a database</span>
- <span style="font-size: 14px">SQL can retrieve data from a database</span>
- <span style="font-size: 14px">SQL can insert records in a database</span>
- <span style="font-size: 14px">SQL can update records in a database</span>
- <span style="font-size: 14px">SQL can delete records from a database</span>
- <span style="font-size: 14px">SQL can create new databases</span>
- <span style="font-size: 14px">SQL can create new tables in a database</span>
- <span style="font-size: 14px">SQL can create stored procedures in a database</span>
- <span style="font-size: 14px">SQL can create views in a database</span>
- <span style="font-size: 14px">SQL can set permissions on tables, procedures, and views</span>

## <span style="font-size: 17px">Database Tables</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">A database most often contains one or more tables. Each table is identified by a name (e.g. "Customers" or "Orders"), and contain records (rows) with data.</span>

- SQL keywords are NOT case sensitive: `select` is the same as `SELECT`

## <span style="font-size: 17px">Some of The Most Important SQL Commands:</span>

- `SELECT` - extracts data from a database
- `UPDATE` - updates data in a database
- `DELETE` - deletes data from a database
- `INSERT INTO` - inserts new data into a database
- `CREATE DATABASE` - creates a new database
- `ALTER DATABASE` - modifies a database
- `CREATE TABLE` - creates a new table
- `ALTER TABLE` - modifies a table
- `DROP TABLE` - deletes a table
- `CREATE INDEX` - creates an index (search key)
- `DROP INDEX` - deletes an index

  ---

# <span style="font-size: 19px">SQL SELECT Statement:-</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`SELECT`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement is used to select data from a database.</span>

## Syntax:

```
SELECT column1, column2, ...FROM table_name;
```

<span style="font-size: 15px">Here, column1, column2, ... are the </span>*<span style="font-size: 15px">field names</span>*<span style="font-size: 15px"> of the table you want to select data from.The table_name represents the name of the </span>*<span style="font-size: 15px">table</span>*<span style="font-size: 15px"> you want to select data from.</span>

**<span style="font-size: 15px">Example:</span>** 

```
SELECT CustomerName, City FROM Customers;
```

## <span style="font-size: 19px">Select ALL columns</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To return all columns, without specifying every column name, you can use the </span>`SELECT *`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> syntax:</span>

```
SELECT * FROM Customers;
```

---

# <span style="font-size: 19px">SQL SELECT DISTINCT Statement:-</span>

`SELECT DISTINCT`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement is used to return only distinct (different) values.</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Inside a table, a column often contains many duplicate values; and sometimes you only want to list the different (distinct) values.</span>

## Syntax

```
SELECT DISTINCT column1, column2, ...FROM table_name;
```

---

# SQL WHERE Clause:-

<span style="font-size: 15px">The </span>`WHERE`<span style="font-size: 15px"> clause is used to filter records.It is used to extract only those records that fulfill a specified condition.</span>

## Syntax

```
SELECT column1, column2, ...FROM table_name
WHERE condition;
```

**<span style="font-size: 15px">Example:</span>**

```
SELECT * FROM Customers
WHERE Country='Mexico';
```

<span style="font-size: 15px">SQL requires single quotes around text values (most database systems will also allow double quotes).However, numeric fields should not be enclosed in quotes:</span>

## <span style="font-size: 17px">Operators in The WHERE Clause:</span>

<table>
<tbody><tr><td colspan="1" rowspan="1"><p>=</p></td><td colspan="1" rowspan="1"><p>Equal</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&gt;</p></td><td colspan="1" rowspan="1"><p>Greater than</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&lt;</p></td><td colspan="1" rowspan="1"><p>Less than</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&gt;=</p></td><td colspan="1" rowspan="1"><p>Greater than or equal</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&lt;=</p></td><td colspan="1" rowspan="1"><p>Less than or equal</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&lt;&gt;</p></td><td colspan="1" rowspan="1"><p>Not equal. <strong>Note:</strong> In some versions of SQL this operator may be written as !=</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>BETWEEN</p></td><td colspan="1" rowspan="1"><p>Between a certain range</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>LIKE</p></td><td colspan="1" rowspan="1"><p>Search for a pattern</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>IN</p></td><td colspan="1" rowspan="1"><p>To specify multiple possible values for a column</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody>
</table>

**<span style="font-size: 15px">Example For Each Operator:</span>**

```
SELECT * FROM Customers 
WHERE customer_id = 1

SELECT * FROM Customers 
WHERE customer_id > 1

SELECT * FROM Customers 
WHERE customer_id < 1

SELECT * FROM Customers 
WHERE customer_id >= 1

SELECT * FROM Customers 
WHERE customer_id <= 1

SELECT * FROM Customers 
WHERE customer_id <> 1    //Customer ID=1 will not be present in Output

SELECT * FROM Customers 
WHERE customer_id BETWEEN 1 AND 5 

SELECT * FROM Customers 
WHERE customer_name LIKE 's%' //Output with 's' present in name 

SELECT * FROM Customers
WHERE City IN ('Paris','London'); //Output Rows with only Paris&London in City Colomn
```

---

# SQL ORDER BY:-

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`ORDER BY`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword is used to sort the result-set in ascending or descending order.</span>

## Syntax:

```
SELECT column1, column2, ...FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

**<span style="font-size: 17px">Example:</span>**

```
SELECT * FROM Products
ORDER BY Price ASC;  //Not mentioning ASC|DESC with take ASC by Default
```

## <span style="font-size: 17px">ORDER BY Several Columns:</span>

```
SELECT * FROM Customers
ORDER BY Country, CustomerName;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The following SQL statement selects all customers from the "Customers" table, sorted by the "Country" and the "CustomerName" column. This means that it orders by Country, but if some rows have the same Country, it orders them by CustomerName.</span>

## <span style="font-size: 17px">Using Both ASC and DESC:</span>

```
SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The following SQL statement selects all customers from the "Customers" table, sorted ascending by the "Country" and descending by the "CustomerName" column.</span>

---

# SQL AND Operator:-

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`AND`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator is used to filter records based on more than one condition, like if you want to return all customers from Spain that starts with the letter 'G'.</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause can contain one or many </span>`AND`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operators.</span>

## Syntax

```
SELECT column1, column2, ...FROM table_name
WHERE condition1 
AND condition2 
AND condition3 ...;
```

## AND vs OR

`AND`<span style="font-size: 15px"> operator displays a record if </span>*<span style="font-size: 15px">all</span>*<span style="font-size: 15px"> the conditions are TRUE.</span>

<span style="font-size: 15px"> </span>`OR`<span style="font-size: 15px"> operator displays a record if </span>*<span style="font-size: 15px">any</span>*<span style="font-size: 15px"> of the conditions are TRUE.</span>

## <span style="font-size: 19px">Combining AND and OR:</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The following SQL statement selects all customers from Spain that starts with a "G" or an "R".</span>

```
SELECT * FROM Customers
WHERE Country = 'Spain' 
AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');
```

---

# <span style="font-size: 21px">SQL OR Operator:-</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`OR`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator is used to filter records based on more than one condition</span>

`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause can contain one or more </span>`OR`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operators.</span>

## Syntax

```
SELECT column1, column2, ...FROM table_name
WHERE condition1 
OR condition2 
OR condition3 ...;
```

---

# <span style="font-size: 21px">SQL </span><span style="font-size: 21px">NOT</span><span style="font-size: 21px"> Operator</span>:-

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`NOT`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator is used in combination with other operators to give the opposite result, also called the negative result.</span>

## Syntax

```
SELECT column1, column2, ...FROM table_name
WHERE NOT condition;
```

**<span style="font-size: 17px">Example:</span>** 

```
SELECT * FROM Customers
WHERE NOT Country = 'Spain';
```

---

# <span style="font-size: 21px">SQL </span><span style="font-size: 21px">INSERT INTO</span><span style="font-size: 21px"> Statement:-</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`INSERT INTO`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement is used to insert new records in a table.</span>

**<span style="font-size: 19px">Syntax: </span><span style="font-size: 17px">INSERT INTO</span>**<span style="font-size: 17px"> </span>

<span style="font-size: 15px">It is possible to write the </span>`INSERT INTO`<span style="font-size: 15px"> statement in two ways:</span>

<span style="font-size: 15px">1. Specify both the column names and the values to be inserted:</span>

```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the </span>`INSERT INTO`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> syntax would be as follows:</span>

```
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

**<span style="font-size: 17px">Example:</span>**

```
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```

## Insert Multiple Rows

### <span style="font-size: 17px">Example:</span>

```
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway'),
('Greasy Burger', 'Per Olsen', 'Gateveien 15', 'Sandnes', '4306', 'Norway'),
('Tasty Tee', 'Finn Egan', 'Streetroad 19B', 'Liverpool', 'L1 0AA', 'UK');
```

---

**<span style="font-size: 21px">SQL </span><span style="font-size: 21px">NULL Values:-</span>**

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!</span>

## <span style="font-size: 19px">How to Test for NULL Values?</span>

`IS NULL`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> and </span>`IS NOT NULL`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operators</span>

**<span style="font-size: 17px">Syntax : IS NULL</span>**

`IS NULL`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator is used to test for empty values (NULL values).</span>

```
SELECT column_names FROM table_name
WHERE column_name IS NULL;  //column parameter which is null
```

**<span style="font-size: 17px">Syntax : IS  NOT NULL</span>**

`IS NOT NULL`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator is used to test for non-empty values (NOT NULL values).</span>

```
SELECT column_names FROM table_name
WHERE column_name IS NOT NULL;
```

---

# <span style="font-size: 21px">SQL UPDATE Statement:-</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`UPDATE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement is used to modify the existing records in a table.</span>

**<span style="font-size: 19px">Syntax:</span>**

```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;  
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">when updating records in a table! Notice the </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause in the </span>`UPDATE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement. The </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause specifies which record(s) that should be updated. If you omit the </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause, all records in the table will be updated!</span>

### Example

```
UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If you omit the </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause, ALL records will be updated!</span>

### Example

```
UPDATE CustomersSET 
ContactName='Juan';
```

---

# <span style="font-size: 21px">SQL DELETE Statement:-</span>

`DELETE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement is used to delete existing records in a table.</span>

**<span style="font-size: 19px">Syntax:</span>**

```
DELETE FROM table_name 
WHERE condition;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">when deleting records in a table! Notice the </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause in the </span>`DELETE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement. The </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause specifies which record(s) should be deleted. If you omit the </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause, all records in the table will be deleted!</span>

```
DELETE FROM Customers 
WHERE CustomerName='Alfreds Futterkiste';
```

## <span style="font-size: 17px">Delete All Records:</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Delete all rows in a table without deleting the table</span>

```
DELETE FROM table_name;
```

## <span style="font-size: 17px">Delete a Table:</span>

<span style="font-size: 15px">To delete the table completely, use the </span>`DROP TABLE`<span style="font-size: 15px"> statement:</span>

### Example:

```
DROP TABLE Customers;
```

---

# <span style="font-size: 21px">SQL SELECT TOP Clause:-</span>

<span style="font-size: 15px">The </span>`SELECT TOP`<span style="font-size: 15px"> clause is used to specify the number of records to return.</span>

<span style="font-size: 15px">The </span>`SELECT TOP`<span style="font-size: 15px"> clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.</span>

**<span style="font-size: 19px">Example:</span>**

```
SELECT TOP 3 * FROM Customers;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Not all database systems support the </span>`SELECT TOP`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause. MySQL supports the </span>`LIMIT`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause to select a limited number of records, while Oracle uses </span>`FETCH FIRST n ROWS ONLY`

## LIMIT (MySQL) :

```
SELECT * FROM Customers
LIMIT 3;
```

## FETCH FIRST (Oracle) :

```
SELECT * FROM Customers
FETCH FIRST 3 ROWS ONLY;
```

## SQL TOP PERCENT (SQL Server/MS Access) :

```
SELECT TOP 50 PERCENT * FROM Customers;
```

## <span style="font-size: 21px">ADD a WHERE CLAUSE:-</span>

### <span style="font-size: 19px">Example</span>

```
SELECT TOP 3 * FROM Customers
WHERE Country='Germany';
```

---

**<span style="font-size: 21px">SQL MIN() and MAX() Functions:-</span>**

<span style="font-size: 15px">The </span>`MIN()`<span style="font-size: 15px"> function returns the smallest value of the selected column.</span>

<span style="font-size: 15px">The </span>`MAX()`<span style="font-size: 15px"> function returns the largest value of the selected column.</span>

## Syntax:

```
SELECT MIN(column_name) 
FROM table_name
WHERE condition;
```

```
SELECT MAX(column_name)
FROM table_name
WHERE condition;
```

## Set Column Name (Alias):

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">When you use </span>`MIN()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> or </span>`MAX()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, the returned column will be named </span>`MIN(field)`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> or </span>`MAX(field)`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> by default. To give the column a new name, use the </span>`AS`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword:</span>

### <span style="font-size: 19px">Example</span>

```
SELECT MIN(Price) AS SmallestPrice
FROM Products;
```

---

# <span style="font-size: 21px">SQL COUNT() Function:-</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`COUNT()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> function returns the number of rows that matches a specified criterion.</span>

**<span style="font-size: 19px">Syntax :</span>**

```
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
```

### <span style="font-size: 19px">Example:</span>

```
SELECT COUNT(*)
FROM Products;
```

## <span style="font-size: 19px">Ignore Duplicates: </span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If </span>`DISTINCT`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> is specified, rows with the same value for the specified column will be counted as one.</span>

### <span style="font-size: 19px">Example:</span>

```
SELECT COUNT(DISTINCT Price)
FROM Products;
```

## Use an Alias:

```
SELECT COUNT(*) AS [number of records]
FROM Products;
```

---

# <span style="font-size: 23px">SQL SUM() Function:</span>

The `SUM()` function returns the total sum of a numeric column.

## Syntax

```
SELECT SUM(column_name)
FROM table_name
WHERE condition;
```

### <span style="font-size: 19px">Example</span>

```
SELECT SUM(Quantity)
FROM OrderDetails;
```

---

# <span style="font-size: 23px">SQL AVG() Function:</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`AVG()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> function returns the average value of a numeric column.</span>

## Syntax

```
SELECT AVG(column_name)
FROM table_name
WHERE condition;
```

## Higher Than Average:

<span style="font-size: 15px">To list all records with a higher price than average, we can use the </span>`AVG()`<span style="font-size: 15px"> function in a sub query:</span>

### <span style="font-size: 19px">Example</span>

<span style="font-size: 15px">Return all products with a higher price than the average price:</span>

```
SELECT * FROM Products
WHERE price > (SELECT AVG(price) FROM Products);
```

---

**<span style="font-size: 23px">SQL LIKE Operator:</span>**

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`LIKE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator is used in a </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause to search for a specified pattern in a column.</span>

<span style="font-size: 15px">There are two wildcards often used in conjunction with the </span>`LIKE`<span style="font-size: 15px"> operator:</span>

- <span style="font-size: 15px"> The percent sign </span>`%`<span style="font-size: 15px"> represents zero, one, or multiple characters</span>
- <span style="font-size: 15px"> The underscore sign </span>`_`<span style="font-size: 15px"> represents one, single character</span>

## Syntax

```
SELECT column1, column2, ...
FROM table_name
WHERE columnN 
LIKE pattern;
```

## The \_ Wildcard :

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">It can be any character or number, but each </span>`_`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> represents one, and only one, character.</span>

### <span style="font-size: 19px">Example:</span>

```
SELECT * FROM Customers
WHERE city LIKE 'L_nd__';
```

## The % Wildcard :

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`%`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> wildcard represents any number of characters, even zero characters.</span>

### <span style="font-size: 21px">Example:</span>

```
SELECT * FROM Customers
WHERE city LIKE '%L%';
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To return records that starts with a specific letter or phrase, add the </span>`%`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> at the end of the letter or phrase.  //</span><span style="font-family: Consolas, Menlo, courier new, monospace; color: mediumblue; font-size: 15px">LIKE</span><span style="font-family: Consolas, Menlo, courier new, monospace; color: rgb(0, 0, 0); font-size: 15px"> </span><span style="font-family: Consolas, Menlo, courier new, monospace; color: brown; font-size: 15px">'La%'</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To return records that ends with a specific letter or phrase, add the </span>`%`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> at the beginning of the letter or phrase.  //</span><span style="font-family: Consolas, Menlo, courier new, monospace; color: mediumblue; font-size: 15px">LIKE</span><span style="font-family: Consolas, Menlo, courier new, monospace; color: rgb(0, 0, 0); font-size: 15px"> </span><span style="font-family: Consolas, Menlo, courier new, monospace; color: brown; font-size: 15px">'%a'</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To return records that contains a specific letter or phrase, add the </span>`%`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> both before and after the letter or phrase.  //</span><span style="font-family: Consolas, Menlo, courier new, monospace; color: mediumblue; font-size: 15px">LIKE</span><span style="font-family: Consolas, Menlo, courier new, monospace; color: rgb(0, 0, 0); font-size: 15px"> </span><span style="font-family: Consolas, Menlo, courier new, monospace; color: brown; font-size: 15px">'%or%'</span>

## <span style="font-size: 21px">the \[\] Wildcard:</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`[]`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> wildcard returns a result if </span>*any*<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> of the characters inside gets a match.</span>

### <span style="font-size: 19px">Example :</span>

```
SELECT * FROM Customers
WHERE CustomerName LIKE '[bsp]%';
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Return all customers starting with either "b", "s", or "p".</span>

## th<span style="font-size: 21px">e - Wildcard :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`-`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> wildcard allows you to specify a range of characters inside the </span>`[]`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> wildcard.</span>

### <span style="font-size: 21px">Example :</span>

```
SELECT * FROM Customers
WHERE CustomerName LIKE '[a-f]%';
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Return all customers starting with "a", "b", "c", "d", "e" or "f".</span>

## Without Wildcard :

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If no wildcard is specified, the phrase has to have an exact match to return a result.</span>

```
SELECT * FROM Customers
WHERE Country LIKE 'Spain';
```

---

# <span style="font-size: 23px">SQL IN Operator :</span>

<span style="font-size: 15px">The </span>`IN`<span style="font-size: 15px"> operator allows you to specify multiple values in a </span>`WHERE`<span style="font-size: 15px"> clause.</span>

<span style="font-size: 15px">The </span>`IN`<span style="font-size: 15px"> operator is a shorthand for multiple </span>`OR`<span style="font-size: 15px"> conditions.</span>

## <span style="font-size: 21px">Syntax</span>

```
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
```

### <span style="font-size: 21px">Example</span>

<span style="font-size: 15px">Return all customers from 'Germany', 'France', or 'UK'</span>

```
SELECT * FROM Customers
WHERE Country IN ('Germany', 'France', 'UK');
```

## <span style="font-size: 23px">NOT IN :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">By using the </span>`NOT`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword in front of the </span>`IN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator, you return all records that are NOT any of the values in the list.</span>

### <span style="font-size: 21px">Example</span>

<span style="font-size: 15px">Return all customers that are NOT from 'Germany', 'France', or 'UK':</span>

```
SELECT * FROM Customers
WHERE Country NOT IN ('Germany', 'France', 'UK');
```

## IN (SELECT):

```
SELECT * FROM Customers
WHERE CustomerID IN (SELECT CustomerID FROM Orders);
```

## NOT IN (SELECT) : 

```
SELECT * FROM Customers
WHERE CustomerID NOT IN (SELECT CustomerID FROM Orders);
```

---

# SQL BETWEEN Operator :

<span style="font-size: 15px">The </span>`BETWEEN`<span style="font-size: 15px"> operator selects values within a given range. The values can be numbers, text, or dates.</span>

<span style="font-size: 15px">The </span>`BETWEEN`<span style="font-size: 15px"> operator is inclusive: begin and end values are included. </span>

## <span style="font-size: 19px">Syntax</span>

```
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

## NOT BETWEEN : 

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To display the products outside the range of the previous example, use </span>`NOT BETWEEN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">:</span>

```
SELECT * FROM Products
WHERE Price NOT BETWEEN 10 AND 20;
```

## BETWEEN with IN :

**<span style="font-size: 19px">Example :</span>**

```
SELECT * FROM Products
WHERE Price BETWEEN 10 AND 20
AND CategoryID IN (1,2,3);
```

```
SELECT * FROM Products
WHERE ProductName 
BETWEEN "Carnarvon Tigers" AND "Chef Anton's Cajun Seasoning"
ORDER BY ProductName;
```

```
SELECT * FROM Orders
WHERE OrderDate 
BETWEEN '1996-07-01' AND '1996-07-31';
```

---

# **<span style="font-size: 23px">SQL Aliases :</span>**

<span style="font-size: 15px">SQL aliases are used to give a table, or a column in a table, a temporary name.Aliases are often used to make column names more readable.</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">An alias is created with the </span>`AS`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword.</span>

## Syntax

<span style="font-size: 15px">When alias is used on column:</span>

```
SELECT column_name AS alias_name
FROM table_name;
```

<span style="font-size: 15px">When alias is used on table:</span>

```
SELECT column_name(s)
FROM table_name AS alias_name;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If you want your alias to contain one or more spaces, like "</span>`My Great Products`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">", surround your alias with square brackets or double quotes.</span>

```
SELECT ProductName AS [My Great Products]
FROM Products;
```

```
SELECT ProductName AS "My Great Products"
FROM Products;
```

---

## <span style="font-size: 23px">Concatenate Columns</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The following SQL statement creates an alias named "Address" that combine four columns (Address, PostalCode, City and Country):</span>

```
SELECT CustomerName, Address + ', ' + PostalCode + ' ' + City + ', ' + Country AS Address
FROM Customers;
```

### MySQL Example :

```
SELECT CustomerName, CONCAT(Address,', ',PostalCode,', ',City,', ',Country) AS Address
FROM Customers;
```

### Oracle Example :

```
SELECT CustomerName, (Address || ', ' || PostalCode || ' ' || City || ', ' || Country) AS Address
FROM Customers;
```

---

## <span style="font-size: 23px">SQL JOIN :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">A </span>`JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause is used to combine rows from two or more tables, based on a related column between them.</span>

## Different Types of SQL JOINs :

- `(INNER) JOIN`: <span style="font-size: 15px">Returns records that have matching values in both tables</span>

![SQL INNER JOIN](https://www.w3schools.com/sql/img_inner_join.png)- <span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> </span>`LEFT (OUTER) JOIN`: <span style="font-size: 15px">Returns all records from the left table, and the matched records from the right table</span>

![SQL LEFT JOIN](https://www.w3schools.com/sql/img_left_join.png)- <span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> </span>`RIGHT (OUTER) JOIN`: <span style="font-size: 15px">Returns all records from the right table, and the matched records from the left table</span>

![SQL RIGHT JOIN](https://www.w3schools.com/sql/img_right_join.png)- <span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> </span>`FULL (OUTER) JOIN`<span style="font-size: 15px">: Returns all records when there is a match in either left or right table</span>

![SQL FULL OUTER JOIN](https://www.w3schools.com/sql/img_full_outer_join.png)---

## INNER JOIN : 

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`INNER JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword selects records that have matching values in both tables.</span>

## Syntax

```
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`INNER JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword returns only rows with a match in both tables. Which means that if you have a product with no CategoryID, or with a CategoryID that is not present in the Categories table, that record would not be returned in the result.</span>

### <span style="font-size: 19px">Example</span>

<span style="font-size: 15px">Join Products and Categories with the INNER JOIN keyword:</span>

```
SELECT ProductID, ProductName, CategoryName
FROM ProductsINNER 
JOIN Categories 
ON Products.CategoryID = Categories.CategoryID;
```

`JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> and </span>`INNER JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> will return the same result.</span>

## JOIN Three Tables

### Example

```
SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
FROM ((Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID)
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);
```

---

## <span style="font-size: 23px">LEFT JOIN :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`LEFT JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.</span>

### <span style="font-size: 21px">Syntax</span>

```
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

---

## <span style="font-size: 23px">RIGHT JOIN :</span>

<span style="font-size: 15px">The </span>`RIGHT JOIN`<span style="font-size: 15px"> keyword returns all records from the right table (table2), and the matching records from the left table (table1). The result is 0 records from the left side, if there is no match.</span>

### <span style="font-size: 19px">Syntax</span>

```
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">In some databases </span>`RIGHT JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> is called </span>`RIGHT OUTER JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">.</span>

---

## <span style="font-size: 23px">FULL OUTER JOIN :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`FULL OUTER JOIN`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword returns all records when there is a match in left (table1) or right (table2) table records</span>

### <span style="font-size: 21px">Syntax</span>

```
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```

**<span style="font-size: 19px">Example :</span>**

```
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```

---

# <span style="font-size: 23px">SQL Self Join : </span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">A self join is a regular join, but the table is joined with itself.</span>

### <span style="font-size: 19px">Self Join Syntax :</span>

```
SELECT column_name(s)
FROM table1 T1, table1 T2
WHERE condition;
```

### <span style="font-size: 19px">Example :</span>

```
SELECT A.CustomerName AS CustomerName1, B.CustomerName AS CustomerName2, A.City
FROM Customers A, Customers B
WHERE A.CustomerID <> B.CustomerID
AND A.City = B.City
ORDER BY A.City;
```

---

**<span style="font-size: 23px">SQL UNION Operator :</span>** 

<span style="font-size: 15px">The </span>`UNION`<span style="font-size: 15px"> operator is used to combine the result-set of two or more </span>`SELECT`<span style="font-size: 15px"> statements.</span>

- <span style="font-size: 15px">Every </span>`SELECT`<span style="font-size: 15px"> statement within </span>`UNION`<span style="font-size: 15px"> must have the same number of columns</span>
- <span style="font-size: 15px">The columns must also have similar data types</span>
- <span style="font-size: 15px">The columns in every </span>`SELECT`<span style="font-size: 15px"> statement must also be in the same order</span>

**<span style="font-size: 19px">UNION Syntax :</span>**

```
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`UNION`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator selects only distinct values by default. To allow duplicate values, use </span>`UNION ALL`

```
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```

## <span style="font-size: 21px">SQL UNION With WHERE :</span>

```
SELECT City, Country FROM Customers
WHERE Country='Germany'
UNION
SELECT City, Country FROM Suppliers
WHERE Country='Germany'
ORDER BY City;
```

---

# <span style="font-size: 23px">SQL GROUP BY Statement :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`GROUP BY`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement groups rows that have the same values into summary rows</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`GROUP BY`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> statement is often used with aggregate functions (</span>`COUNT()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, </span>`MAX()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, </span>`MIN()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, </span>`SUM()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, </span>`AVG()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">) to group the result-set by one or more columns.</span>

### <span style="font-size: 19px">Syntax :</span>

```
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```

---

## <span style="font-size: 23px">SQL HAVING Clause :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`HAVING`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> clause was added to SQL because the </span>`WHERE`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword cannot be used with aggregate functions.</span>

### <span style="font-size: 19px">Syntax :</span>

```
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
```

**<span style="font-size: 19px">Example :</span>** 

```
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5;
```

---

## <span style="font-size: 23px">SQL EXISTS Operator : </span>

<span style="font-size: 15px">The </span>`EXISTS`<span style="font-size: 15px"> operator is used to test for the existence of any record in a subquery.</span>

<span style="font-size: 15px">The </span>`EXISTS`<span style="font-size: 15px"> operator returns TRUE if the subquery returns one or more records.</span>

### <span style="font-size: 19px">EXISTS Syntax :</span>

```
SELECT column_name(s)
FROM table_name
WHERE EXISTS
(SELECT column_name FROM table_name WHERE condition);
```