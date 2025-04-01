## 1. What is PostgreSQL?
### Ans : 
PostgreSQL is an open-source object-relational database management system known for its scalability, stability. 

## 2. What is the purpose of a database schema in PostgreSQL? 
### Ans  : 
A database schema in PostgreSQL is like a folder that organizes different database objects. It helps keep things organized, prevents naming problems, and allows control over who can access specific parts of the database. 

## 3. Explain the Primary Key and Foreign Key concepts in PostgreSQL. 
### Ans  : 
Primary Key: Uniquely identifies each record in a table. </br>
Foreign Key: Make relationship between two tables by referencing a primary key.

## 4.What is the difference between the VARCHAR and CHAR data types? 
### Ans : 
VARCHAR: Stores variable-length strings.</br>
CHAR: Stores fixed-length strings, padding with spaces.

## 5. Explain the purpose of the WHERE clause in a SELECT statement. 
### Ans  : 
The WHERE clause filters rows based on specified conditions.

## 6. What are the LIMIT and OFFSET clauses used for? 
### Ans  : 
LIMIT: Restricts the number of rows returned. </br>
OFFSET: Skips a specified number of rows.

## 7. How can you modify data using UPDATE statements? 
### Ans  :  
The UPDATE statement changes existing data in a table based on specified conditions.
```
UPDATE customers
SET name = 'Alice'
WHERE id = 1; 

```

## 8. What is the significance of the JOIN operation, and how does it work in PostgreSQL? 
### Ans : 
The JOIN operation in PostgreSQL is used to combine rows from two or more tables based on a related column.
```
SELECT * FROM customers
 JOIN orders ON customers.id = orders.customer_id; 
```

## 9. Explain the GROUP BY clause and its role in aggregation operations. 
### Ans  :
 The GROUP BY clause groups rows based on column values to apply aggregate functions like COUNT(), SUM(), etc.

```
SELECT customer_id, COUNT(*) FROM orders
GROUP BY customer_id;

```
## 10. How can you calculate aggregate functions like COUNT(), SUM(), and AVG() in PostgreSQL? 
### Ans :
1. COUNT(): Counts the number of rows in a set. </br>
   ```
   SELECT COUNT(*) FROM orders;

   ```
2. SUM(): Calculates the total sum of a numeric column. </br>
   ```
   SELECT SUM(order_amount) FROM orders;

   ```
3. SUM(): Calculates the total sum of a numeric column. </br>
   ```
   SELECT AVG(order_amount) FROM orders;

   ```

   