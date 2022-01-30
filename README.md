# Cis-Benckmark-AWS
Apply CIS Benckmark on AWS

What this Template does:

     * Check Root Activity;
     * Check Console Login Failures;
     * Check Console Signin Without MFA
     * Check KMS Key Disabled or Scheduled for Deletion
     * Unauthorized Activity Attempt


Cis-Benchmark on AWS using Cloudformation.


## Requirements

1 - A e-mail where the alarm will be send.

2 - Create a new Bucket S3, and apply "Static website hosting".

3 - Disable "Block all public access"

4 - And now apply the follow policy to allow read-only access

```
    {
        "Version": "2012-10-17",
        "Statement": [
            {
                "Sid": "PublicRead",
                "Effect": "Allow",
                "Principal": "*",
                "Action": [
                    "s3:GetObject",
                    "s3:GetObjectVersion"
                ],
                "Resource": "arn:aws:s3:::YOUR-NEW-BUCKET-S3/*"
            }
        ]
    }
```




## Obs: This is a update from old version which works just in python 2.7    
     https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/template?stackName=Compliance-CIS-Benchmark&templateURL=https://aws-quickstart.s3.amazonaws.com/quickstart-compliance-cis-benchmark/templates/main.template
