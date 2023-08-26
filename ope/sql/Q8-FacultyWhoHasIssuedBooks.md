Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

**Problem Statement:**
Q001lisdb: Write an SQL query to find the first name and last name of each faculty who has issued books in July 2021. [Database: LIS] lisdb:

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/967149f5-633d-40d0-a852-f92a6f6be93f)

```sql
SELECT DISTINCT f.faculty_fname, f.faculty_lname
FROM faculty AS f
JOIN members AS m ON f.id = m.id
JOIN book_issue AS bi ON m.member_no = bi.member_no
WHERE bi.doi BETWEEN '2021-07-01' AND '2021-07-31'
```
