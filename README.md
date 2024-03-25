
# AWS Hands on Continuation

## Amazon RDS

- The process of creating a database
  ![aws-1](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/7b4cbc2b-de2a-4c6c-9e5e-7f871b51b75e)


- AWS RDS Aurora being created using the mySQL database engine
![aws-2](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/6005c8d5-ab98-408f-9224-773469d3aefc)

- Then the creation of AWS Elasticache Redis Cache

![aws-3](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/676b8d3a-bc7a-476d-8e79-de1f5cbd7f16)

- The creation of a domain abdulhamid.com on amazon Route53,

![aws-4](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/9cd2de89-9aee-4622-98e7-eb202f8a0778)

- Creation of an S3 Bucket

  ![aws-5](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/51d727b4-6a4b-4af0-840a-24698a4007dc)

- S3 bucket named myabdulbucket being created already

  ![aws-6](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/e8be402b-e9e0-4735-a24c-cd0621aa445e)

- Uploading a png file on my AWS S3 bucket

![aws-7](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/e2db96bd-c074-4873-9119-0bc8364ec011)

![aws-8](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/caaa4e22-ac53-43a8-b545-046ac661a210)


Sample of an S3 Bucket policy
```JSON
{

"id" : "Policy15672859245",
"Version": "2012-10-17",
"Statement": [

{

"Sid": "Stmt12674263965",
"Action":[

"s3: BetObject"
],
"Effect":"Allow",
"Resource":"arn:aws:s3:::myabdulbucket",
"Principal":"*"
}
]


}



```

- Uploading a static website on AWS S3, index.html file

![aws-9](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/bf9201f5-37aa-4d2d-b6fd-5a298fccdaea)
![aws-10](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/76e928d1-e73e-4436-b5e3-480e043f163a)
![aws-11](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/2a9d7375-7ab6-4f37-8948-dfcbeac46fd1)

- Bucket Versioning enabled
![aws-1](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/e32fadca-d338-48ec-be54-3e2a5fba8ef9)

- Bucket version for the index.html file shown there

![aws-2](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/168e63cb-19fa-461b-adc9-3aa9c2d1e0cd)

- S3 Bucket Replica being created, by first creating the bucket and its replica


![aws-3](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/9a97e2ec-53d9-435b-bdff-2f80159ef30f)


- Creation of a destination bucket replication rule

![aws-4](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/568afb53-29c6-4423-a03e-bf1c5a39089e)


- Batch Object Operations asking if we want to replicate exisiting objects
![aws-5](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/185fcfe9-5f4a-4271-9703-d15348db6a8b)

  
- the replication rule created finally

![aws-6](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/0aa30582-b8f7-473e-bcf6-9df13473368f)


- Setting of storage classes for the AWS S3 Bucket object from the properties tab


![aws-7](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/0a5ff87b-0a6c-4a8c-aaa8-d0d3e6f76dd8)

![aws-8](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/9d84473d-f8e9-44f4-9a83-10644dfe4d17)


- Ading a lifecycle rule for the objects in the S3 Bucket


![aws-9](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/fc4ea461-504b-4697-a448-9813722ee911)

- Getting started with the EC2 instance metadata Version 2 (V2)

launching of eC2 instance for the instance metadata

![aws-10](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/9d0da330-9fd6-4b19-a04d-6b506ecf32e3)

- The first token code for the imdsV2 being put in our EC2 instance connect to get our token for the metadata

![aws-11](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/c337a7da-37f2-4f6d-af3e-ab335d995fb5)

- Here are the tokens to be used

```shell
TOKEN=`curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600"`

```

```shell
curl -H "X-aws-ec2-metadata-token: $TOKEN" http://169.254.169.254/latest/meta-data/
```

- Our token for imdsV2 getting our EC2 instance metadata works as expected


![aws-12](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/958e741d-ab48-4c6f-b140-67dc8fbe168b)





