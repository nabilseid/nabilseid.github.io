# Bash Cookbook

### Delete files/directory recursively from S3

```bash
aws s3 ls BUCKET-NAME --recursive > file_Structure
# after all file keys are extracted filter only the target dir to delete

# create objects of 1000 file key and delete
cat file_Structure | xargs -P8 -n1000 bash -c 'aws s3api delete-objects 
--bucket ml-box-data 
--delete "Objects=[$(printf "{Key=%s}," "$@")], Quiet=true"' _
```

### Delete files/directory recursively

Remove `#!bash -v` flag if you don't want verbose output.

```bash
# find and list all files that match *.bak pattern
find . -name "*.bak" -type f         

# find and delete all files that match *.bak pattern
find . -name "*.bak" -type f -delete 

find . -name "*.egg-info" -type d # find all dir that match the pattern
find . -name "*.egg-info" -type d -exec rm -rv {} + #(1)!
find . -name "*.egg-info" -type d -exec rm -rv {} \; #(2)!
```

1.  Find and delete all dir that match the pattern.
    The `#!bash +` at the end will result in `#!bash rm -rv file1 file2 ...`

2.  Find and delete all dir that match the pattern.
    The `#!bash \;` at the end will result in `#!bash rm -rv file1;` `#!bash rm -rv file2;` ...


