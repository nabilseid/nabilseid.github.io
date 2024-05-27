# Queries

All queries need either `AthenaTable` or `TempTable` to execute. Query 
instance has `show_query()` that let's you preview the sql query constracted 
and `exec()` to execute constracted query on Athena, `exec()` returns a dataframe.

## Supported queries

* [SELECT](select/)
* [INSERT INTO](insert_into/)
* [CREATE](create/)
* [CREATE AS](create_as/)
* [CTE](cte/)
* [UNLOAD](unload/)
* [WINDOW](window/)