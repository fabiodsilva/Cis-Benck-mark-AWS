# Cis-Benck-mark-AWS
Apply CIS Benck-mark on AWS



Instalação do Cis-Bench-mark na nuvem AWS usando cloudformation.

Atualizado pra python 3.8

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
