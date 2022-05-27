---
title: SQL on Pandas
---

## How to execute SQL on a Pandas DataFrame

Pandas DataFrames stored in local variables can be queried as if they are regular tables within DuckDB.

```py
import duckdb
import pandas

# connect to an in-memory database
con = duckdb.connect()

my_df = pandas.DataFrame.from_dict({'a': [42]})

# query the Pandas DataFrame "my_df"
results = con.execute("SELECT * FROM my_df").df()
```
