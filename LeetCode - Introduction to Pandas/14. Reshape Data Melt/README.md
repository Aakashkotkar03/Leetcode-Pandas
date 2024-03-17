# LeetCode

# Problem
DataFrame report
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| product     | object |
| quarter_1   | int    |
| quarter_2   | int    |
| quarter_3   | int    |
| quarter_4   | int    |
+-------------+--------+
Write a solution to reshape the data so that each row represents sales data for a product in a specific quarter.

The result format is in the following example.

 

Example 1:

Input:
+-------------+-----------+-----------+-----------+-----------+
| product     | quarter_1 | quarter_2 | quarter_3 | quarter_4 |
+-------------+-----------+-----------+-----------+-----------+
| Umbrella    | 417       | 224       | 379       | 611       |
| SleepingBag | 800       | 936       | 93        | 875       |
+-------------+-----------+-----------+-----------+-----------+
Output:
+-------------+-----------+-------+
| product     | quarter   | sales |
+-------------+-----------+-------+
| Umbrella    | quarter_1 | 417   |
| SleepingBag | quarter_1 | 800   |
| Umbrella    | quarter_2 | 224   |
| SleepingBag | quarter_2 | 936   |
| Umbrella    | quarter_3 | 379   |
| SleepingBag | quarter_3 | 93    |
| Umbrella    | quarter_4 | 611   |
| SleepingBag | quarter_4 | 875   |
+-------------+-----------+-------+
Explanation:
The DataFrame is reshaped from wide to long format. Each row represents the sales of a product in a quarter.


Explanation:-
Reshaping DataFrame to Long Format
Introduction
In data analysis and manipulation, it is often necessary to reshape data from a wide format to a long format or vice versa. Reshaping data allows for easier analysis and visualization, as well as compatibility with certain statistical models and algorithms. In this article, we will explore how to reshape a DataFrame in Python using the pandas library.

Key Concepts
Before we dive into the code examples, let's understand some key concepts related to reshaping data:

Wide Format: In the wide format, each row represents a unique observation, and each column represents a variable. This format is often used when data is collected over time or across different categories.

Long Format: In the long format, each row represents a unique combination of variables, and each column represents a specific variable. This format is often used when data needs to be aggregated or analyzed based on multiple variables.

Reshaping: Reshaping refers to the process of transforming data from one format to another. This can be done using various techniques, such as melting, pivoting, stacking, and unstacking.

Code Structure
To reshape a DataFrame from wide to long format, we can use the melt() function provided by the pandas library. The melt() function takes the following parameters:

report: The DataFrame to be reshaped.
id_vars: The column(s) to be used as identifier variables (columns that will remain unchanged).
value_vars: The column(s) to be melted (columns that will be transformed into rows).
var_name: The name of the variable column.
value_name: The name of the value column.
The melt() function returns a new DataFrame in the long format.

Conclusion
Reshaping a DataFrame from wide to long format is a common task in data analysis and manipulation. By using the melt() function provided by the pandas library, we can easily transform a DataFrame to better suit our analysis needs. Understanding the concepts of wide and long formats, as well as the various techniques for reshaping data, allows us to effectively manipulate and analyze data in Python.