Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

**Problem Statement:**
Q002lisdb: Write a SQL query to find the department code and the number of students in each department who are born after '2003-02-09'. [Database: LIS] lisdb:

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/82c380ff-a131-4bdf-8786-15cebef31680)

```sql
SELECT departments.department_code,
       Count(students.roll_no)
FROM   departments
       JOIN students
         ON departments.department_code = students.department_code
WHERE  students.dob > '2003-02-09'
GROUP  BY departments.department_code 
```
