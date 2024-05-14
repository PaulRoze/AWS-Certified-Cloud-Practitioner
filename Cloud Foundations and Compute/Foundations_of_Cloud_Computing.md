# Foundations of Cloud Computing
- [CapEx vs OpEx](#capex-vs-opex)
- [Cloud Computing Advantages and Benefits](#cloud-computing-advantages-and-benefits)
    - [Advantages](#advantages)
    - [Benefits](#benefits)
- [Cloud Computing Models](#cloud-computing-models)
    - [Infrastructure as a Service (IaaS)](#infrastructure-as-a-service-iaas)
    - [Software as a Service (SaaS)](#software-as-a-service-saas)
    - [Platform as a Service (PaaS)](#platform-as-a-service-paas)
- [Cloud Computing Deployment Models](#cloud-computing-deployment-models)
    - [Private Cloud](#private-cloud)
    - [Public Cloud](#public-cloud)
    - [Hybrid Cloud](#hybrid-cloud)
- [Exploring Regions and Availability Zones](#exploring-regions-and-availability-zones)
    - [AWS Regions](#aws-regions)
    - [Region Characteristics](#region-characteristics)
    - [AWS Availability Zones](#aws-availability-zones)
    - [Availability Zone Characteristics](#availability-zone-characteristics)
    - [Quick Quiz!](#region-quick-quiz)
    - [Exam Tips](#region-exam-tips)
- [Reviewing Edge Locations](#reviewing-edge-locations)
    - [Latency Explained](#latency-explained)
    - [Local Zones](#local-zones)
    - [Edge Locations](#edge-locations)
    - [Quick Quiz!](#edge-quick-quiz)
    - [Exam Tips](#edge-exam-tips)
- [Introducing the frameworks](#introducing-the-frameworks)
    - [Cloud Adoption Framework Overview](#cloud-adoption-framework-overview)
        - [Cloud Transformation Domains](#cloud-transformation-domains)
        - [Cloud Transformation Journey Phases](#cloud-transformation-journey-phases)
    - [AWS Well-Architected Framework Overview](#aws-well-architected-framework-overview)
    - [General Design Principles](#general-design-principles)
    - [Exam Tips](#framework-exam-tips)
- [Meeting the AWS Management Console and Accessing AWS](#meeting-the-aws-managment-console-and-accessing-aws)
    - [AWS Management Console](#aws-management-console)
    - [Root User vs IAM User](#root-user-vs-iam-user)
    - [AWS Command Line Interface (CLI)](#aws-command-line-interface-cli)
    - [Programmatic access to AWS services](#programmatic-access-to-aws-services)
    - [AWS Management Console Quick Quiz!](#aws-management-console-quick-quiz)
    - [Exam Tips](#management-console-exam-tips)
- [Foundations of Cloud Computing Exam Tips](#foundations-of-cloud-computing-exam-tips)
---

<div style="text-align: center; margin: 20px 0;">
    <a href="https://aws.amazon.com/certification/certified-cloud-practitioner/">
        <img src="https://d1.awsstatic.com/certification/badges/AWS-Certified-Cloud-Practitioner_badge_150x150.17da917fbddc5383838d9f8209d2030c8d99f31e.png" alt="AWS Certified Cloud Practitioner Badge">
    </a>
</div>

## CapEx vs OpEx
- **Capital Expenditure (CapEx)**: Upfront investment in physical Infrastructure, such as data centers and servers.
- **Operational Expenditure (OpEx)**: Pay-as-you-go pricing model, such as AWS, where you pay only for what you use.

## Cloud Computing Advantages and Benefits
### Advantages:
- **Global in Minutes**: Deploy applications in multiple regions worldwide in minutes.
- **No Data Center Spending**: No need to spend money on data centers, servers, and other physical Infrastructure.
- **Economies of Scale**: Cloud providers can offer lower prices due to economies of scale.
- **Speed and Agility**: Quickly deploy resources and scale up or down as needed.
- **Stop Guessing Capacity**: No need to guess how much capacity you need. Scale up or down as needed.
- **CapEx for Variable Expenses**: Pay only for what you use, rather than investing in physical Infrastructure.
### Benefits:
- **High Availability**: Cloud providers offer high availability and fault tolerance.
- **Elasticity**: Scale up or down as needed.
- **Agility**: Quickly deploy resources.
- **Durability**: Data is stored redundantly across multiple locations.

## Cloud Computing Models
### Infrastructure as a Service (IaaS)
- **IaaS**: Provides virtual servers and storage.
- **Examples**: Amazon EC2, Amazon S3.
### Software as a Service (SaaS)
- **SaaS**: Provides software applications over the internet.
- **Examples**: Gmail, Office 365.
### Platform as a Service (PaaS)
- **PaaS**: Provides a platform for developers to build applications.
- **Examples**: AWS Elastic Beanstalk, Heroku.
## Cloud Computing Deployment Models
### Private Cloud
- **Private Cloud**: The cloud infrastructure dedicated to a single organization.
- **Advantages**: More control over security and compliance.
### Public Cloud
- **Public Cloud**: The cloud infrastructure shared by multiple organizations.
- **Advantages**: Economies of scale, pay-as-you-go pricing.
### Hybrid Cloud
- **Hybrid Cloud**: Combination of private and public cloud infrastructure.
- **Advantages**: Support by Direct Connect, VPN, and other technologies.

## Exploring Regions and Availability Zones
### AWS Regions
- **Region**: physical location worldwide with multiple Availability Zones.
Aws groups regions into geographic areas. And can include several regions. Which each location. 
- **Examples**: Ohio & N.Virginia region resides in the US East (N. Virginia) region.
### Region Characteristics
- **Independent**: Each region is isolated from other regions.
- **Resource and Service Specific**: Not all services are available in all regions.
### AWS Availability Zones
- **Availability Zone**: One or more discrete data centers with redundant power, networking, and connectivity in an AWS region.
- **Examples**: us-east-1a, us-east-1b.
### Availability Zone Characteristics
- **Highly Available**: Availability Zones are designed to be highly available.
- **Fault Tolerant**: Availability Zones designed to be fault tolerant.

### Region Quick Quiz!
#### **You have been asked by an executive if the application launched is fault-tolerant. You investigate and see that it is currently in us-east-1a only. Is the application fault tolerant?**
<details>
  <summary>Answer</summary>
    <b>No</b>, the application is not fault-tolerant because it is only in one Availability Zone.
</details>

#### **You have your application running across multiple AZs, but it has gone down! What could be the reason?**
<details>
  <summary>Answer</summary>
    The application could have gone down due to a <b>regional issue</b>, such as a power outage.
</details>

### Region Exam Tips
- **Region**: A Region is global and comprises two or more AZs(Availability Zones).
- **Availability Zone(AZ)**: An AZ comprises multipe data centers.
- **Multi-AZ**: Such deployment provides High Availability and Fault Tolerance. 

## Reviewing Edge Locations
### Latency Explained
- **Latency**: Time it takes for data to travel from the source to the destination.
- **Factors**: Distance, Bandwidth, Network Congestion.
### Local Zones
- **Local Zones**: AWS infrastructure deployments closer to a large population, industry, and IT centers.
- **Examples**: Los Angeles, California.
### Edge Locations
- **Edge Locations**: AWS infrastructure deployments that cache content for faster user delivery.
- **Examples**: CloudFront, Route 53.
### Edge Quick Quiz!
#### **You have been tasked with ensuring millisecond latency on the latest application launched. What can you use to ensure this?**
<details>
  <summary>Answer</summary>
    You can use <b>Local Zones</b> to ensure millisecond latency.
</details>

#### **You need to lower latency on a website available on two continents. What can you use to do this?**
<details>
  <summary>Answer</summary>
    You can lower latency by using <b>Edge Locations</b>.
</details>

### Edge Exam Tips
- **Edge Locations**: Edge Locations ensures low latency by placing content closer to users.
- **Local Zones**: an extension of a region enabling real-time gaming.

## Introducing the frameworks
### Cloud Adoption Framework Overview
- **Cloud Adoption Framework**: Focuses on using AWS to transform and accelerate business outcomes digitally.
- **Six Perspectives**: 
    - Security:
        - Security:
            - Governance
            - Assurance
            - Application
        - Protection:
            - Infrastructure
            - Data
        - Management:
            - Identity and Access Management
        - Incident Response
        - Threat Detection
    - Business
        - Management
            - Finance
            - Portfolio
            - Innovation
            - Product
        - Data
            - Monetization
            - Science
        - Business Insight
    - Platform
        - Architecture and Engineering
            - Platform
            - Data
        - Continuous Integration and Continuous Delivery(CI/CD)
        - Modern Application Development
        - Provisioning and Orchestration
    - Operations
        - Management
            - Event (AIOps)
            - Incident and Problem
            - Change and Release
            - Performance and Capacity
            - Configuration
            - Patch
            - Availability and Continuity
            - Application
        - Observability
    - Governance
        - Management
            - Program and Project Benefits
            - Risk
            - Cloud Financial
            - Application Portfolio
        - Data
    - People
        - Transformation
            - Leadership
            - Workforce
        - Organization
            - Design
            - Alignment
        - Cloud Fluency
        - Change Acceleration
        - Culture Evolution

#### Cloud Transformation Domains

| **Technology**         | **Process**                  | **Organization**           | **Product**                   |
| ---------------------- | ---------------------------- | -------------------------- | ----------------------------- |
| Migrate and modernize  | Digitize, automate, and optimize | Reimagine orchestration | Reimagine your business model |

#### Cloud Transformation Journey Phases

| **Envision** | **Align** | **Launch** | **Scale** |
|-------------|-----------|------------|-----------|
| **Benefits to business outcomes** | **Gaps across perspectives** | **Deliver initiatives with value** | **Expand sustainable initiatives** |



### AWS Well-Architected Framework Overview
| Focus Area               | Description | Tools and Techniques |
|--------------------------|-------------|----------------------|
| **Security**             | Focuses on protecting data, systems, and any assets your workload uses. | Use **CloudTrail** to log all actions performed in your account. |
| **Cost Optimization**    | Focuses on the ongoing process of maintaining costs in the cloud. | Use **S3 Intelligent-Tiering** to automatically move data. |
| **Performance Efficiency** | Focuses on using computing resources efficiently to meet requirements. | Use **Lambda** to run code with zero administration. |
| **Operational Excellence** | Focuses on creating applications supporting your workload. | Use **CodeCommit** for code and template version control. |
| **Reliability**          | Focuses on architecting a workload to be consistent and recover quickly. | Use **Multi-AZ deployments** of RDS databases. |
| **Sustainability**       | Focuses on environmental impacts like energy efficiency and consumption. | Use **EC2 Auto Scaling** to ensure maximum utilization. |

### General Design Principles

- **Stop Guessing Your Capacity Needs**
  - Focus on precise capacity planning based on actual usage data and trends.
  
- **Test Systems at Production Scale**
  - Ensure systems are tested under production load conditions to guarantee scalability and reliability.
  
- **Consider Evolutionary Architectures**
  - Embrace architectural designs that can evolve to meet changing business requirements.
  
- **Automate with Architectural Experimentation in Mind**
  - Implement automation considering the flexibility needed for future experiments and changes.
  
- **Drive Architectures Using Data**
  - Base architectural decisions on solid data analysis to optimize performance and resource utilization.
  
- **Improve Through Game Days**
  - Regularly schedule game days to simulate outages and other scenarios to improve system resilience and preparedness.

### Framework Exam Tips
- **Understand the CAF Perspectives and the Cloud Transformation Journey Phases.**
  - Gain insights into the Cloud Adoption Framework (CAF) and recognize the stages of the cloud transformation journey.

- **Understand the Well-Architected Framework pillars, design principles, and how they apply in the real world.**
  - Familiarize yourself with the foundational principles of the Well-Architected Framework and learn how to apply them effectively in practical scenarios.

## Meeting the AWS Management Console and Accessing AWS
### AWS Management Console
- **AWS Management Console**: Web-based interface for managing AWS services.
- **Features**: Access to all AWS services, billing, and account management.
### Root User vs. IAM User
- **Root User**: The account owner can access all AWS services.
- **IAM User**: User created within an AWS account with specific permissions.
### AWS Command Line Interface (CLI)
- **AWS CLI**: Command-line tool for managing AWS services.
### Programmatic access to AWS services
- **Application Code**: Access from application code with SDKs using programmatic calls. Integrate directly with applications through code.
- **Software Development Kits (SDKs)**: Access from programming languages (Java, Python, C#, and more). Extensive support for multiple programming languages, enabling diverse development environments.

### AWS Management Console Quick Quiz!
#### **Your AWS account was created last week. You are logging in to your account for the second time to create some resources. Should you use the root user to log in?**
<details>
  <summary>Answer</summary>
    You Should <b>NOT use the root user!</b>.
    When you create an AWS account, your first steps must be to set up MFA and create your daily user or group.
</details>

### Management Console Exam Tips
| Aspect              | Description                                                       |
|---------------------|-------------------------------------------------------------------|
| **Root User Protection** | Multi-factor authentication (MFA) should protect the root user. |
| **Root User Power**     | The root user has power that no other user has.                   |
| **Management Tools**    | The Command Line Interface (CLI) and Software Development Kits (SDKs) are other options for managing AWS resources. |

## Foundations of Cloud Computing Exam Tips
- Service Categories - Reading AWS Services Whitepaper - It will automatically know that some answers are wrong.
    - *Example* - If the question is about a computing service to migrate, our answers are RDS, VPC, S3, WAF, and EC2. We know that RDS, VPC, S3, and WAF are not compute services. So, the answer is EC2.
- Six Advantages of Cloud Computing
    - Going Global in Minutes
    - Stop spending money on your data centers
    - Stop guessing capacity
    - Increase speed and agility
    - Benefit from massive economies of scale
    - Trade fixed expenses for variable expenses
- Cloud Computing Models
    - IaaS - Infrastructure as a Service
    - PaaS - Platform as a Service
    - SaaS - Software as a Service
- Three Cloud Deployment Models
    - Private Cloud - Everything runs on your Infrastructure
    - Public Cloud - Everything run on the cloud provider infrastructure
    - Hybrid Cloud - A mix of both
- Regions and Availability Zones
    - Regions are made up of Availability Zones
    - Availability Zones are made up of multiple data centers
    - Multi-AZ deployments provide High Availability and Fault Tolerance
- Edge Locations
    - Edge Locations are used to cache content for faster delivery to users
    - Local Zones are an extension of a region, enabling things like real-time gaming
- Cloud Adoption Framework
    - Envision, Align, Launch, Scale
    - Six Perspectives: 
        - Business
        - People
        - Governance
        - Platform
        - Security
        - Operations
- AWS Well-Architected Framework: 
    - Security
    - Cost Optimization
    - Performance Efficiency
    - Operational Excellence
    - Reliability
    - Sustainability
- AWS Management Console
    - Root User = POWER
        - IAM User = Specific Permissions
    - AWS CLI
    - Programmatic access to AWS services
