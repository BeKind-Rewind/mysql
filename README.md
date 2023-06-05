# mysql


EXERCISES

QUERY:
	
1.display all the information of the employees:
	SELECT * FROM employees;
2. find the salaries of all employees:
	SELECT * FROM salaries;
3.display the unique designations for the employees:
	SELECT DISTINCT title FROM titles;
4.list the emp_name and salary is increased by 15% and expressed as no. of Dollars: 
	SELECT 
    employees.first_name, 
    employees.last_name, 
    (1.15*(salaries.salary)) AS "Salary" 
  FROM employees 
  JOIN salaries 
    ON employees.emp_no = salaries.emp_no;

5. produce the output of employees name and job name as a format of "Employee & Job":
  SELECT 
    CONCAT(
    employees.first_name, 
    ' ', 
    employees.last_name, 
    ' ', 
    titles.title
    ) 
  AS "Employee & Job" 
  FROM employees 
  JOIN titles 
    ON employees.emp_no=titles.emp_no;

6.produce the output of employees as follows:
Employee
JONAS(manager).	
  SELECT 
    CONCAT(e
      mployees.first_name, 
      ' ', 
      employees.last_name, 
      '(', 
      lower(titles.title), 
      ')'
      ) 
    AS "Employee" 
  FROM employees 
  JOIN titles 
  ON employees.emp_no=titles.emp_no;

7.list the employees with Hire date in the format like February 22, 1991.
  SELECT 
    employees.emp_no AS "ID", 
  CONCAT(
    employees.first_name, 
    ' ', 
    employees.last_name
    ) 
    AS "Employee", 
    salaries.salary AS "Salary", 
  DATE_FORMAT(employees.hire_date,'%M %e, %Y') 
    AS "Hire Date" 
  FROM employees 
  JOIN salaries 
    ON employees.emp_no=salaries.emp_no;

8. count the number of characters without considering the spaces for each name.:
  SELECT length(TRIM(last_name))
  FROM employees;

9.list the emp_id, salary, and commission of all the employees:
  SELECT 
    e.emp_no,
    s.salary
  FROM 
    employees e,
    salaries s
  WHERE 
    e.emp_no = s.emp_no;

10.display the unique department with jobs:

11. list the employees who does not belong to department 2001
12.list the employees who joined before 1991:
13.average salaries of all the employees who works as ANALYST
14.display all the details of the employees whose commission is more than their salary:
15.list the employees whose salary is more than 3000 after giving 25% increment
16.list the name of the employees, those having six characters to their name
17.list the employees who joined in the month January.
18. list the name of employees and their manager separated by the string 'works for'
19.list all the employees whose designation is CLERK:
20. list the employees whose experience is more than 27 years
21.list the employees whose salaries are less than 3500:
22. list the name, job_name, and salary of any employee whose designation is ANALYST:
23.list the employees who have joined in the year 1991:
24.list the name, id, hire_date, and salary of all the employees joined before 1 apr 91
25.list the employee name, and job_name who are not working under a manager:
26.list all the employees joined on 1st may 91:
27. list the id, name, salary, and experiences of all the employees working for the manger 68319
28. list the id, name, salary, and experience of all the employees who earn more than 100 as daily salary.
29.list the employees who are retiring after 31-Dec-99 after completion of 8 years of service period
30.list those employees whose salary is an odd value.
31. list those employees whose salary contain only 3 digits
32.list the employees who joined in the month of APRIL:
33.list the employees who are SALESMAN and gathered an experience which month portion is more than 10
34. list the employees of department id 3001 or 1001 joined in the year 1991:
35.list all the employees of designation CLERK in department no 2001
36.list the ID, name, salary, and job_name of the employees for -
1. Annual salary is below 34000 but receiving some commission which should not be more than the salary,
2. And designation is SALESMAN and working for department 3001.
37. list the employees who joined in any year except the month February
38.list the employees whose annual salary is within the range 24000 and 50000
39.list the employees working under the managers 63679, 68319, 66564, 69000:
40.list the employees along with department name
41.list the name, job name, manager id, salary, manager name, manager's salary for those employees whose salary is greater than the salary of their managers. 
42.list the employees whose manager name is JONAS
43.list the name and salary of FRANK if his salary is equal to max_sal of his grade
44.list the employees who are working either MANAGER or ANALYST with a salary range between 2000 to 5000 without any commission.  
45.display all the details of managers
46.display the employee ID, name, job name, hire date, and experience of all the managers
47. list all the employees of grade 2 and 3
48.display all the employees of grade 4 and 5 who are working as ANALYST or MANAGER.
49.list the employees who are senior to ADELYN
50)list the employees of grade 3 and 4 working in the department of FINANCE or AUDIT and whose salary is more than the salary of ADELYN and experience is more than FRANK. List the result in the ascending order of experience
