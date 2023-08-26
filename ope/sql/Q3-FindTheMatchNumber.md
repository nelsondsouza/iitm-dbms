Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

 Problem Statement: 
Q003flisdb: Write an SQL query to find the match number where the host team ID is 'T0004' and the guest team ID is 'T0002'.[Database: FLIS] flisdb: 

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/638824e3-02ef-4876-9b7e-1d7fa75b3b6c)

```sql
SELECT match_num
FROM matches
WHERE host_team_id = 'T0004'
AND guest_team_id = 'T0002'
```
