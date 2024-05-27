# Queries

All queries need either `AthenaTable` or `TempTable` to execute. Query 
instance has `show_query()` that let's you preview the sql query constracted 
and `exec()` to execute constracted query on Athena, `exec()` returns a dataframe.

## Supported queries

* [SELECT](athenaSQL/quereis/select.md)
* [INSERT INTO](athenaSQL/quereis/insert_into.md)
* [CREATE](athenaSQL/quereis/create.md)
* [CREATE AS](athenaSQL/quereis/create_as.md)
* [CTE](athenaSQL/quereis/cte.md)
* [UNLOAD](athenaSQL/quereis/unload.md)
* [WINDOW](athenaSQL/quereis/window.md)