Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

**Problem Statement:**
Q002flisdb: Write an SQL query to find the player name, data of birth, team name and manager name of each player whose jersey number is 59. [Database: FLIS] flisdb:

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/81193450-05a9-47aa-9298-e32054f65b7e)

```sql
SELECT players.NAME,
       players.dob,
       teams.NAME,
       managers.NAME
FROM   players
       JOIN teams
         ON players.team_id = teams.team_id
       JOIN managers
         ON teams.team_id = managers.team_id
WHERE  players.jersey_no = 59 
```
