# LeetCode

# Problem
Table: Customers

+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| id          | int     |
| name        | varchar |
+-------------+---------+
id is the primary key (column with unique values) for this table.
Each row of this table indicates the ID and name of a customer.
 

Table: Orders

+-------------+------+
| Column Name | Type |
+-------------+------+
| id          | int  |
| customerId  | int  |
+-------------+------+
id is the primary key (column with unique values) for this table.
customerId is a foreign key (reference columns) of the ID from the Customers table.
Each row of this table indicates the ID of an order and the ID of the customer who ordered it.
 

Write a solution to find all customers who never order anything.

Return the result table in any order.

The result format is in the following example.

 

Example 1:

Input: 
Customers table:
+----+-------+
| id | name  |
+----+-------+
| 1  | Joe   |
| 2  | Henry |
| 3  | Sam   |
| 4  | Max   |
+----+-------+
Orders table:
+----+------------+
| id | customerId |
+----+------------+
| 1  | 3          |
| 2  | 1          |
+----+------------+
Output: 
+-----------+
| Customers |
+-----------+
| Henry     |
| Max       |
+-----------+



Solution: Find Customers Who Never Order Anything
Introduction
In this article, we will discuss a solution to find all customers who never order anything. We will provide a detailed explanation of the code provided and walk through an example to demonstrate its usage.

Key Concepts
To understand the solution, we need to familiarize ourselves with the key concepts involved:

Customers Table: This table contains information about customers, including their unique ID and name.
Orders Table: This table contains information about orders, including the unique ID of the order and the ID of the customer who placed the order.
Primary Key: A primary key is a column with unique values that uniquely identifies each row in a table.
Foreign Key: A foreign key is a reference column that refers to the primary key of another table.
Code Structure
The code provided is a Python function named find_customers that takes two parameters: customers and orders. Both parameters are Pandas DataFrames representing the Customers and Orders tables, respectively. The function returns a Pandas DataFrame containing the names of customers who never placed an order.

Explanation: In this example, we have four customers: Joe, Henry, Sam, and Max. The Orders table shows that Sam (customer ID 3) and Joe (customer ID 1) have placed orders. We need to find the customers who never placed an order.

The code uses the isin function to check if the customer ID exists in the Orders table. The ~ operator negates the result, giving us the customers who never placed an order. The code then selects the 'name' column from the resulting DataFrame and renames it to 'Customers' for clarity.

The output DataFrame contains the names of customers who never placed an order: Henry and Max.

Conclusion
In this article, we discussed a solution to find all customers who never order anything. We explained the code provided, walked through an example, and demonstrated its usage. By using the provided Python function and the Customers and Orders tables, you can easily find the customers who never placed an order.