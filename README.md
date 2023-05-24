### s3 index.html
https://02-serving-spa-guschins.s3.eu-west-1.amazonaws.com/index.html

### CloudFront
https://diofnp3m9i6l5.cloudfront.net/

### Bucket policy
``````
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity E21G5710R3CMLV"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::02-serving-spa-guschins/*"
        }
    ]
}
