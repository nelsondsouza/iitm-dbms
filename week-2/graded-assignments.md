## Question 1
#Write an SQL statement to find the match numbers of those matches in which the host team scored more (goals) than the guest team. [Database: FLIS]

```sql
SELECT match_num
FROM   matches
WHERE  host_team_score > guest_team_score;
```

## Question 2
Write an SQL statement to find the match numbers and fourth referees ID of the matches where assistant referee 1(assistant_referee_1) is 'R0002'.[Database: FLIS]

```sql
SELECT match_num, fourth_referee
FROM match_referees
WHERE assistant_referee_1 = 'R0002';
```

## Question 3
Write an SQL statement to find the names of players of the team: 'All Stars'.[Database: FLIS]

```sql
SELECT players.name
FROM   players
       JOIN teams
         ON players.team_id = teams.team_id
WHERE  teams.name= 'All Stars';
```

## Question 4
Write an SQL statement to find the first names and mobile number (student_fname, mobile_no) of students who belong to the department with department code as 'EE' and who were born after '2001-06-15'.[Database: LIS]

```sql
SELECT student_fname, mobile_no
FROM   students
WHERE  department_code = 'EE'
       AND dob > '2001-06-15';
```

## Question 5
Write an SQL statement to find the last names (faculty_lname) of male faculty who belong to the department:'Electrical Engineering'.[Database: LIS]

```sql
SELECT faculty_lname
FROM   faculty
       JOIN departments
         ON faculty.department_code = departments.department_code
WHERE  faculty.gender = 'M'
       AND departments.department_name = 'Electrical Engineering';
```
