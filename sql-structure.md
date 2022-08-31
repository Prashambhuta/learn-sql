# Structure of SQL queries.


I have seen long complex queries where it is hard to figure out the structure. In this file I will try to understand a base of such structures.


```SQL

SELECT <list of columns>, <list of aggregations>           -- select statement

FROM <main table>                           -- main table

JOIN <alternate table> <join condition>     -- join statements

WHERE <condition>                           -- where statements

GROUP BY <condition>                        -- group by conditions

HAVING <condition>                          -- having on aggregated columns
```

## Aggregation & Group by

Tips: 

* Only use columns inside select statemet that are inside the `GROUP BY` statement.

* `HAVING` is used to filter out values of aggregated columns, such as, `HAVING COUNT(*) > 2`

