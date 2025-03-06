
# AWS CLI (Command Line Interface)

AWS CLI (Command Line Interface) is a powerful tool that allows users to interact with AWS services directly from the command line. It enables automation, scripting, and seamless management of AWS resources.

## Features of AWS CLI
- **Manage AWS Resources**: Create, modify, and delete AWS resources using commands.
- **Automation & Scripting**: Integrate with shell scripts for automated workflows.
- **Cross-Platform**: Works on Windows, macOS, and Linux.
- **Secure Authentication**: Supports access key-based and role-based authentication.
- **Batch Operations**: Perform multiple tasks efficiently.
- **Integration with AWS Services**: Works with EC2, S3, IAM, Lambda, and more.

## Installing AWS CLI

### Windows
1. Download the installer from [AWS CLI official website](https://aws.amazon.com/cli/).
2. Run the installer and follow the on-screen instructions.
3. Verify installation:
   ```sh
   aws --version
   ```

### macOS (Using Homebrew)
```sh
brew install awscli
aws --version
```

### Linux
```sh
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
sudo apt install ./AWSCLIV2.pkg
aws --version
```

## Configuring AWS CLI
After installation, configure AWS CLI using:
```sh
aws configure
```
You will be prompted to enter:
- AWS Access Key ID
- AWS Secret Access Key
- Default region (e.g., `us-east-1`)
- Output format (default: `json`)

## Common AWS CLI Commands

### S3 (Simple Storage Service)
- List S3 buckets:
  ```sh
  aws s3 ls
  ```
- Upload a file:
  ```sh
  aws s3 cp myfile.txt s3://my-bucket/
  ```
- Download a file:
  ```sh
  aws s3 cp s3://my-bucket/myfile.txt .
  ```

### EC2 (Elastic Compute Cloud)
- List running instances:
  ```sh
  aws ec2 describe-instances
  ```
- Start an EC2 instance:
  ```sh
  aws ec2 start-instances --instance-ids i-1234567890abcdef0
  ```
- Stop an EC2 instance:
  ```sh
  aws ec2 stop-instances --instance-ids i-1234567890abcdef0
  ```

### IAM (Identity and Access Management)
- List IAM users:
  ```sh
  aws iam list-users
  ```
- Create a new IAM user:
  ```sh
  aws iam create-user --user-name mynewuser
  ```

## Benefits of AWS CLI
- **Fast & Efficient**: Execute tasks quickly compared to the AWS Management Console.
- **Scriptable**: Automate tasks for DevOps workflows.
- **Secure**: Use IAM roles and credentials for controlled access.
- **Scalable**: Easily manage multiple AWS accounts and services.

AWS CLI is a must-have tool for developers, system administrators, and DevOps engineers looking to efficiently manage AWS resources through the command line.
