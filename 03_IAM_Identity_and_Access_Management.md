# IAM – Identity and Access Management

Created by: Beatriz Almeida
Created time: December 6, 2024 7:17 PM

# TOPICS:

- IAM – Definition
- Initial Concepts (Users, Groups, Roles)
- IAM Permissions and Policies
- IAM Security Tools
- IAM Guidelines and Best Practices
- Multi-Factor Authentication in AWS

---

## IAM – Definition

Service that enables you to securely control access to AWS resources. It allows you to manage:

- Who ****can access resources.
- What actions they can perform on those resources.

## Initial Concepts

- **Users**
    - Individuals that interact with AWS services
    - All Users have unique credentials
    
    OBSERVATIONS:
    
    - Users do not have to belong to a group
    - Users can belong to multiple groups
    
- **Groups**
    - Groupings of IAM Users to simplify permissions management
    
- **Roles**
    - Grant temporary permissions to entities (users, applications, or AWS services).
    - Ideal for granting cross-account or service-to-service access.

IAM Roles for Services

- Roles can be given to services to allow them to perform actions on behalf of users or applications.
- Example use case: An EC2 instance can assume a role to access S3 buckets without the need for storing long-term credentials.

## IAM Permissions and Policies

- **Permissions** are defined using policies.
- **Policies**
    - Policies are JSON documents that define permissions.
    - Function: Specify what actions are allowed or denied on specific resources.
    - Policies can be attached to: **Users, Groups, Roles**
    - Policy Types:
        - Inline Policies: Attached to a single User, Group or Role
        - Managed Policies: Reusable policies created and maintained by AWS or the customer
        - Group Inherited Policies: Apply to all users in a group
    - Key elements of a policy:
        1. **Version**: Policy language version (e.g., `2012-10-17`).
        2. **Statement**: Contains one or more permissions (allow or deny).
        3. **Action**: Specifies which AWS service actions are allowed or denied.
        4. **Resource**: Specifies the AWS resources to which the actions apply.
        5. **Effect**: Either `Allow` or `Deny`.
    - Policy example:
    
    ```json
    {
      "Version": "2012-10-17",
      "Statement": [
        {
          "Effect": "Allow",
          "Action": "s3:ListBucket",
          "Resource": "arn:aws:s3:::example-bucket"
        }
      ]
    }
    ```
    

### Password Policies

AWS allows you to define a **password policy** for IAM users to ensure strong security standards.

Common password policy settings:

- Minimum password length
- Specific characters
- Require unique password
- Implement password expiration after a certain period
- Multi-Factor Authentication

## IAM Security Tools

Helpful tools for maintaing security within your IAM entities.

- **IAM Credential Report:** Report with details and credentials about all IAM users in the AWS account
- **IAM Access Advisor:** Shows service permissions granted to a user and indicates the last time those permissions were used.
- **IAM Policy Simulator:** A tool that lets you test and validate the impact of IAM policies before applying them to users, groups, or roles.

## IAM Guidelines and Best Practices

1. **Follow the Principle of Least Privilege**:
    - Grant only the permissions required to perform a specific task.
    - Regularly review and adjust permissions as needed.
2. **Enable Multi-Factor Authentication (MFA)**:
    - Enforce MFA for privileged IAM users (e.g., admin accounts).
    - Adds an additional layer of security by requiring users to provide a code from an MFA device along with their password.
3. **Use IAM Roles Instead of IAM Users for Applications**:
    - Assign roles to AWS resources instead of using IAM user credentials in code or configuration files.
    - Prevents security issues that could arise from accidental exposure of long-term credentials.
4. **Rotate IAM Credentials Regularly**:
    - Regularly rotate IAM access keys and passwords.
    - Remove unused credentials to reduce risk.
5. **Use AWS Managed Policies for Common Use Cases**:
    - AWS provides a set of predefined managed policies that are regularly updated.
    - Managed policies are designed for common use cases and provide a good starting point for granting permissions.

## **Multi-Factor Authentication (MFA)**

MFA devices supported by AWS:

- Virtual MFA Device
- Hardware MFA Device
- U2F Security Key
- AWS Multi-Factor Authentication (MFA)