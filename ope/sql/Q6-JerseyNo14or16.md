Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".
 Problem Statement: 
Q001flisdb: Write an SQL query to print the name, the jersey number and the name of the manager (of the team) of each player 
whose jersey number is either 14 or 16. Note that the players could be of different teams. [Database: FLIS] flisdb: 

![](https://backend.seek.onlinedegree.iitm.ac.in/23t2_cs2001/assets/img/flis.png?seed=47436&url=assets/img/flis.png)

```sql
SELECT players.name, players.jersey_no, managers.name
FROM players
JOIN teams ON players.team_id = teams.team_id
JOIN managers ON teams.team_id = managers.team_id
WHERE players.jersey_no IN (14, 16)
```
