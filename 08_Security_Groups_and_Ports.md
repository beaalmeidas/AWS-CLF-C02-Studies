# Security Groups and Ports

Created by: Beatriz Almeida
Created time: January 5, 2025 11:33 PM

# TOPICS

- Security Groups – Definition and important points
- Key Features of Security Groups
- Security Groups use cases
- Security Group Rules
- Best practices
- Important Ports

---

## Security Groups

Virtual firewalls that control the traffic in EC2 instances, controlling inbound and outbound traffic.

- They rovide a way to manage access to resources within a VPC.
- It helps secure your resources in Amazon Virtual Private Cloud (VPC) by allowing or denying specific types of traffic based on rules.

## **Key Features**

- **By default, all inbound traffic is denied, and all outbound traffic is allowed.**
- You can specify rules based on protocol (TCP, UDP, ICMP), port number, and source IP address or CIDR block.

## **Security Group use cases**

- Restricting access to an application server (allowing only specific IPs).
- Allowing traffic from specific ports (e.g., HTTP/HTTPS).
- Isolating database instances from public access.

## Security Group Rules

- Each security group can have up to **60 inbound and 60 outbound rules** by default.
    - This limit can be increased by requesting through AWS Support
- When you create a VPC, a default security group is automatically created, which allows all outbound traffic and denies all inbound traffic by default.
- You can assign multiple security groups to a single EC2 instance.

## Security Best Practices

- Apply the principle of least privilege (only allow necessary traffic).
- Regularly review and audit security group rules.
- Use descriptive names and tags for easy management.

## Important Ports

| **Port Number** | **Protocol** | **Service** | **Description** |
| --- | --- | --- | --- |
| 20 | TCP | FTP (Data Transfer) | Used for transferring files over FTP. |
| 21 | TCP | FTP (Control) | Used for controlling file transfer sessions. |
| 22 | TCP | SSH | Secure Shell for secure logins and command execution. |
| 80 | TCP | HTTP | Hypertext Transfer Protocol for web traffic. |
| 443 | TCP | HTTPS | Secure HTTP for secure web traffic. |
| 3389 | TCP | RDP | Used for Remote Desktop Protocol, allowing users to connect to and control remote Windows machines. |