## Download a file from S3
```aws s3 cp s3://fh-pi-name-f-eco/test.txt . ```

## List files in directory
``` aws s3 ls --recursive --summarize s3://fh-pi-name-f-eco/directory1/directory2```

## Use quotations to use a directory name with spaces 
*Ideally do not use spaces in names!!
``` aws s3 ls "s3://fh-pi-name-f-eco/test final.txt" ```

## Delete a file from S3
```aws s3 rm s3://fh-pi-name-f-eco/test.txt ```

## Delete all files in a directory
``` aws s3 rm s3://fh-pi-name-f-eco/directory1/directory2 --recursive ```

## Do a dry-run before removing a large batch of items to confirm 
``` aws s3 rm --dryrun --recursive s3://fh-pi-name-f-eco/directory1/directory2 ```

## Delete multiple files with a prefix/suffix
* This command deletes all files with the prefix "slurm" and keeps everything else.

### first the dry-run
```aws s3 rm --dryrun --recursive --include "slurm*" --exclude "*" s3://fh-pi-name-f-eco/directory1/directory2 ```
### then delete
```aws s3 rm --recursive --include "slurm*" --exclude "*" s3://fh-pi-name-f-eco/directory1/directory2 ```
