# 365erator

scripts in python & go to translate bulk domain lists into m365 tenant ids

this can quickly translate a full ccTLD/gTLD list into a file allowing reverse lookups

```shell
go run fetch.go demo-domainlist.txt
```

```shell
python3 fetch.py demo-domainlist.txt
```

## example

both the python and go version of these scripts should be given a filename containing a line-delimited set of domains

```shell
echo 'microsoft.com' > domains.txt
echo 'apple.com' >> domains.txt
go run fetch.go domains.txt
```

the output csv should appear similar to

```csv
domain,tenantid
microsoft.com,72f988bf-86f1-41af-91ab-2d7cd011db47
apple.com,ba8f4151-ab0e-4da6-862d-68b05906e887
```
