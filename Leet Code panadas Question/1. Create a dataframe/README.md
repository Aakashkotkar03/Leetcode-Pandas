#Create a DataFrame from List

#Problem 

Write a solution to create a DataFrame from a 2D list called student_data. This 2D list contains the IDs and ages of some students.

The DataFrame should have two columns, student_id and age, and be in the same order as the original 2D list.

The result format is in the following example. 

Example 1:

Input:
student_data:
[
  [1, 15],
  [2, 11],
  [3, 11],
  [4, 20]
]
Output:
+------------+-----+
| student_id | age |
+------------+-----+
| 1          | 15  |
| 2          | 11  |
| 3          | 11  |
| 4          | 20  |
+------------+-----+

A DataFrame was created on top of student_data, with two columns named student_id and age.


#Explnation

Explaining DataFrame Creation Function in Python
Introduction
In this explanation, we will delve into a Python function that creates a Pandas DataFrame from a list of student data. The function takes a list of lists containing student information and converts it into a structured DataFrame using the Pandas library.

Key Concepts
Pandas DataFrame: Pandas is a powerful data manipulation library in Python. DataFrames are two-dimensional, size-mutable, and heterogeneous tabular data structures with labeled axes (rows and columns).
Function Parameters: The function createDataframe takes a parameter student_data, which is a list of lists containing student information.
Return Type: The function returns a Pandas DataFrame with columns labeled as 'student_id' and 'age'.
Code Structure
The provided Python function createDataframe uses the Pandas library to create a DataFrame from the input student_data. The function definition specifies that student_data is a list of lists containing integer values representing student IDs and ages. The function returns a Pandas DataFrame with columns 'student_id' and 'age'.

Conclusion
Understanding how to create a Pandas DataFrame from a list of lists in Python is essential for data manipulation and analysis tasks. By utilizing functions like createDataframe, you can efficiently convert raw data into a structured format suitable for further analysis and visualization. This function simplifies the process of creating DataFrames, making data handling more manageable and structured.
