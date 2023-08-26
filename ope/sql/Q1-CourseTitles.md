Instructions to submit the query:

1.  In the dropdown with Choose Language, select Zip.

1.  Write the query in the editor. There should NOT be any semicolon at the end of the query.
2.  Click on Test Run.
3.  If it has run correctly, it will give the message: "Correct select query" at the bottom.
4.  If not, it will give an error message or incorrect select query.
5.  Once you are satisfied that your query works correctly, then click on "Submit".
![](https://backend.seek.onlinedegree.iitm.ac.in/23t2_cs2001/assets/img/university.PNG?seed=41107&url=assets/img/university.PNG)

**Problem Statement:**  
Q006university: Write an SQL query to find the title of the courses that belongs to the 'Statistics' department. [Database: University] university:

```sql
SELECT title
FROM course
WHERE dept_name = 'Statistics'
```
