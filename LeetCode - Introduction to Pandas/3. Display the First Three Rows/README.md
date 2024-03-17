# LeetCode

#Problem

DataFrame: employees
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| employee_id | int    |
| name        | object |
| department  | object |
| salary      | int    |
+-------------+--------+
Write a solution to display the first 3 rows of this DataFrame.

 

Example 1:

Input:
DataFrame employees
+-------------+-----------+-----------------------+--------+
| employee_id | name      | department            | salary |
+-------------+-----------+-----------------------+--------+
| 3           | Bob       | Operations            | 48675  |
| 90          | Alice     | Sales                 | 11096  |
| 9           | Tatiana   | Engineering           | 33805  |
| 60          | Annabelle | InformationTechnology | 37678  |
| 49          | Jonathan  | HumanResources        | 23793  |
| 43          | Khaled    | Administration        | 40454  |
+-------------+-----------+-----------------------+--------+
Output:
+-------------+---------+-------------+--------+
| employee_id | name    | department  | salary |
+-------------+---------+-------------+--------+
| 3           | Bob     | Operations  | 48675  |
| 90          | Alice   | Sales       | 11096  |
| 9           | Tatiana | Engineering | 33805  |
+-------------+---------+-------------+--------+
Explanation: 
Only the first 3 rows are displayed.


#Expalnation

Explaining the Function to Select First Rows of a DataFrame
Introduction
In this explanation, we will delve into a Python function that selects the first few rows of a DataFrame using the Pandas library.

Key Concepts
The key concept here is to understand how to extract the initial rows of a DataFrame in Python using the Pandas library. The function selectFirstRows takes a DataFrame as input and returns the first three rows of that DataFrame.

Code Structure
The provided Python function selectFirstRows utilizes the Pandas library to achieve the task. It defines a function that takes a Pandas DataFrame named employees as input and returns the first three rows of that DataFrame using the head() method.

Conclusion
Understanding how to extract the initial rows of a DataFrame is crucial in data analysis and manipulation tasks. By using the head() method in Pandas, we can easily retrieve the first few rows of a DataFrame, allowing us to preview the data or perform further operations on a subset of the data.