# Ex. No: 4 Creating Procedures using PL/SQL
### Date:
### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
create table employee2(empid number,empname varchar(10),dept varchar(10),salary number);
CREATE OR REPLACE PROCEDURE insert_employee_data AS
BEGIN
INSERT INTO employee2(empid,empname,dept,salary)
values(1,'John','HR',50000);
INSERT INTO employee2(empid,empname,dept,salary)
values(2,'Joe','IT',60000);
INSERT INTO employee2(empid,empname,dept,salary)
values(3,'Bob','Finance',55000);
COMMIT;
FOR emp_rec IN (SELECT * FROM employee2) LOOP
DBMS_OUTPUT.PUT_LINE('Employee ID: ' || emp_rec.empid || ', Employee Name: ' || emp_rec.empname || ', Department: ' || emp_rec.dept || ', Salary: ' || emp_rec.salary);
END LOOP;
END;
/

BEGIN
insert_employee_data;
END;
/
```
### Output:

![image](https://github.com/SanjithaBolisetti/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119393633/c5d7009a-6f6f-4cf8-8940-57b546c3e35c)






### Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
