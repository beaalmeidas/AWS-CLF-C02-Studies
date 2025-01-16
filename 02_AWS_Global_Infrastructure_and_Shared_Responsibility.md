# AWS Glonal Infrastructure and Shared Responsibility

# TOPICS

- AWS Global Infrastructure (Regions, Availability Zones, Edge Locations)
- AWS Shared Responsibility Model

---

## AWS Global Infrastructure

## **Regions**

- Geographic area of the world
- **Important points about Regions:**
    - Each AWS Region consists of a minimum of three Availability Zones (AZ)
    - Customer applications have to be deployed in the closest-possible AWS Region, for lower latency
    - Services offered vary by region
    - Prices vary by region
    

## **Availability Zones (AZ)**

- Each Availability Zone (AZ) consists of one or more discrete data centers
- Each AZ in a Region has the data and services of the other one(s) mirrored, for fault tolerance/security

## **Edge Locations (EL)**

- Smaller data centers that suplement the AZs
- Functions: Caching, CDN, Cloud Fronting
    - **Caching**:
        
        Storing frequently accessed data temporarily in a location closer to the user to reduce latency and improve performance.
        
    - **CDN (Content Delivery Network)**:
        
        A distributed network of servers that delivers content (images, videos, websites, etc) to users from the server closest to them, improving speed and reliability.
        
    - **Cloud Fronting**:
        
        Technique that uses a Content Delivery Network (CDN) to hide the intended destination of HTTPS traffic / mask the origin of a service or application, often done for performance or privacy purposes.. Example: AWS CloudFront.
        

## AWS Shared Responsibility Model

AWS and its customers share responsibility for the security of their computing activities.

### **AWS Responsibilities**

- Security OF the cloud
- AWS is responsible for protecting the infrastructure
    - Includes hardware, software, networking, and facilities:
        - **Physical security** of data centers and general hardware.
        - Software security, such as maintaining hypervisors, host operating systems, and network infrastructure.
        - **Global network** operations, such as DDoS protection and monitoring.

### **Customer Responsibilities**

- Security in the Cloud
- Customers are responsible for managing and securing what they put in the cloud.
    - Includes:
        - **Data protection**: Encrypt data in transit and at rest.
        - **IAM**: Control access through Identity and Access Management (IAM) roles, users, and policies.
        - **OS and application configurations**: Maintain security of guest operating systems, applications, and firewall configurations.
        - **Network settings**: Manage security group rules and network access control lists (NACLs).
        - **Compliance**: Ensure compliance with regulations and standards based on data storage and usage.

### **Example Responsibilities for Different AWS Services**

| **Service Type** | **AWS Responsibility** | **Customer Responsibility** |
| --- | --- | --- |
| **IaaS (e.g., EC2)** | Securing physical infrastructure, hypervisor, and network. | Configure and secure OS, patch management, data, and network settings. |
| **PaaS (e.g., RDS)** | Managing the database engine, backups, and patching. | Secure data at rest and in transit, manage DB access, and IAM roles. |
| **SaaS (e.g., S3)** | Protecting the service's underlying infrastructure. | Manage permissions, bucket policies, and data lifecycle rules. |