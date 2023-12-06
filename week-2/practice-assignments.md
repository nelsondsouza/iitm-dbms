
## Question 1

Write an SQL statement to find the name of the manager of the team: “All Stars”.  Database: FLIS

```sql
SELECT
  m.name
FROM managers m,
     teams t
WHERE m.team_id = t.team_id
AND t.name = 'All Stars';
```

## Question 2

Write an SQL statement to find the names of all teams.  Database: FLIS

```sql
SELECT  name
FROM  teams;
```

## Question 3

Write an SQL statement to find the titles of books authored by an author having first name as ”Joh Paul” and last name as ”Mueller”.  Database: LIS
```sql
SELECT  c.title  
FROM  book_catalogue  c,  
book_authors  a  
WHERE  c.isbn_no  =  a.isbn_no  
AND  author_fname  =  'Joh Paul'  
AND  author_lname  =  'Mueller';
```

## Question 4

Write a SQL statement to find the titles of books published by 'McGraw Hill Education'.[Database: LIS]

```sql
SELECT title
FROM   book_catalogue
WHERE  publisher = 'McGraw Hill Education';
```

## Question 5

Write an SQL statement to display the first name and the last name of students (stu- dent fname, student lname) pursuing ‘PG’ courses.  Database: LIS

```sql
SELECT  student_fname,  
student_lname  
FROM  students  s,  
members  m  
WHERE  s.roll_no  =  m.roll_no  
AND  member_type  =  'PG';
```
