# LeetCode

# Problem
DataFrame animals
+-------------+--------+
| Column Name | Type   |
+-------------+--------+
| name        | object |
| species     | object |
| age         | int    |
| weight      | int    |
+-------------+--------+
Write a solution to list the names of animals that weigh strictly more than 100 kilograms.

Return the animals sorted by weight in descending order.

The result format is in the following example.

 

Example 1:

Input: 
DataFrame animals:
+----------+---------+-----+--------+
| name     | species | age | weight |
+----------+---------+-----+--------+
| Tatiana  | Snake   | 98  | 464    |
| Khaled   | Giraffe | 50  | 41     |
| Alex     | Leopard | 6   | 328    |
| Jonathan | Monkey  | 45  | 463    |
| Stefan   | Bear    | 100 | 50     |
| Tommy    | Panda   | 26  | 349    |
+----------+---------+-----+--------+
Output: 
+----------+
| name     |
+----------+
| Tatiana  |
| Jonathan |
| Tommy    |
| Alex     |
+----------+
Explanation: 
All animals weighing more than 100 should be included in the results table.
Tatiana's weight is 464, Jonathan's weight is 463, Tommy's weight is 349, and Alex's weight is 328.
The results should be sorted in descending order of weight.

Explanation:-
Listing Names of Animals that Weigh More than 100 Kilograms
Introduction
In this article, we will discuss how to write a solution to list the names of animals that weigh strictly more than 100 kilograms. We will use a DataFrame called "animals" to store the information about the animals.

Key Concepts
To solve this problem, we need to perform the following steps:

Filter the animals based on their weight, selecting only those that weigh more than 100 kilograms.
Sort the filtered animals by weight in descending order.
Extract the names of the sorted animals.
Code Structure
The code provided is a Python function called findHeavyAnimals that takes a DataFrame called animals as input and returns a DataFrame containing the names of the animals that weigh more than 100 kilograms.

Explanation
Suppose we have the following DataFrame called animals:

name	species	age	weight
Tatiana	Snake	98	464
Khaled	Giraffe	50	41
Alex	Leopard	6	328
Jonathan	Monkey	45	463
Stefan	Bear	100	50
Tommy	Panda	26	349
We want to find the names of animals that weigh strictly more than 100 kilograms and sort them by weight in descending order.

The code animals.loc[animals['weight']>100] filters the animals based on their weight, selecting only those that weigh more than 100 kilograms. This gives us the following DataFrame:

name	species	age	weight
Tatiana	Snake	98	464
Alex	Leopard	6	328
Jonathan	Monkey	45	463
Tommy	Panda	26	349
Next, we use the sort_values function to sort the filtered animals by weight in descending order. The ascending=False parameter ensures that the sorting is done in descending order. This gives us the following DataFrame:

name	species	age	weight
Tatiana	Snake	98	464
Jonathan	Monkey	45	463
Tommy	Panda	26	349
Alex	Leopard	6	328
Finally, we use the [['name']] syntax to extract only the "name" column from the sorted DataFrame. This gives us the final result:

name
Tatiana
Jonathan
Tommy
Alex
Conclusion
In this article, we discussed how to write a solution to list the names of animals that weigh strictly more than 100 kilograms. We used a DataFrame to store the information about the animals and performed filtering, sorting, and column extraction operations to obtain the desired result. The code provided can be used as a starting point to solve similar problems involving data manipulation in Python.