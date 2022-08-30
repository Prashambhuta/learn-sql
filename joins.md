# Joins in SQL

The idea of joining table is to make complex query and aggregrations run.

## Types of Joins

1. INNER JOIN or JOIN

    Default JOIN in SQL, INTERSECTION of two tables.

2. LEFT JOIN

    Anything from the left table that doesnt match up with the right table is **!not dropped**. **Everything from the left table is kept.**

    ```sql
    SELECT col1, col2
    FROM tab1
    LEFT JOIN tab2 ON tab2.id = tab1.fr_id;
    ```

    > All information from `tab1` will be saved.

3. RIGHT JOIN

    Anything from the left table that doesnt match up with the right table is **!dropped**. **Everything from the right table is kept.**

    ```sql
    SELECT col1, col2
    FROM tab1
    RIGHT JOIN tab2 ON tab2.id = tab1.fr_id;
    ```

    > All information from `tab2` will be saved.

4. FULL JOIN

    Union of two tables.