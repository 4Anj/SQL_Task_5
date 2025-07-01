# Task 5: SQL Joins 
Objective
Learn to combine data from multiple related tables using SQL JOINs: INNER JOIN, LEFT JOIN, RIGHT JOIN, and a simulated FULL OUTER JOIN.

## Tools Used
MySQL Workbench

SQL (Structured Query Language)

## Tables Created
1. Customers
```sql
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    CustomerName VARCHAR(100),
    Country VARCHAR(50)
);

INSERT INTO Customers VALUES(1, 'Alice', 'India');
INSERT INTO Customers VALUES(2, 'Bob', 'USA');
INSERT INTO Customers VALUES(3, 'Charlie', 'UK');
INSERT INTO Customers VALUES(4, 'Diana', 'India');
```

2. Orders
```sql
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    OrderAmount DECIMAL(10,2)
);

INSERT INTO Orders VALUES(101, 1, 500.00);
INSERT INTO Orders VALUES(102, 2, 300.00);
INSERT INTO Orders VALUES(103, 3, 700.00);
INSERT INTO Orders VALUES(104, 4, 400.00);
```
## SQL JOIN Queries
🔸 1. INNER JOIN
Returns only the rows with matching CustomerID in both tables.

```sql
SELECT C.CustomerName, O.OrderID, O.OrderAmount
FROM Customers C
INNER JOIN Orders o ON C.CustomerID = O.CustomerID;
```

🔸 2. LEFT JOIN
Returns all customers, and any matching orders.

```sql
SELECT C.CustomerID, O.OrderID, O.OrderAmount
FROM Customers C
left JOIN Orders o ON C.CustomerID = O.CustomerID;
```

🔸 3. RIGHT JOIN
Returns all orders, and any matching customers.

```sql
SELECT C.CustomerName, c.CustomerID, O.OrderID, O.OrderAmount
FROM Customers c
RIGHT JOIN Orders o ON C.CustomerID = O.CustomerID;
```

🔸 4. FULL OUTER JOIN (Simulated using UNION)
Combines results from both LEFT JOIN and RIGHT JOIN to simulate a full join.

```sql
SELECT C.CustomerName, c.country, o.OrderID, O.OrderAmount
FROM Customers c
LEFT JOIN Orders o ON C.CustomerID = O.CustomerID

UNION

SELECT C.CustomerName, c.country,  O.OrderID, O.OrderAmount
FROM Customers c
RIGHT JOIN Orders o ON C.CustomerID = O.CustomerID;
```
