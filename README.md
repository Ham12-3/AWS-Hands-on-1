
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


- Creation of an S3 Event from the property section in the S3 bucket you created


![aws-13](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/bbf40865-44a3-4db2-9985-e9714702a3ac)

- Creation of an event notification




- Creation of queue for the event notification destination


![aws-15](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/ebd7eeb7-4cfc-44c2-9315-15cb02d4008e)

- Editing the SQS Queue policy to accept the event notification

![aws-16](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/7833f3fe-2d8a-4bb5-a275-4d6bec4eae06)

- Generating the policy for the amazon SQS Queue using the aws policy generator

![aws-17](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/fad57e58-0104-4c36-9348-941ababe1f7f)

Here is the policy in JSON

```JSON
{
  "Id": "Policy1711364311955",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Stmt1711364309953",
      "Action": [
        "sqs:SendMessage"
      ],
      "Effect": "Allow",
      "Resource": "arn:aws:sqs:us-east-1:058264276076:demos3notification",
      "Principal": "*"
    }
  ]
}
```
Now our event notification has been created finally

![aws-18](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/497b9e60-c836-48db-8d33-9b3fad1a6c5a)

- Working on the server side encryption settings on the objects in the S3 bucket

![aws-19](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/54ec16d7-1d42-4ad1-a766-112630a5cd59)


- Here is the final encryption being created finally

![aws-20](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/274213c6-fa72-47e3-a645-248d0393671a)

- Setting up an statice website hosting and then planning to work on CORS(Cross Origin Resource Sharing)

![aws-21](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/40d2a591-cc5a-447b-84ca-7f2e2b6baa5e)

- Got an error from setting the static website

![aws-22](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/860e1401-d877-4808-9d62-0b3a740de37e)

- Finally working now

![aws-23](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/cdd792b4-0694-49c6-89d3-942d4893a97d)

Due to the bucket policy I added to allow public access

Here is the bucket policy:

```JSON
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "*"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::demo-encryption-mide/*"
        }
    ]
}

```


- Created another bucket to allow the CORS


![aws-24](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/b8b22ff0-6138-4af3-aad2-156247453d47)


- Then we have the CORS policy to allow the cross origin possible

```JSON
[
    {
        "AllowedHeaders": [
            "Authorization"
        ],
        "AllowedMethods": [
            "GET"
        ],
        "AllowedOrigins": [
            "http://demo-encryption-mide.s3-website-us-east-1.amazonaws.com"
        ],
        "ExposeHeaders": [],
        "MaxAgeSeconds": 3000
    }
]
```

- CORS origin worked finally


![aws-25](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/fd18ea5c-ebc2-484b-af69-5faadca9d646)


- Getting the server side logging for the S3 bucket done


![aws-26](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/4c21f5b2-e1d5-46c4-8473-b9a93de63fe6)

- Making use of S3 presigned URL to share files and data for a specific period of time

![aws-27](https://github.com/Ham12-3/AWS-Hands-on-1/assets/93613316/744f0b9f-5463-4fc6-8f65-141586941dc1)


