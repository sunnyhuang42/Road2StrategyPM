# SQL 常用语句

## Some of The Most Important SQL Commands

```SQL
SELECT - extracts data from a database
UPDATE - updates data in a database
DELETE - deletes data from a database
INSERT INTO - inserts new data into a database
CREATE DATABASE - creates a new database
ALTER DATABASE - modifies a database
CREATE TABLE - creates a new table
ALTER TABLE - modifies a table
DROP TABLE - deletes a table
CREATE INDEX - creates an index (search key)
DROP INDEX - deletes an index
        
``` 



## 基础命令 
```SQL
mysql-ctl start
 
mysql-ctl cli
 
mysql-ctl stop
 
exit;
 
quit;
 
\q;
 
ctrl-c
        
``` 

## CREATE

## READ

### 筛选某列特定数据

```SQL
SELECT * FROM Customers
WHERE City = "London" OR Country = "UK";

SELECT * FROM Customers
WHERE Country='Germany' AND (City='Berlin' OR City='München');
 
WHERE Age >= 18;    
WHERE Address IS NOT NULL;   
```



```SQL
SELECT * 
FROM products
ORDER BY Price DESC;
  
SELECT * FROM `members` ORDER BY `gender`,`date_of_birth` DESC;      
``` 


```SQL
SELECT 
    customerName,
    COUNT(*) AS 'number of orders'
FROM customers
INNER JOIN orders
	ON orders.customerID = customers.customerID
GROUP BY customers.customerID;
        
``` 

```SQL
SELECT 
    username,
    photos.id,
    photos.image_url, 
    COUNT(*) AS total
FROM photos
INNER JOIN likes
    ON likes.photo_id = photos.id
INNER JOIN users
    ON photos.user_id = users.id
GROUP BY photos.id
ORDER BY total DESC
LIMIT 1;
        
``` 

```SQL
SELECT first_name, 
       last_name, 
       Count(rating)                    AS COUNT, 
       Ifnull(Min(rating), 0)           AS MIN, 
       Ifnull(Max(rating), 0)           AS MAX, 
       Round(Ifnull(Avg(rating), 0), 2) AS AVG, 
       CASE 
         WHEN Count(rating) >= 10 THEN 'POWER USER' 
         WHEN Count(rating) > 0 THEN 'ACTIVE' 
         ELSE 'INACTIVE' 
       end                              AS STATUS 
FROM   reviewers 
       LEFT JOIN reviews 
              ON reviewers.id = reviews.reviewer_id 
GROUP  BY reviewers.id; 
        
``` 



## UPDATE

### 插入数据

```SQL
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');        
``` 

```SQL
UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;       
``` 


## DELETE




### 删除某个表

```SQL
DROP TABLE customers;
        
``` 



