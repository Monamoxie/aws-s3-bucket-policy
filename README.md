# AWS S3 BUCKET POLICY

Only use if you need to grant your bucket public access and allow CRUD operations from outside

`{
    "Version": "2008-10-17",
    "Statement": [
        {
            "Sid": "AllowPublicRead",
            "Effect": "Allow",
            "Principal": {
                "AWS": "*"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
        },
        {
            "Sid": "AllObjectActions",
            "Effect": "Allow",
            "Principal": {
                "AWS": "*"
            },
            "Action": "s3:*Object",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
        }
    ]
}`
