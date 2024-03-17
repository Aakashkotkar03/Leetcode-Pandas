# LeetCode

# Problem
DataFrame df1
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| student_id  | int    |
| name        | object |
| age         | int    |
+-------------+--------+

DataFrame df2
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| student_id  | int    |
| name        | object |
| age         | int    |
+-------------+--------+

Write a solution to concatenate these two DataFrames vertically into one DataFrame.

The result format is in the following example.

 

Example 1:

Input:
df1
+------------+---------+-----+
| student_id | name    | age |
+------------+---------+-----+
| 1          | Mason   | 8   |
| 2          | Ava     | 6   |
| 3          | Taylor  | 15  |
| 4          | Georgia | 17  |
+------------+---------+-----+
df2
+------------+------+-----+
| student_id | name | age |
+------------+------+-----+
| 5          | Leo  | 7   |
| 6          | Alex | 7   |
+------------+------+-----+
Output:
+------------+---------+-----+
| student_id | name    | age |
+------------+---------+-----+
| 1          | Mason   | 8   |
| 2          | Ava     | 6   |
| 3          | Taylor  | 15  |
| 4          | Georgia | 17  |
| 5          | Leo     | 7   |
| 6          | Alex    | 7   |
+------------+---------+-----+
Explanation:
The two DataFramess are stacked vertically, and their rows are combined.

import pandas as pd: This line imports the pandas library under the alias pd, which is a common convention.

def concatenateTables(df1: pd.DataFrame, df2: pd.DataFrame) -> pd.DataFrame:: This line defines a function named concatenateTables. It takes two parameters, df1 and df2, both expected to be DataFrames. The function annotation -> pd.DataFrame specifies that the function will return a DataFrame.

df = pd.concat([df1, df2]): This line uses the pd.concat() function to concatenate the two input DataFrames, df1 and df2, along their rows. By default, pd.concat() concatenates along axis 0, which corresponds to rows. The result is stored in the variable df.

return df: This line returns the concatenated DataFrame df as the output of the function.