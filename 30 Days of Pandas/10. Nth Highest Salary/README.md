# LeetCode

# Problem
Table: Employee

+-------------+------+
| Column Name | Type |
+-------------+------+
| id          | int  |
| salary      | int  |
+-------------+------+
id is the primary key (column with unique values) for this table.
Each row of this table contains information about the salary of an employee.
 

Write a solution to find the nth highest salary from the Employee table. If there is no nth highest salary, return null.

The result format is in the following example.

 

Example 1:

Input: 
Employee table:
+----+--------+
| id | salary |
+----+--------+
| 1  | 100    |
| 2  | 200    |
| 3  | 300    |
+----+--------+
n = 2
Output: 
+------------------------+
| getNthHighestSalary(2) |
+------------------------+
| 200                    |
+------------------------+
Example 2:

Input: 
Employee table:
+----+--------+
| id | salary |
+----+--------+
| 1  | 100    |
+----+--------+
n = 2
Output: 
+------------------------+
| getNthHighestSalary(2) |
+------------------------+
| null                   |
+------------------------+

Finding the nth Highest Salary from the Employee Table
Introduction
In this article, we will discuss how to find the nth highest salary from the Employee table using Python. We will provide a solution that returns the nth highest salary from the table and handles cases where there is no nth highest salary.

Key Concepts
To find the nth highest salary from the Employee table, we will use the pandas library in Python. We will add a rank column to the table based on the salary column and then filter the table to get the row with the desired rank. Finally, we will return the nth highest salary or null if it doesn't exist.

Code Structure
The code provided consists of a function called nth_highest_salary that takes two parameters: employee (a pandas DataFrame representing the Employee table) and N (an integer representing the desired rank). The function returns a pandas DataFrame with a single column named getNthHighestSalary(N).

Code Examples
Let's take a look at the code example provided and understand how it works.

language-python
 Copy code
import pandas as pd

def nth_highest_salary(employee: pd.DataFrame, N: int) -> pd.DataFrame:
    employee['rank'] = employee['salary'].rank(method='dense', ascending=False)
    nthhighest = employee[employee['rank'] == N]
    colu_name = f'getNthHighestSalary({N})'
    return pd.DataFrame({colu_name: [nthhighest['salary'].iloc[0] if len(nthhighest) > 0 else None]})
The nth_highest_salary function takes the employee DataFrame and N as input parameters. It adds a new column called 'rank' to the DataFrame using the rank method from pandas. The rank method assigns a rank to each salary in descending order. The method='dense' parameter ensures that the ranks are assigned without any gaps.

Next, the function filters the DataFrame to get the rows where the rank is equal to the desired rank N. It assigns the filtered DataFrame to the variable nthhighest.

The function then creates a column name getNthHighestSalary(N) using string formatting and returns a new DataFrame with this column. The value in the column is the nth highest salary if nthhighest is not empty, otherwise it is set to None.

Conclusion
Finding the nth highest salary from the Employee table can be easily achieved using the pandas library in Python. By adding a rank column to the table and filtering based on the desired rank, we can obtain the nth highest salary. The provided code and solution demonstrate how to accomplish this task efficiently.

