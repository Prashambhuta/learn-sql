# Transactions in SQL

Transactions are a way to make sure complete queries are run before commiting the changes permanently to the database. It is a good way to manage discrepancy in databases.

```sql
BEGIN -- begin transaction

<SQL QUERY>

COMMIT; -- commit changes permanently
<>
```
