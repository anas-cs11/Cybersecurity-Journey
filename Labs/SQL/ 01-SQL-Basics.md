# SQL (Structured Query Language) is used to interact with databases—retrieving, modifying, and analyzing data efficiently.

## In cybersecurity, SQL is critical for:

Investigating logs and detecting suspicious activity

Querying large datasets during incident response

Understanding and preventing attacks like SQL injection

Managing access control and sensitive data securely

# COMMANDS 
## SELECT Command

Used to choose which columns (data) you want to see from a table.

## FROM Command

Used to specify which table you are getting the data from.

## WHERE Command

Used to filter data based on conditions (like finding specific rows).

***

# DATABASE



| id | name  | role    | country | login_attempts |
| -- | ----- | ------- | ------- | -------------- |
| 1  | Arun  | admin   | India   | 2              |
| 2  | John  | user    | USA     | 5              |
| 3  | Meena | analyst | India   | 1              |
| 4  | Alex  | user    | UK      | 7              |
| 5  | Ravi  | admin   | India   | 3              |

***


## EXCERCISES
### Q1: Get all 'users' names
ANS: SELECT name FROM users;
## OUTPUT
| name  |
| ----- |
| Arun  |
| John  |
| Meena |
| Alex  |
| Ravi  |
***


### Q2: Get all data from users table
ANS: SELECT * FROM users;
## OUTPUT

| id | name  | role    | country | login_attempts |
| -- | ----- | ------- | ------- | -------------- |
| 1  | Arun  | admin   | India   | 2              |
| 2  | John  | user    | USA     | 5              |
| 3  | Meena | analyst | India   | 1              |
| 4  | Alex  | user    | UK      | 7              |
| 5  | Ravi  | admin   | India   | 3              |
***


### Q3: Get users from India
ANS: SELECT name, country FROM users
WHERE country = 'India';
## OUTPUT
| name  | country |
| ----- | ------- |
| Arun  | India   |
| Meena | India   |
| Ravi  | India   |
***

### Q4: Find users with more than 3 login attempts
ANS: SELECT name FROM users;
## OUTPUT
| name | login_attempts |
| ---- | -------------- |
| John | 5              |
| Alex | 7              |
***

### Q5:Find admin users in India
ANS: SELECT name, role FROM users
WHERE role = 'admin' AND country = 'India';
## OUTPUT
| name | role  |
| ---- | ----- |
| Arun | admin |
| Ravi | admin |



***




