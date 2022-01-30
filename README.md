# Cis-Benck-mark-AWS
Apply CIS Benckmark on AWS

What this Template does:

     * Check Root Account was used;
     * Check root account has MFA;
     * Check Console Login Failures;
     * Check users without MFA


Obs: This is a update from old version     
     URL: https://us-east-2.console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/create/template?stackName=Compliance-CIS-Benchmark&templateURL=https://aws-quickstart.s3.amazonaws.com/quickstart-compliance-cis-benchmark/templates/main.template
 


Cis-Benchmark on AWS using Cloudformation.


## Requirements

A e-mail where the alarm will be send.

Create a Bucket S3, and apply "Static website hosting".

And now apply the follow policy to allow read-only access
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
            "Resource": "arn:aws:s3:::YOUR-BUCKET-S3/*"
        }
    ]
}
```



