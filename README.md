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

Inside the `Buckets` panel, click on `Create bucket`. 

![Bucket-01](https://user-images.githubusercontent.com/35587864/177148475-bc9b0052-5e3f-4abc-8305-11bb31d7be71.png)
Key in a `Bucket name` of your choice separated by `-`, select your region - or select one closest to your region if your region is not available on the list, and click `Choose bucket`. 

![general-configuration-01](https://user-images.githubusercontent.com/35587864/177148710-a47b1c51-2e72-4619-9eb7-1d5afef994f7.png)

The region will be shown alongside your bucket name on the `Buckets` panel .

![buckets-panel](https://user-images.githubusercontent.com/35587864/177148753-3c06d388-b738-4960-bfeb-fc8a8d22dc5e.png)

Enable ACLs.

![ACL](https://user-images.githubusercontent.com/35587864/177148789-97d0a5f4-5660-4089-9b9b-67650b104693.png)

Uncheck all boxes in `Block Public Access` settings and `agree` to the acknowledgement

![uncheck-01](https://user-images.githubusercontent.com/35587864/177148830-c0c2f6a2-afe2-476a-b1ed-dd98e75b8e9f.png)

Once the bucket is created, you should see them in the list. 

![final-bucket-name-01](https://user-images.githubusercontent.com/35587864/177148961-00c3df65-95f7-417b-8d9a-d3a9090f44c7.png)

Inside `Permissions`, go to `Cross-origin resource sharing` and click on `edit`. Paste the following. 

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

![credentials](https://user-images.githubusercontent.com/35587864/177149113-ecc80c6c-ea14-4766-89a1-27ef1a4d0a34.png)

Click on `Access keys (access key ID and secret access key)` then `Create New Access Key`. 

![credentials_2](https://user-images.githubusercontent.com/35587864/177149136-346d1348-3e5f-4833-b711-ff191cb1421a.png)

![key](https://user-images.githubusercontent.com/35587864/177149164-764c333c-e84b-4859-9080-6aa9f25231d3.png)
