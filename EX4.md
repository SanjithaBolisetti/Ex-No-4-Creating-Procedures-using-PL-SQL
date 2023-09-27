# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
create table employee2(empid number,empname varchar(10),dept varchar(10),salary number);

SQL> CREATE OR REPLACE PROCEDURE insert_employee_data AS
  2  BEGIN
  3  INSERT INTO employee2(empid,empname,dept,salary)
  4  values(1,'John','HR',50000);
  5  INSERT INTO employee2(empid,empname,dept,salary)
  6  values(2,'Joe','IT',60000);
  7  INSERT INTO employee2(empid,empname,dept,salary)
  8  values(3,'Bob','Finance',55000);
  9  COMMIT;
 10  FOR emp_rec IN (SELECT * FROM employee2) LOOP
 11  DBMS_OUTPUT.PUT_LINE('Employee ID: ' || emp_rec.empid || ', Employee Name: ' || emp_rec.empname || ', Department: ' || emp_rec.dept || ', Salary: ' || emp_rec.salary);
 12  END LOOP;
 13  END;
 14  /

SQL> BEGIN
  2  insert_employee_data;
  3  end;
  4  /
### Output:
![image](https://github.com/dineshgl/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119393633/b0d4a458-7dfb-4967-9ff4-e9a800fded56)

### Result:
Program executed successfully.
