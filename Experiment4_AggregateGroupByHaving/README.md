# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**

![image](https://github.com/user-attachments/assets/6d478a1e-f402-4d9b-b1b4-82acd1ca3b6a)


```sql
SELECT Diagnosis, COUNT(*) AS DiagnosisCount
FROM MedicalRecords
GROUP BY Diagnosis
ORDER BY DiagnosisCount DESC
LIMIT 1;
```

**Output:**

![image](https://github.com/user-attachments/assets/21e78e1e-a092-4e23-a4f1-df3f6255446b)


**Question 2**

![image](https://github.com/user-attachments/assets/ead773fb-d4d6-4f4b-9c02-a9cb011f8e9b)


```sql
SELECT 
  Specialty,
  Gender,
  COUNT(*) AS TotalDoctors
FROM Doctors
GROUP BY Specialty, Gender
ORDER BY Specialty, Gender;
```

**Output:**

![image](https://github.com/user-attachments/assets/0df250ba-82ff-4b1d-8010-0c289f6e6a6d)

**Question 3**

![image](https://github.com/user-attachments/assets/f37d5384-c40e-4888-be9d-067a2dfd521f)


```sql
SELECT 
  Address,
  COUNT(*) AS TotalPatients
FROM Patients
GROUP BY Address
ORDER BY Address;
```

**Output:**

![image](https://github.com/user-attachments/assets/a780c5d8-c7e8-4f6e-a618-4f9842285403)


**Question 4**

![image](https://github.com/user-attachments/assets/99fbc0ee-4eab-4951-8329-b893fb6899d6)



```sql
SELECT 
  SUM(purch_amt) AS TOTAL
FROM orders;
```

**Output:**

![image](https://github.com/user-attachments/assets/42323470-da2a-480d-ada5-7696509c260c)


**Question 5**

![image](https://github.com/user-attachments/assets/cf422229-bf29-4df5-a8ba-42c28e84fe93)


```sql
SELECT 
  COUNT(*) AS COUNT
FROM employee
WHERE age > 32;```

**Output:**

![image](https://github.com/user-attachments/assets/5f6bcb0e-eaa3-4c0d-98b8-c49faaeefc45)


**Question 6**
---
-- Paste Question 6 here

```sql
-- Paste your SQL code below for Question 6
```

**Output:**

![Output6](output.png)

**Question 7**

![image](https://github.com/user-attachments/assets/ddb513e9-d0dd-4ccc-a25a-2ca4b7aa5079)

```sql
SELECT 
  COUNT(DISTINCT age) AS COUNT
FROM employee;
```

**Output:**

![image](https://github.com/user-attachments/assets/a21d4163-6297-456f-9546-8b006ce9f684)


**Question 8**
---
-- Paste Question 8 here

```sql
-- Paste your SQL code below for Question 8
```

**Output:**

![Output8](output.png)

**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
