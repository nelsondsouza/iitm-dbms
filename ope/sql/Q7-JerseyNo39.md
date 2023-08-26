Instructions to submit the query:

In the dropdown with Choose Language, select Zip.
Write the query in the editor. There should NOT be any semicolon at the end of the query. 
Click on Test Run.
If it has run correctly, it will give the message: "Correct select query" at the bottom.
If not, it will give an error message or incorrect select query.
Once you are satisfied that your query works correctly, then click on "Submit".

**Problem Statement:**
Q002flisdb: Write an SQL query to find the name, dob and the respective team name and the manager name of each player whose jersey number is '39'.[Database: FLIS] flisdb: 

![image](https://github.com/nelsondsouza/iitm-dbms/assets/19646977/e3a1bf73-7c79-4d9d-83d1-faeae27a3630)

```sql
SELECT players.name, players.dob, teams.name, managers.name
FROM players
JOIN teams ON players.team_id = teams.team_id
JOIN managers ON teams.team_id = managers.team_id
WHERE players.jersey_no = 39
```
