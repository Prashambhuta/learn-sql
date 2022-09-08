# Common Table Expressions

CTE are used to simplify drived, nested and complex queries, which are reusable and easily readable. CTE are used to break complex logic. 

To get started, we create a temporary table.

```sql
DROP TABLE IF EXISTS temp_table;

CREATE TABLE temp_table (
    name VARCHAR,
    object_id int
);
```

A common cte:

```sql
WITH my_cte AS (
    SELECT name, object_id 
    FROM temp_table
    WHERE object_id > 50
)
SELECT name
FROM my_cte;
```

### Subquery vs CTE

Working with cte instead of subquery, for example:

#### Subquery:

§products table
|id | product_name | price|
|----| ---- | ----|
|1| shirt | 299|
|2| tshirt | 199 |
|3| jeans | 499 |

```sql
SELECT product_name, price 
FROM products
WHERE price > (SELECT AVG(price) FROM products);
```

#### CTE:

```sql
WITH price_cte AS (
    SELECT product_name, price, AVG(price) as avg_price FROM products
    GROUP BY product_name, price
)
SELECT product_name 
FROM price_cte where price > avg_price;
```