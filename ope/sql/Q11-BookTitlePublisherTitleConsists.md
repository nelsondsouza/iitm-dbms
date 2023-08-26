Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

**Problem Statement:**
Q002lisdb: Write an SQL query to find the book title and publisher of those books whose title consists of `Science' in it. [Database: LIS] lisdb:

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/9b49bc80-0abf-43c1-806d-53d0692051e1)

```sql
SELECT title,
       publisher
FROM   book_catalogue
WHERE  title LIKE '%Science%'
```
