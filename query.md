
Open the playground using '/play'

## Get the size of tables from database

```sql
SELECT
    database AS "Database",
    table AS "Table",
    SUM(data_compressed_bytes) / (1024 * 1024) AS "Size (MB)",
    SUM(data_compressed_bytes) / (1024 * 1024 * 1024) AS "Size (GB)"
FROM
    system.parts
WHERE
    database = 'database_name'
GROUP BY
    database, table;
```
