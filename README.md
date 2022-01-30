# Cis-Benck-mark-AWS
Apply CIS Benck-mark on AWS

Obs: 
This is update from old version 
 URL: https://us-east-2.console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/create/template?stackName=Compliance-CIS-Benchmark&templateURL=https://aws-quickstart.s3.amazonaws.com/quickstart-compliance-cis-benchmark/templates/main.template
 
update from python 2.7 to python 3.8.


Cis-Benchmark on AWS using Cloudformation.



pré-requisitos 

O bucket de origem do scritps devem está com a função "Static website hosting" enabled.

E com a policy abaico aplicada para permitir apenas acesso read only.

----------------------------------------------------------------------------

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
            "Resource": "arn:aws:s3:::aws-quickstart-luckie-tech/*"
        }
    ]
}

--------------------------------------------------------------------------


AWS CIS-Benck-mark

Check Root Account was used
Check root account has mfa
