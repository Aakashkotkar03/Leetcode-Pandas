# LeetCode

# Problem
Table: Employees

+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| employee_id | int     |
| name        | varchar |
| salary      | int     |
+-------------+---------+
employee_id is the primary key (column with unique values) for this table.
Each row of this table indicates the employee ID, employee name, and salary.
 

Write a solution to calculate the bonus of each employee. The bonus of an employee is 100% of their salary if the ID of the employee is an odd number and the employee's name does not start with the character 'M'. The bonus of an employee is 0 otherwise.

Return the result table ordered by employee_id.

The result format is in the following example.

 

Example 1:

Input: 
Employees table:
+-------------+---------+--------+
| employee_id | name    | salary |
+-------------+---------+--------+
| 2           | Meir    | 3000   |
| 3           | Michael | 3800   |
| 7           | Addilyn | 7400   |
| 8           | Juan    | 6100   |
| 9           | Kannon  | 7700   |
+-------------+---------+--------+
Output: 
+-------------+-------+
| employee_id | bonus |
+-------------+-------+
| 2           | 0     |
| 3           | 0     |
| 7           | 7400  |
| 8           | 0     |
| 9           | 7700  |
+-------------+-------+
Explanation: 
The employees with IDs 2 and 8 get 0 bonus because they have an even employee_id.
The employee with ID 3 gets 0 bonus because their name starts with 'M'.
The rest of the employees get a 100% bonus.

Solution: Calculating Employee Bonuses
Introduction
In this article, we will discuss a solution to calculate the bonus of each employee based on certain conditions. The bonus amount will be determined by the employee's salary and their employee ID and name.

Key Concepts
To calculate the bonus, we will consider the following key concepts:

Employee ID: A unique identifier for each employee.
Employee Name: The name of the employee.
Salary: The salary of the employee.
Bonus: The bonus amount to be calculated based on specific conditions.
Code Structure
The code provided is written in Python and uses the pandas library to perform data manipulation and calculations. The code defines a function called calculate_special_bonus that takes a pandas DataFrame named employees as input and returns another DataFrame with the calculated bonuses.

The calculate_special_bonus function takes the employees DataFrame as input. It first uses the loc function to filter the rows of the DataFrame based on two conditions:

The employee ID is an odd number (employees['employee_id'] % 2 == 1).
The employee's name does not start with the character 'M' (employees['name'].str[0] != 'M').
For the filtered rows, the function assigns the employee's salary to the 'bonus' column. This means that if an employee meets the specified conditions, they will receive a bonus equal to their salary.

Next, the function selects only the 'employee_id' and 'bonus' columns from the DataFrame and sorts the result by the 'employee_id' column in ascending order.

Finally, the function fills any missing values in the 'bonus' column with 0 using the fillna function. This ensures that employees who do not meet the bonus conditions have a bonus value of 0.

The function returns the resulting DataFrame with the calculated bonuses.

Conclusion
In this article, we discussed a solution to calculate the bonus of each employee based on specific conditions. The provided code uses the pandas library in Python to perform the necessary calculations and manipulations on the employee data. By understanding the code structure and the key concepts involved, you can easily adapt this solution to calculate bonuses for your own employee dataset.