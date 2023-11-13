1. If a table contains string columns such as name and address, but many queries do not retrieve those columns, consider splitting the string columns into a separate table and using join queries with a foreign key when necessary. When MySQL retrieves any value from a row, it reads a data block containing all the columns of that row (and possibly other adjacent rows). Keeping each row small, with only the most frequently used columns, allows more rows to fit in each data block. Such compact tables reduce disk I/O and memory usage for common queries. [REF](https://dev.mysql.com/doc/refman/8.0/en/optimize-character.html)

2. If using random IDs as primary keys, use numeric IDs since it is faster to compare and sort.

3. Use the ideal data types to optimize disk space usage.