## IN Operator

Used to match multiple values in a column (cleaner than multiple OR conditions).

## BETWEEN Operator

Used to filter values within a range (inclusive of both ends).
*** 

# DATABASE 
| id | username | country | login_time | failed_attempts |
| -- | -------- | ------- | ---------- | --------------- |
| 1  | arun     | India   | 10         | 1               |
| 2  | john     | USA     | 22         | 4               |
| 3  | meena    | India   | 14         | 0               |
| 4  | alex     | UK      | 2          | 6               |
| 5  | ravi     | India   | 18         | 2               |
| 6  | sara     | Canada  | 9          | 3               |

# EXCERCISES

## 1. Find users from India, USA, or UK using IN
QUERY: SELECT username, country FROM login_logs
WHERE country IN ('India', 'USA', 'UK');

#### Output:
| username | country |
| -------- | ------- |
| arun     | India   |
| john     | USA     |
| meena    | India   |
| alex     | UK      |
| ravi     | India   |
***

## 2. Find users who are NOT from India or USA
QUERY: SELECT username, country FROM login_logs
WHERE country NOT IN ('India', 'USA');

#### Output:
| username | country |
| -------- | ------- |
| alex     | UK      |
| sara     | Canada  |
***

## 3. Find users who logged in between 10 and 20 hours
QUERY: SELECT username, login_time FROM login_logs
WHERE login_time BETWEEN 10 AND 20;

#### Output:
| username | login_time |
| -------- | ---------- |
| arun     | 10         |
| meena    | 14         |
| ravi     | 18         |
***
## 4. Find users with failed attempts between 2 and 5
QUERY: SELECT username, failed_attempts FROM login_logs
WHERE failed_attempts BETWEEN 2 AND 5;

#### Output:
| username | failed_attempts |
| -------- | --------------- |
| john     | 4               |
| ravi     | 2               |
| sara     | 3               |
***
## 5. Find users from India AND login time between 10 and 20
QUERY: SELECT username, country, login_time FROM login_logs
WHERE country = 'India' AND login_time BETWEEN 10 AND 20;

#### Output:
| username | country | login_time |
| -------- | ------- | ---------- |
| arun     | India   | 10         |
| meena    | India   | 14         |
| ravi     | India   | 18         |

