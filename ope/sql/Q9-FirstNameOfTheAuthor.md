Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

**Problem Statement:**
Q002lisdb: Write a SQL query to find the first name of the author of the book 'Java 8 Programming Black Book'. [Database:LIS] lisdb:

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/3c6f9037-c9c7-41f1-88e5-b9ece19bacf2)

```sql
SELECT ba.author_fname
FROM   book_authors AS ba
       JOIN book_catalogue AS bc
         ON ba.isbn_no = bc.isbn_no
WHERE  bc.title = 'Java 8 Programming Black Book' 
```
