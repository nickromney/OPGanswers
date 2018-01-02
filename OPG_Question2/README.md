# Pre-interview test - answer to Question 2
Submitted by Nick Romney 2 January 2018

## Question
Write an Ansible playbook to create an instance that can store items in S3.

### Approach
- Create an AWS S3 bucket
- Create an AWS IAM role for the EC2 instance
- Create an AWS IAM Managed policy to allow writes to the S3 bucket
- Create an AWS EC2 instance, using the IAM role

### Notes
Using Amazon Linux 2 LTS Candidate AMI 2017.12.0 (HVM), SSD Volume Type - ami-b09e1ac9

### Install AWS CLI on Amazon Linux

```curl -O https://bootstrap.pypa.io/get-pip.py
python get-pip.py --user
export PATH=~/.local/bin:$PATH
source ~/.bash_profile
pip install awscli --upgrade --user```

### Use the AWS CLI to test uploading a file from the EC2 instance

```touch file1.txt
aws s3 cp file1.txt s3://nickromneyec2tos3/```