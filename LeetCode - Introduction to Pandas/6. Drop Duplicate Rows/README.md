# LeetCode

# Problem

DataFrame customers
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| customer_id | int    |
| name        | object |
| email       | object |
+-------------+--------+
There are some duplicate rows in the DataFrame based on the email column.

Write a solution to remove these duplicate rows and keep only the first occurrence.

The result format is in the following example.

 

Example 1:
Input:
+-------------+---------+---------------------+
| customer_id | name    | email               |
+-------------+---------+---------------------+
| 1           | Ella    | emily@example.com   |
| 2           | David   | michael@example.com |
| 3           | Zachary | sarah@example.com   |
| 4           | Alice   | john@example.com    |
| 5           | Finn    | john@example.com    |
| 6           | Violet  | alice@example.com   |
+-------------+---------+---------------------+
Output:  
+-------------+---------+---------------------+
| customer_id | name    | email               |
+-------------+---------+---------------------+
| 1           | Ella    | emily@example.com   |
| 2           | David   | michael@example.com |
| 3           | Zachary | sarah@example.com   |
| 4           | Alice   | john@example.com    |
| 6           | Violet  | alice@example.com   |
+-------------+---------+---------------------+
Explanation:
Alic (customer_id = 4) and Finn (customer_id = 5) both use john@example.com, so only the first occurrence of this email is retained.


#Explanation:

Explaining the Function to Drop Duplicate Emails
Introduction
In this explanation, we will delve into a Python function that aims to drop duplicate email entries from a Pandas DataFrame. The function is designed to ensure data integrity by removing redundant email records.

Key Concepts
Pandas DataFrame: The function operates on a Pandas DataFrame, a two-dimensional, size-mutable, potentially heterogeneous tabular data structure with labeled axes.
drop_duplicates() Method: This method in Pandas is used to remove duplicate rows from a DataFrame based on a subset of columns.
keep Parameter: The 'keep' parameter specifies which duplicate entries to keep. In this case, 'first' indicates keeping the first occurrence and removing subsequent duplicates.

Conclusion
The dropDuplicateEmails function efficiently removes duplicate email entries from a Pandas DataFrame, ensuring data cleanliness and consistency. By utilizing the drop_duplicates method with the 'keep' parameter set to 'first', the function retains the first occurrence of each unique email while eliminating subsequent duplicates. This process aids in data deduplication and maintenance of accurate records within the DataFrame.
