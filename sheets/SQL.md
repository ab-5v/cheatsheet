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
