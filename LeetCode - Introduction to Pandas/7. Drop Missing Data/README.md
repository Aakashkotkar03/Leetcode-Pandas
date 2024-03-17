# LeetCode

# Problem
DataFrame students
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| student_id  | int    |
| name        | object |
| age         | int    |
+-------------+--------+
There are some rows having missing values in the name column.

Write a solution to remove the rows with missing values.

The result format is in the following example.

 

Example 1:

Input:
+------------+---------+-----+
| student_id | name    | age |
+------------+---------+-----+
| 32         | Piper   | 5   |
| 217        | None    | 19  |
| 779        | Georgia | 20  |
| 849        | Willow  | 14  |
+------------+---------+-----+
Output:
+------------+---------+-----+
| student_id | name    | age |
+------------+---------+-----+
| 32         | Piper   | 5   |
| 779        | Georgia | 20  | 
| 849        | Willow  | 14  | 
+------------+---------+-----+
Explanation: 
Student with id 217 havs empty value in the name column, so it will be removed.


Explanation:-
import pandas as pd: This line imports the pandas library, typically aliased as pd, allowing access to Pandas functions and data structures.

def dropMissingData(students: pd.DataFrame) -> pd.DataFrame:: This line defines a function named dropMissingData. It takes one argument, students, which is expected to be a DataFrame. The annotation -> pd.DataFrame indicates that the function will return a DataFrame.

students = students.dropna(subset=['name']): This line performs the core operation of the function. It uses the dropna() method to remove rows with missing values (NaN) specifically in the 'name' column. The subset=['name'] parameter specifies that only the 'name' column should be considered for dropping rows with missing values. The result of this operation is assigned back to the students variable.

return students: This line returns the modified DataFrame students, which now contains only the rows where the 'name' column does not have missing values.