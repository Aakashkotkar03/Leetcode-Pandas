# LeetCode

# Problem
DataFrame weather
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| city        | object |
| month       | object |
| temperature | int    |
+-------------+--------+
Write a solution to pivot the data so that each row represents temperatures for a specific month, and each city is a separate column.

The result format is in the following example.

 

Example 1:
Input:
+--------------+----------+-------------+
| city         | month    | temperature |
+--------------+----------+-------------+
| Jacksonville | January  | 13          |
| Jacksonville | February | 23          |
| Jacksonville | March    | 38          |
| Jacksonville | April    | 5           |
| Jacksonville | May      | 34          |
| ElPaso       | January  | 20          |
| ElPaso       | February | 6           |
| ElPaso       | March    | 26          |
| ElPaso       | April    | 2           |
| ElPaso       | May      | 43          |
+--------------+----------+-------------+
Output:
+----------+--------+--------------+
| month    | ElPaso | Jacksonville |
+----------+--------+--------------+
| April    | 2      | 5            |
| February | 6      | 23           |
| January  | 20     | 13           |
| March    | 26     | 38           |
| May      | 43     | 34           |
+----------+--------+--------------+
Explanation:
The table is pivoted, each column represents a city, and each row represents a specific month.


Explanation:- 
Explaining Pivot Table Creation in Pandas
Introduction
In this explanation, we will delve into a Python function that creates a pivot table using the Pandas library. Pivot tables are powerful tools for reshaping and summarizing data, especially when dealing with large datasets.

Key Concepts
The key concept here is the creation of a pivot table using the pivot function provided by Pandas. This function allows us to reorganize data from a DataFrame into a new table structure based on specified columns.

Code Structure
The provided Python function pivotTable takes a Pandas DataFrame weather as input and returns a new DataFrame with a pivot table structure. The function uses the pivot method to pivot the data based on the 'month', 'city', and 'temperature' columns.

Conclusion
Understanding how to create pivot tables using Pandas is essential for data manipulation and analysis tasks. By utilizing the pivot function, we can efficiently transform data into a more structured format that facilitates analysis and visualization. This code snippet provides a concise example of how to create a pivot table in Python using Pandas, showcasing the simplicity and power of the library for data processing tasks.