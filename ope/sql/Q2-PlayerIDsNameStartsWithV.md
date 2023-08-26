
Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

 Problem Statement: 
Q001flisdb: Write an SQL query to find the player IDs of the players whose name starts with 'V'.[Database: FLIS] flisdb: 

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/62686a7d-0366-4893-8398-1cb89ebddf3f)

```sql
SELECT player_id
FROM players
WHERE name LIKE 'V%'
```
