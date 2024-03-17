# LeetCode

#Problem
DataFrame students
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| student_id  | int    |
| name        | object |
| age         | int    |
+-------------+--------+

Write a solution to select the name and age of the student with student_id = 101.

The result format is in the following example.

 

Example 1:
Input:
+------------+---------+-----+
| student_id | name    | age |
+------------+---------+-----+
| 101        | Ulysses | 13  |
| 53         | William | 10  |
| 128        | Henry   | 6   |
| 3          | Henry   | 11  |
+------------+---------+-----+
Output:
+---------+-----+
| name    | age | 
+---------+-----+
| Ulysses | 13  |
+---------+-----+
Explanation:
Student Ulysses has student_id = 101, we select the name and age.


#Explanation:

Explaining Data Selection Function in Python
Introduction
In this explanation, we will delve into a Python function that selects specific data from a Pandas DataFrame based on a condition. The function aims to filter out rows where the 'student_id' is equal to 101 and returns only the 'name' and 'age' columns for those rows.

Key Concepts
Pandas DataFrame: Pandas is a popular library in Python used for data manipulation and analysis. DataFrames are two-dimensional, size-mutable, and heterogeneous tabular data structures with labeled axes.

Function Definition: The provided function, selectData, takes a Pandas DataFrame named students as input and returns a new DataFrame containing only the 'name' and 'age' columns for rows where the 'student_id' is 101.

Code Structure
The function selectData consists of the following components:

Input: students (Pandas DataFrame) - The original DataFrame containing student data.
Output: Returns a new DataFrame df with columns 'name' and 'age' for rows where 'student_id' is 101.


Conclusion
The selectData function efficiently filters the student data based on the 'student_id' column, extracting only the 'name' and 'age' information for students with an ID of 101. Understanding such data selection operations is crucial for data analysis and manipulation tasks in Python using Pandas.