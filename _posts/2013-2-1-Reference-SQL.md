---
layout: post
title: Reference - SQL
---


## Count occurrences of value 
Can be used to find duplicates in database.

```sql
SELECT distinct A.datname,NumOccurrences
FROM pg_stat_activity A
INNER JOIN
  (SELECT  
    datname, COUNT(datname) AS NumOccurrences
   FROM
     pg_stat_activity
   GROUP BY 
     datname
    )  B
ON
  A.datname = B.datname
ORDER BY NumOccurrences DESC
```