# Subqueries

Subquery in SELECT:
```SQL
SELECT <list of columns>, <list of aggregations>,  <single value subquery> AS        -- select statement

FROM <main table>                           -- main table

JOIN <alternate table> <join condition>     -- join statements

WHERE <condition>                           -- where statements

GROUP BY <condition>                        -- group by conditions

HAVING <condition>                          -- having on aggregated columns
```


Subquery in FROM:

**Note**: Subqueries must have an alias attached to it.

As long as SELECT, WHERE and other statements are compatible.

```sql
SELECT <list of columns>, <list of aggregations>       -- select statement

FROM <sub query including AS>               -- sub query
```

Subquery in JOIN:

Same concept as FROM statement. The subquery should match the structure of other statements.

```sql
JOIN <sub query AS>                         -- join statements
```

Subquery in WHERE:\

```SQL

WHERE <column name> <criteria> <subquery>   -- where statements
```

example: 

§products table
|id | product_name | price|
|----| ---- | ----|
|1| shirt | 299|
|2| tshirt | 199 |
|3| jeans | 499 |

```sql
SELECT product_name, price 
FROM products
WHERE price > (SELECT AVG(price) from database);
```