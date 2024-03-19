# LeetCode

# Problem
Table: Users

+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| user_id       | int     |
| name          | varchar |
| mail          | varchar |
+---------------+---------+
user_id is the primary key (column with unique values) for this table.
This table contains information of the users signed up in a website. Some e-mails are invalid.
 

Write a solution to find the users who have valid emails.

A valid e-mail has a prefix name and a domain where:

The prefix name is a string that may contain letters (upper or lower case), digits, underscore '_', period '.', and/or dash '-'. The prefix name must start with a letter.
The domain is '@leetcode.com'.
Return the result table in any order.

The result format is in the following example.

 

Example 1:

Input: 
Users table:
+---------+-----------+-------------------------+
| user_id | name      | mail                    |
+---------+-----------+-------------------------+
| 1       | Winston   | winston@leetcode.com    |
| 2       | Jonathan  | jonathanisgreat         |
| 3       | Annabelle | bella-@leetcode.com     |
| 4       | Sally     | sally.come@leetcode.com |
| 5       | Marwan    | quarz#2020@leetcode.com |
| 6       | David     | david69@gmail.com       |
| 7       | Shapiro   | .shapo@leetcode.com     |
+---------+-----------+-------------------------+
Output: 
+---------+-----------+-------------------------+
| user_id | name      | mail                    |
+---------+-----------+-------------------------+
| 1       | Winston   | winston@leetcode.com    |
| 3       | Annabelle | bella-@leetcode.com     |
| 4       | Sally     | sally.come@leetcode.com |
+---------+-----------+-------------------------+
Explanation: 
The mail of user 2 does not have a domain.
The mail of user 5 has the # sign which is not allowed.
The mail of user 6 does not have the leetcode domain.
The mail of user 7 starts with a period.

Finding Users with Valid Emails
Introduction
In this article, we will discuss how to find users with valid emails using Python. We will provide a solution to filter out users whose emails do not meet the specified criteria.

Key Concepts
To determine if an email is valid, we need to check two things:

The prefix name: It should start with a letter and can contain letters (upper or lower case), digits, underscore '_', period '.', and/or dash '-'.
The domain: It should be '@leetcode.com'.
Code Structure
The code provided is a Python function called valid_emails. It takes a pandas DataFrame called users as input and returns a filtered DataFrame containing only the users with valid emails.

Let's break down the code and understand how it works:

We import the pandas library, which provides powerful data manipulation and analysis tools.
We define a function called valid_emails that takes a pandas DataFrame called users as input and returns a filtered DataFrame.
Inside the function, we use the str.match method of the 'mail' column in the users DataFrame to check if each email matches the specified pattern.
The regular expression pattern ^[A-Za-z][A-Za-z0-9_\.\-]*@leetcode[.]com$ is used to match the email format. Let's break it down:
^ and $ are anchors that match the start and end of the string, respectively.
[A-Za-z] matches a single letter (upper or lower case) at the beginning of the string.
[A-Za-z0-9_\.\-]* matches zero or more occurrences of letters, digits, underscore '_', period '.', or dash '-'.
@leetcode[.]com matches the domain '@leetcode.com'.

Conclusion
In this article, we discussed how to find users with valid emails using Python. We provided a solution that filters out users whose emails do not meet the specified criteria. By using the valid_emails function, we can easily find the users with valid emails in a given DataFrame.