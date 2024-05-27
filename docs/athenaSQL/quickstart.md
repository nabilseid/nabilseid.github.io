### Installing athenaSQL

```bash
$ pip install athenaSQL
```

### Usage

Using athenaSQL is stright forward. First we create a table abstraction class then building a query is just calling chain methods on top of it.

```python
from athenaSQL import Athena

# creating athena table instance from database
table = Athena('database_name').table('table_name')

# creating athena table instance from database
query = table.select()

query.show_query()
```

```
SELECT
    *
FROM "database_name"."table_name"
```
