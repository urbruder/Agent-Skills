# SQL Query Framework

## Query design checklist

- What is the business question?
- What is one row in the output?
- What tables are needed?
- What filters apply?
- What joins are needed?
- Is there a one-to-many join risk?
- What date field defines the period?
- Are nulls meaningful?
- What metric formula should be used?

## Common patterns

### Aggregation

```sql
select date_trunc('month', created_at) as month, count(*) as orders
from orders
group by 1
order by 1;
```

### Join with CTE

```sql
with customers as (
  select id, email from users
)
select c.email, count(o.id) as orders
from customers c
left join orders o on o.user_id = c.id
group by 1;
```

### Window function

```sql
select *,
  row_number() over (partition by customer_id order by created_at desc) as rn
from orders;
```

## Dialect notes

BigQuery uses backticks and functions like `DATE_TRUNC(date, MONTH)`.
Postgres uses `date_trunc('month', timestamp)`.
Snowflake uses `DATE_TRUNC('month', date_col)`.
SQL Server uses different date functions and brackets sometimes.

## Validation

Check row counts before and after joins. Check duplicate keys. Compare totals to known dashboard numbers.
