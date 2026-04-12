## AND Operator

Used to combine multiple conditions, and all conditions must be TRUE.

## OR Operator

Used to combine conditions where at least one condition must be TRUE.

## NOT Operator

Used to exclude a condition (reverse the result).

***
# DATABASE
| id | name  | role    | country | login_attempts |
| -- | ----- | ------- | ------- | -------------- |
| 1  | Arun  | admin   | India   | 2              |
| 2  | John  | user    | USA     | 5              |
| 3  | Meena | analyst | India   | 1              |
| 4  | Alex  | user    | UK      | 7              |
| 5  | Ravi  | admin   | India   | 3              |


___
## EXCERCISES
### 1. Find users who are admins AND from India
ANS: SELECT name, role, country FROM users
WHERE role = 'admin' AND country = 'India';

| name | role  | country |
| ---- | ----- | ------- |
| Arun | admin | India   |
| Ravi | admin | India   |

***

## 2. Find users who are from India OR USA
ANS: SELECT name, country FROM users
WHERE country = 'India' OR country = 'USA';
| name  | country |
| ----- | ------- |
| Arun  | India   |
| John  | USA     |
| Meena | India   |
| Ravi  | India   |
***
## 3. Find users who are NOT from India
ANS: SELECT name, country FROM users
WHERE NOT country = 'India';
| name | country |
| ---- | ------- |
| John | USA     |
| Alex | UK      |

***
## 4. Find users who are NOT admins
ANS: SELECT name, role FROM users
WHERE NOT role = 'admin';
| name  | role    |
| ----- | ------- |
| John  | user    |
| Meena | analyst |
| Alex  | user    |
***
## 5. Find users who are from India AND have login_attempts < 3
ANS: SELECT name, login_attempts FROM users
WHERE country = 'India' AND login_attempts < 3;
| name  | login_attempts |
| ----- | -------------- |
| Arun  | 2              |
| Meena | 1              |


