# Python Cookbook

### Handling `Unnamed: n` column  in pandas - `Pandas`

- Set index to False when writing to csv file.
- Set col index 0 when reading csv file.

```python
pd.to_csv('flat_file.csv', index=False)   # set index to false when writing
pd.read_csv('flat_file.csv', index_col=0) # set index_col to 0 when reading
```
