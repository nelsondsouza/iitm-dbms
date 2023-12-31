In this question, you must write a Python program to output the name of the main referee for a given match date (in yyyy-mm-dd format). The input to your program is a file named “date.txt” that has the match date as the first word of the file. Your program must assume that date.txt resides in the same folder as your Python program.  
 
The output name has to be formatted as follows. The last name is displayed followed by the initials of the first name, then a full stop, a space and then the initials of the middle name (if the middle name exists), followed by a full stop.

-   For example, if the name of the main referee is “Kennedy Sapam”, the output must be ”Sapam K.”
    
-   If the name of the main referee is “Asit Kumar Sarkar”, the output must be ”Sarkar A. K.”
    

![](https://backend.seek.onlinedegree.iitm.ac.in/23t1_cs2001/assets/img/flis.png)  


```python
import sys
import os
import psycopg2

file = open('date.txt', 'r')
date = file.read()

try:
    connection = psycopg2.connect(
        database = sys.argv[1],
        user = os.environ.get('PGUSER'),
        password = os.environ.get('PGPASSWORD'),
        host = os.environ.get('PGHOST'),
        port = os.environ.get('PGPORT'))
        
    cursor = connection.cursor()
    
    query = "select referees.name from match_referees, matches, referees where match_referees.match_num = matches.match_num and matches.match_date = '{}' and match_referees.referee = referees.referee_id".format(date)
    
    cursor.execute(query)
    
    result_of_query = cursor.fetchall()
    
    for result in result_of_query:
        list_of_name = list(map(str, result[0].split(" ")))
        final_result = list_of_name[-1]
        for name in list_of_name[:-1]:
            final_result += " "+name[0]+"."
    print(final_result)
        
    cursor.close()
except(Exception, psycopg2.DatabaseError) as error:
    print(error)
finally:
    connection.close()  
```
