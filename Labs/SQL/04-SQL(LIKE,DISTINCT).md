## LIKE Operator

Used to search for patterns in text (using wildcards):

% → any number of characters
_ → exactly one character

## DISTINCT Operator

Used to remove duplicate values and show only unique results.

# DATABASE


| id | name  | department | email                                       | country |
| -- | ----- | ---------- | ------------------------------------------- | ------- |
| 1  | Arun  | IT         | [arun@gmail.com](mailto:arun@gmail.com)     | India   |
| 2  | Anil  | HR         | [anil@yahoo.com](mailto:anil@yahoo.com)     | India   |
| 3  | Meena | IT         | [meena@gmail.com](mailto:meena@gmail.com)   | India   |
| 4  | Alex  | Finance    | [alex@outlook.com](mailto:alex@outlook.com) | UK      |
| 5  | John  | IT         | [john@gmail.com](mailto:john@gmail.com)     | USA     |
| 6  | Asha  | HR         | [asha@gmail.com](mailto:asha@gmail.com)     | India   |



# EXCERCISES

## 1. Find names starting with 'A'
QUERY: SELECT name FROM employees
WHERE name LIKE 'A%';

#### Output:
| name |
| ---- |
| Arun |
| Anil |
| Alex |
| Asha |

## 2. Find emails ending with 'gmail.com'
QUERY: SELECT name, email FROM employees
WHERE email LIKE '%gmail.com';

#### Output:
| name  | email                                     |
| ----- | ----------------------------------------- |
| Arun  | [arun@gmail.com](mailto:arun@gmail.com)   |
| Meena | [meena@gmail.com](mailto:meena@gmail.com) |
| John  | [john@gmail.com](mailto:john@gmail.com)   |
| Asha  | [asha@gmail.com](mailto:asha@gmail.com)   |



## 3. Find names with exactly 5 letters
QUERY: SELECT name FROM employees
WHERE name LIKE '_____';

#### Output:
| name  |
| ----- |
| Meena |


## 4. Get unique departments using DISTINCT
QUERY: SELECT DISTINCT department FROM employees;

#### Output:
| department |
| ---------- |
| IT         |
| HR         |
| Finance    |


## 5. Get unique countries
QUERY: SELECT DISTINCT country FROM employees;

#### Output:
| country |
| ------- |
| India   |
| UK      |
| USA     |

