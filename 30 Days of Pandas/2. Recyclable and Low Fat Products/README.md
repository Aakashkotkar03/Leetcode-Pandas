# LeetCode

# Problem
Table: Products

+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| product_id  | int     |
| low_fats    | enum    |
| recyclable  | enum    |
+-------------+---------+
product_id is the primary key (column with unique values) for this table.
low_fats is an ENUM (category) of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.
recyclable is an ENUM (category) of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.
 

Write a solution to find the ids of products that are both low fat and recyclable.

Return the result table in any order.

The result format is in the following example.

 

Example 1:

Input: 
Products table:
+-------------+----------+------------+
| product_id  | low_fats | recyclable |
+-------------+----------+------------+
| 0           | Y        | N          |
| 1           | Y        | Y          |
| 2           | N        | Y          |
| 3           | Y        | Y          |
| 4           | N        | N          |
+-------------+----------+------------+
Output: 
+-------------+
| product_id  |
+-------------+
| 1           |
| 3           |
+-------------+
Explanation: Only products 1 and 3 are both low fat and recyclable.


Finding Low Fat and Recyclable Products
Introduction
In this article, we will discuss how to find the IDs of products that are both low fat and recyclable. We will provide a solution using Python and the pandas library to filter the products based on their low fat and recyclable attributes.

Key Concepts
Before we dive into the code, let's understand the key concepts related to the problem:

Products Table: The table contains information about various products, including their IDs, low fat status, and recyclable status.
Low Fat: The low fat attribute of a product indicates whether the product is low fat or not. It is represented by the values 'Y' (low fat) and 'N' (not low fat).
Recyclable: The recyclable attribute of a product indicates whether the product is recyclable or not. It is represented by the values 'Y' (recyclable) and 'N' (not recyclable).
Code Structure
The code provided is a Python function named find_products that takes a pandas DataFrame named products as input and returns a filtered DataFrame containing the IDs of products that are both low fat and recyclable.

Conclusion
In this article, we discussed how to find the IDs of products that are both low fat and recyclable. We provided a Python solution using the pandas library to filter the products based on their low fat and recyclable attributes. By using the find_products function, you can easily retrieve the desired information from a products DataFrame.