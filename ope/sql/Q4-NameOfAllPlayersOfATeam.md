Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

 Problem Statement: 
Q003flisdb:Write an SQL query to find the names of all players of team 'Amigos'.[Database: FLIS] flisdb:

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/05fc7670-8359-4d30-a30f-481ec23a165c)

```sql
SELECT players.name
FROM players
JOIN teams ON players.team_id = teams.team_id
WHERE teams.name = 'Amigos'
```

