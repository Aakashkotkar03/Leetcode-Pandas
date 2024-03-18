# LeetCode

# Problem
Table: Views

+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| article_id    | int     |
| author_id     | int     |
| viewer_id     | int     |
| view_date     | date    |
+---------------+---------+
There is no primary key (column with unique values) for this table, the table may have duplicate rows.
Each row of this table indicates that some viewer viewed an article (written by some author) on some date. 
Note that equal author_id and viewer_id indicate the same person.
 

Write a solution to find all the authors that viewed at least one of their own articles.

Return the result table sorted by id in ascending order.

The result format is in the following example.

 

Example 1:

Input: 
Views table:
+------------+-----------+-----------+------------+
| article_id | author_id | viewer_id | view_date  |
+------------+-----------+-----------+------------+
| 1          | 3         | 5         | 2019-08-01 |
| 1          | 3         | 6         | 2019-08-02 |
| 2          | 7         | 7         | 2019-08-01 |
| 2          | 7         | 6         | 2019-08-02 |
| 4          | 7         | 1         | 2019-07-22 |
| 3          | 4         | 4         | 2019-07-21 |
| 3          | 4         | 4         | 2019-07-21 |
+------------+-----------+-----------+------------+
Output: 
+------+
| id   |
+------+
| 4    |
| 7    |
+------+


Finding Authors Who Viewed Their Own Articles
Introduction
In this task, we need to find all the authors who have viewed at least one of their own articles. We are given a table called "Views" which contains information about the articles viewed by different viewers. Each row in the table represents a viewer viewing an article written by an author on a specific date. The table has columns for article_id, author_id, viewer_id, and view_date.

Key Concepts
To solve this task, we need to filter the rows in the "Views" table where the author_id is equal to the viewer_id, indicating that the author has viewed their own article. We also need to remove any duplicate rows and sort the result by the author_id in ascending order.

Code Structure
The code provided is a Python function called "article_views" that takes a pandas DataFrame named "views" as input and returns another pandas DataFrame as output. The function performs the following steps:

Filter the rows in the "views" DataFrame where the author_id is equal to the viewer_id.
Select only the "viewer_id" column from the filtered DataFrame.
Remove any duplicate rows from the selected column.
Sort the resulting DataFrame by the "viewer_id" column in ascending order.
Rename the "viewer_id" column to "id" in the resulting DataFrame.
Return the resulting DataFrame.

Conclusion
In this task, we learned how to find the authors who have viewed at least one of their own articles. We used the provided "Views" table and filtered the rows where the author_id is equal to the viewer_id. We removed any duplicate rows and sorted the result by the author_id in ascending order. The code provided is a Python function that implements this logic using the pandas library.