# LeetCode

# Problem

DataFrame employees
+-------------+--------+
| Column Name | Type.  |
+-------------+--------+
| name        | object |
| salary      | int.   |
+-------------+--------+
A company plans to provide its employees with a bonus.

Write a solution to create a new column name bonus that contains the doubled values of the salary column.

The result format is in the following example.

 

Example 1:

Input:
DataFrame employees
+---------+--------+
| name    | salary |
+---------+--------+
| Piper   | 4548   |
| Grace   | 28150  |
| Georgia | 1103   |
| Willow  | 6593   |
| Finn    | 74576  |
| Thomas  | 24433  |
+---------+--------+
Output:
+---------+--------+--------+
| name    | salary | bonus  |
+---------+--------+--------+
| Piper   | 4548   | 9096   |
| Grace   | 28150  | 56300  |
| Georgia | 1103   | 2206   |
| Willow  | 6593   | 13186  |
| Finn    | 74576  | 149152 |
| Thomas  | 24433  | 48866  |
+---------+--------+--------+
Explanation: 
A new column bonus is created by doubling the value in the column salary.


#Explanation

Explaining the Creation of a Bonus Column in a Pandas DataFrame
Introduction
In this explanation, we will delve into a Python function that creates a bonus column in a Pandas DataFrame. The function takes a DataFrame containing employee information, multiplies each employee's salary by 2, and adds a new column named 'bonus' to the DataFrame.

Key Concepts
Pandas DataFrame: Pandas is a popular data manipulation library in Python. DataFrames are two-dimensional, size-mutable, and heterogeneous data structures.
Function Definition: The createBonusColumn function takes a Pandas DataFrame as input and returns the same DataFrame with an additional 'bonus' column.
Column Manipulation: The function manipulates the DataFrame by creating a new column based on an existing column's values.
Code Structure
The provided Python function consists of:

Function Name: createBonusColumn
Input Parameter: employees (Pandas DataFrame)
Output: Updated Pandas DataFrame with a 'bonus' column

Conclusion
The createBonusColumn function efficiently adds a 'bonus' column to a Pandas DataFrame by doubling each employee's salary. Understanding how to manipulate DataFrame columns is crucial for data processing and analysis tasks in Python. By utilizing functions like this, you can enhance the functionality and structure of your data for further analysis or visualization.


