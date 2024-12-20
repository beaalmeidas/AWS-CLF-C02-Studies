# AWS Access and Control Concepts

Created by: Beatriz Almeida
Created time: December 6, 2024 7:36 PM

# TOPICS

- AWS Access Tools

---

## AWS Access Tools

- **AWS Management Console:** Web user interface.
- **AWS CLI (AWS Command Line Interface):** Runs in the terminal. Suitable for automation and developers.
- **AWS SDK:** Language-specific APIs for programmatically accessing AWS services using programming languages like Python, etc.
- **AWS Mobile Console:** Mobile app.

## AWS CLI

- AWS Command Line Interface
- Allows you to issue commands and automate tasks across multiple AWS services.
- Windows, macOS, Linux.
- Direct access to the public APIs of AWS services

Important features:

- **Command automation**: Write scripts to automate frequent AWS tasks.
- **Access to all services**: Interact with any AWS service and manage resources from the command line.
- **Profile management**: Manage multiple AWS accounts using different named profiles.
- **JSON and YAML output**: Format CLI responses for better readability or integration with other tools.

Some important commands:

- `aws configure`: For initial setup
- `aws ec2 describe-instances` : For listing EC2 instances
- `aws s3 ls`: For listing S3 instances
- `aws s3 mb s3://new-bucket-name` : Create a new S3 bucket
- `aws s3 file-name.txt s3://new-bucket-name` : Sending a file to S3
- `help`: Add to any command to get detailed instructions on it
- `aws configure --profile profile-name` :  Manage credentials using profiles

## AWS SDK

- AWS Software Development Kit
- Facilitates integration with AWS APIs through abstraction
- Multiplatform (supports many programming languages life Python, Java, JS)
- Simpler code for AWS operations like creating buckets, checking databases, etc
- Authentication and security with IAM

```python
import boto3

# Create an S3 client
s3 = boto3.client('s3')

# List all S3 buckets
response = s3.list_buckets()
print('S3 Buckets:', [bucket['Name'] for bucket in response['Buckets']])
```