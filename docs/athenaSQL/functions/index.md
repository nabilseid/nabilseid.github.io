# Functions

Functions are performed on columns. You can get more references
[here](https://trino.io/docs/current/functions.html>).

Aggregating functions should be used on non grouping cols if query is
grouped. Aggregating functions can also be used in place of window
functions.

`sqrt(col)`: Computes the square root of the specified float value.

`abs(col)`: Computes the absolute value.

`mean(col)`: Aggregate function: returns the average of the values in
a group.

`geometric_mean(col)`: Returns the geometric mean of all input values.

`stddev(col)`: Returns the sample standard deviation of all input
values.

`variance(col)`: Returns the sample variance of all input values.

### Supported queries

* [Aggregation](aggregation/)
* [String](string/)
* [Date and Time](date_time/)
* [URL](url/)
* [Window](window/)
* [Unicode](unicode/)
* [UUID](uuid/)