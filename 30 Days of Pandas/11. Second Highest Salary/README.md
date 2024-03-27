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
 

Write a solution to find the second highest salary from the Employee table. If there is no second highest salary, return null (return None in Pandas).

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
Output: 
+---------------------+
| SecondHighestSalary |
+---------------------+
| 200                 |
+---------------------+
Example 2:

Input: 
Employee table:
+----+--------+
| id | salary |
+----+--------+
| 1  | 100    |
+----+--------+
Output: 
+---------------------+
| SecondHighestSalary |
+---------------------+
| null                |
+---------------------+


Finding the Second Highest Salary in the Employee Table
Introduction
In this article, we will discuss how to find the second highest salary from the Employee table using Python. We will provide a solution that utilizes the pandas library to perform the required operations.

Key Concepts
Before we dive into the code, let's understand the key concepts involved in finding the second highest salary:

Employee Table: The Employee table is a database table that contains information about employees, including their unique ID and salary.

Primary Key: The primary key is a column in the table that contains unique values for each row. In our case, the 'id' column serves as the primary key.

Salary: The salary column in the Employee table represents the salary of each employee.

Code Structure
The code provided consists of a function called second_highest_salary, which takes an input parameter employee of type pandas DataFrame. The function returns a pandas DataFrame containing the second highest salary.

Code Examples
Let's take a closer look at the code and understand how it works:

language-python
 Copy code
import pandas as pd

def second_highest_salary(employee: pd.DataFrame) -> pd.DataFrame:
    employee['rank'] = employee['salary'].rank(method='dense', ascending=False)
    nthhighest = employee[employee['rank'] == 2]
    colu_name = 'SecondHighestSalary'
    return pd.DataFrame({colu_name: [nthhighest['salary'].iloc[0] if len(nthhighest) > 0 else None]})
First, we import the pandas library, which provides powerful data manipulation and analysis capabilities.

The second_highest_salary function takes the employee DataFrame as input.

Inside the function, we add a new column called 'rank' to the DataFrame. This column is calculated using the rank method of pandas, which assigns a rank to each salary in descending order.

Next, we filter the DataFrame to select the rows where the rank is equal to 2. This gives us the employee(s) with the second highest salary.

We create a variable colu_name to store the column name for the output DataFrame.

Finally, we return a new DataFrame containing the second highest salary. If there are no employees with the second highest salary, we return None.

Conclusion
In this article, we discussed how to find the second highest salary from the Employee table using Python. We provided a solution that utilizes the pandas library to perform the required operations. By understanding the key concepts and using the provided code, you can easily find the second highest salary in any Employee table.