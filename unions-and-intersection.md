# Unions & Intersection.

## Union

Unites the results of two separate queries:

```sql
(QUERY 1)
UNION
(QUERY 2)
UNION
```

UNION ALL shows all the rows, even the repetitive ones.

## Intersection

Shows the result of intersection of two or multiple queries.

```sql
(QUERY 1)
INTERSECT
(QUERY 2)
INTERSECT
```

## Except

Shows all results of query 1 EXCEPT the rows present in query 2.

```sql
(QUERY 1)
EXCEPT  -- show query 1 except common rows in query 2.
(QUERY 2)
EXCEPT 
```