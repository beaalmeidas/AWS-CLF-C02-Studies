# Cloud Computing Basics

# TOPICS

- Definition of Cloud Computing
- Characteristics of Cloud Computing
- Advantages and Problems Solved
- Cloud Use Cases
- Deployment Models (Public, Private, Hybrid)
- Types of Cloud Computing
- AWS Cloud Pricing Basics

---

## Cloud Computing – Definition

Cloud computing is the on-demand delivery of compute power, database storage, applications, and other IT resources through a cloud services platform with pay-as-you-go pricing.

- Provisioning of exactly the right type and size of computing resources.
- Access to as many resources as needed, almost instantly.
- A simple way to access servers, storage, databases, and a set of application services.
- Amazon Web Services (AWS) owns and maintains the network-connected hardware, while you provision and use what you need via a web application.

## 5 Characteristics of Cloud Computing

1. **ON-DEMAND SELF-SERVICE**
    
    Users can get computing resources (like servers, storage, etc) whenever needed, without requiring human interaction with the service provider.
    
2. **BROAD NETWORK ACCESS**
    
    Cloud services are accessible over the internet using normal devices, like phones and laptops.
    
3. **RAPID ELASTICITY**
    
    Resources can be quickly scaled up or down according to necessity.
    
4. **MEASURED SERVICE**
    
    Cloud systems track and monitor resource usage to provide transparency and charge users based on their consumption.
    

## Advantages of Cloud Computing and Problems Solved – Cloud Computing

- **Cost Savings**: Pay only for the computing power, storage, and other resources you use.
- **Speed and Agility**: Quickly deploy services and resources.
- **Scalability**: Easily scale resources up or down as needed.
- **High Availability**: Highly available architecture for business continuity.
- **Global Reach**: Access services from any geographical region.
- **Security**: AWS provides robust security capabilities to protect your data.

## Cloud Use Cases

1. **Web Hosting**: Host websites with elastic scaling and high availability.
2. **Big Data Analytics**: Run analytics on large datasets.
3. **Application Hosting**: Host applications with global accessibility and automated scaling.
4. **Disaster Recovery**: Implement disaster recovery strategies with minimized infrastructure.
5. **Backup and Storage**: Store backups in a highly durable and secure manner.

## Deployment Models

**Definition:** Who OWNS and who CAN ACCESS the cloud infrastructure.

- **Public Cloud (AWS & OTHER PROVIDERS)**
    - A third-party provider hosts the infrastructure and services, which are accessible to the public over the internet.
    - Easily scalable and quick deploy
    - Tend to have more security threats
- **Private Cloud**
    - The infrastructure and services are dedicated to a single organization for their exclusive use.
    - Less capable (since there are less resources)
    - More secure
- **Hybrid Cloud**
    - Combines public and private cloud usage (allows organizations to leverage the benefits of both)
    - More flexible

EXTRA: **Multicloud**

- A model where customers use cloud services from multiple public clouds.

## **Types of Cloud Computing**

Definition: Types of services offered by the cloud.

- **Infrastructure as a Service (IaaS)**
    - Provides raw/virtualized computing resources like virtual machines, storage, and networks
    - Offers maximum control over the infrastructure
    - Suitable for developers needing control over OS, middleware, and runtime.
    - Examples: AWS EC2, Google Compute Engine.
- **Platform as a Service (PaaS)**
    - Provides tools and platforms to build, test, and deploy applications without managing the underlying infrastructure
    - Ideal for developers who want to focus on application development.
    - Examples: Heroku, AWS Elastic Beanstalk.
- **Software as a Service (SaaS)**
    - Delivers software applications over the internet, accessible through a browser, without requiring installation
    - Suitable for users needing access to software without infrastructure management.
    - Examples: Google Workspace, Salesforce.

## AWS Cloud Pricing Basics

### 3 fundamental AWS pricing principles:

- **Compute**: The time and resources used by applications from launch to termination, billed hourly
- **Storage**: The cost of storing data in the cloud
- **Outbound transfer**: The cost of data moving between systems

### Other pricing directives:

- **Pay as you go**: Rent resources on-demand
- **Use more, pay less**: Volume discounts and tiered pricing for most services
- **Save when you reserve**: Save money by reserving resources
- **Free usage tier**: New AWS customers receive 12 months of free-tier usage

### Some points on savings:

- **Auto Scaling:** Automatically changes capacity to ensure consistent results at the lowest cost
- **Storage services:** Options to lower pricing based on how frequently data is accessed and the performance needed to retrieve it