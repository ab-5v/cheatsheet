# SQL

## Explore

- `show tables`
- `describe <table_name>`
- `describe function <function_name>`

## Examples

### Sampling

```sql
SELECT
  data
FROM
  table TABLESAMPLE(5 PERCENT)
```

### Temporary table

```sql
CREATE TEMPORARY TABLE tmp_table AS
  SELECT
    id
  FROM
    table_1
  WHERE
    condition IS NOT NULL
;

SELECT
  value
FROM
  table_2 t2
WHERE
  EXISTS (SELECT id FROM tmp_table tmp WHERE tmp.id = t2.id)
```
