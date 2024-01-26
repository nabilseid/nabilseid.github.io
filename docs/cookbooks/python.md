# Python Cookbook

### Handling `Unnamed: n` column in pandas

- Set index to False when writing to csv file.
- Set col index 0 when reading csv file.

```python
pd.to_csv('flat_file.csv', index=False)   # set index to false when writing
pd.read_csv('flat_file.csv', index_col=0) # set index_col to 0 when reading
```

### Change dtype in pandas

- Types can be given at reading
- After reading column type can be changed with `to_numeric()` `astype()` `to_datetime()...`

`to_numeric()` will change type to integer or float as appropriate.
`astype()` let you specify the type you want. It accept a single type or dict of column names paired with types.

[Reference](https://stackoverflow.com/a/28648923/11450091)

```py 
# Give column type when reading, setting dtypes of columns on dtype
df = pd.read_csv('flat_file.csv', dtype={'col_name': str}) 

# Changing types of dataframe column

# change col_name type to numeric. 
df.col_name = pd.to_numeric(df.col_name) 
# change col types with astype
df = df.astype({'col_name': str, 'col_name_2': float}) 
# changing single col
df.col_name = df.col_name.astype(float) 
```
