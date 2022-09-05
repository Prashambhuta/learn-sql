# SQL Keywords

### DISTINCT

Selects distinct values from a single column or multiple columns. Use it with `COUNT` to get distinct values inside a column.

### GREATEST

Returns the greatest value from a list of values (integers, or float). Example `GREATEST (20, 30, price)` will return `price` if `price` is > 20 & 30.

### LEAST

Same, but opposite as GREATEST

### CASE

The case statement goes through conditions one by one and returns a value when the first condition is met.

```sql
CASE
    WHEN <condition> THEN <return>
    WHEN <condition> THEN <return>
    ..
    ELSE <return>
```

### PREPARE

The prepare statement helps clean the values before entering it into a query. Especailly useful for running queries through API.