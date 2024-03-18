
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





