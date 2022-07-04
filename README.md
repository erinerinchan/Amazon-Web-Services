# Amazon Web Services 

- [Create an Amazon Web Services (AWS) account]()
- [Amazon Simple Storage Service (S3)]()
	- [Create a bucket with an AWS region]()
	- [Access Key ID and Secret Access Key]()
- [Set up the `.env` file]()

## Create an Amazon Web Services (AWS) account 

- Visit the [Amazon Web Services (AWS) website](https://portal.aws.amazon.com/billing/signup#/start/email) to create an account. 

## Amazon Simple Storage Service (Amazon S3)

Amazon S3 is a service offered by AWS that provides object storage via a web service interface.

### Create a bucket with an AWS region 

Key in S3 in the search bar, navigate into S3 (not S3 Glacier) and click `Buckets`. 

![S3-01](https://user-images.githubusercontent.com/35587864/177148178-a10ee2a5-b90e-4653-a4f5-cdeb862498bc.png)

Click on `Create bucket`. 

[image] 

Key in a `Bucket name` of your choice separated by `-`, select your region - or select one closest to your region if your region is not available on the list, and click `Choose bucket`. 

[image]

The region will be shown alongside your bucket name on the `Buckets` panel .

[image] 

Enable ACLs

[image] 

Uncheck all boxes in `Block Public Access` settings and `agree` to the acknowledgement

[image] 

Once the bucket is created, you should see them in the list. 
[image] 

Inside `Permissions` go to `Cross-origin resource sharing` and click on `edit`. Paste the following. 

```
[
  {
    "AllowedHeaders": [
      "*"
    ],
    "AllowedMethods": [
      "GET",
      "HEAD",
      "POST",
      "PUT"
    ],
    "AllowedOrigins": [
      "*"
    ],
    "ExposeHeaders": []
  }
]
```
### Access Key ID and Secret Access Key

Navigate into `Security Credentials` in your account dropdown.

[image] 

Click on `Access keys (access key ID and secret access key)` then `Create New Access Key`. 
