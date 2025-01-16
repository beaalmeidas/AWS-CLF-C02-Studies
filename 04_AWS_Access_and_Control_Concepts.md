# AWS Access and Control Concepts

# TOPICS

- AWS Access Tools
    - AWS Management Console
    - AWS CLI
    - AWS SDK
    - AWS Mobile Console
    - AWS CloudShell
    - AWS Tools for PoweShell
    - AWS CDK

---

## AWS Access Tools

- **AWS Management Console:** Web user interface to manually interact with AWS services.
- **AWS CLI (AWS Command Line Interface):** Terminal-based tool for developers and administrators; ideal for automation and scripting.
- **AWS SDK:** Language-specific APIs to programmatically interact with AWS services using programming languages like Python, Java, and JavaScript.
- **AWS Mobile Console:** Mobile app to monitor and manage AWS services on the go.
- **AWS CloudShell:** Browser-based shell for running AWS CLI commands without configuring a local environment.
- **AWS Tools for PowerShell:** PowerShell cmdlets for AWS resource management, specifically tailored for Windows environments.
- **AWS CDK (Cloud Development Kit):** Infrastructure as Code (IaC) tool for defining AWS resources using familiar programming languages.

(Management Console, CLI and SDK are the most important ones for the test)

## AWS CLI

- AWS Command Line Interface: A tool to manage AWS services by issuing commands directly in the terminal.
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

- AWS Software Development Kit: A collection of libraries and tools to abstract AWS API calls and simplify programming for AWS services.
- Facilitates integration with AWS APIs through abstraction
- **Use cases:**
    - Automating resource creation and management.
    - Data processing (e.g., uploading files to S3, querying DynamoDB).
    - Building custom applications with AWS service integration.
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

## **AWS Mobile Console**

- **Purpose:** A mobile app that allows you to monitor and manage AWS resources on the go, directly from your mobile device.
- **Features:**
    - View resource status and health.
    - Respond to alarms and notifications.
    - Perform limited tasks such as stopping and starting EC2 instances, managing S3 buckets, etc.
- **Platforms:** Available on both iOS and Android devices.

## **AWS CloudShell**

- **Purpose:** A browser-based shell that provides an environment to run AWS CLI commands without needing to configure a local terminal or install the AWS CLI.
- **Features:**
    - Preconfigured with the AWS CLI, AWS SDKs, and other common tools.
    - 1 GB of persistent storage to save scripts, code, and other files.
    - Allows you to quickly execute AWS CLI commands in the cloud, making it easier to manage resources.
    - Works directly in the browser with no setup required.

## **AWS Tools for PowerShell**

- **Purpose:**A set of PowerShell cmdlets designed to manage AWS resources and automate tasks using Windows-based environments.
- **Features:**
    - Simplifies AWS resource management using the PowerShell scripting environment.
    - Allows you to script interactions with AWS services like EC2, S3, IAM, and others.
    - Supports both AWS CLI-style commands and native PowerShell commands.
    - Perfect for Windows-centric automation and administration.

## **AWS CDK (Cloud Development Kit)**

- **Purpose:**A framework that allows developers to define AWS infrastructure using familiar programming languages like Python, Java, JavaScript, and TypeScript.
- **Features:**
    - **Infrastructure as Code (IaC):** Use code to define cloud resources rather than manually configuring them.
    - **Multi-Language Support:** Works with Python, TypeScript, JavaScript, Java, and .NET languages.
    - **Declarative Syntax:** Write high-level constructs (e.g., `Bucket`, `Lambda`, `EC2`) instead of raw CloudFormation templates.
    - **Automatic CloudFormation Generation:** Translates high-level code into CloudFormation templates, which are then deployed to AWS.