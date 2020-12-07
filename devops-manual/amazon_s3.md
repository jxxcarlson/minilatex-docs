beginMetadata:
{
    "id": "3bb611ee-e549-42d5-aa56-b2e95387978e",
    "documentNumber": 350,
    "author": "jxxcarlson",
    "title": "Amazon S3",
    "path": "devops-manual/amazon_s3.md",
    "tags": [],
    "keyString": "amazon s3 a=jxxcarlson devops-manual/amazon_s3.md ",
    "timeCreated": 1606451633494,
    "timeModified": 1606451678497,
    "public": false,
    "collaborators": [],
    "docType": "markdown",
    "versionNumber": 0,
    "versionDate": 0
}
endMetadata
[DevOps  Manual](/uuid:11a4b5c6-a8da-40e0-adbe-4276b2743089)

# Amazon  S3

## CLI

[Getting started](https://aws.amazon.com/cli/)

[Reference]

```nolang
$ aws help
$ aws s3 ls s3://mybucket
$ aws s3 cp myfile s3://mybucket/myfolder --acl public-read
$ aws s3 cp myfolder s3://mybucket/myfolder --recursive
$ aws s3 sync myfolder s3://mybucket/myfolder \
  --exclude *.tmp
```
