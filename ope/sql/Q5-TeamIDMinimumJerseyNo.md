Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".
 Problem Statement: 
Q003flisdb: Write an SQL query to find the team ID and the minimum jersey number of each team.[Database: FLIS] flisdb: 

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/7da28726-e422-40a3-9ed0-4a6aed608b56)

```sql
SELECT team_id, MIN(jersey_no) AS min_jersey_no
FROM players
GROUP BY team_id
```
