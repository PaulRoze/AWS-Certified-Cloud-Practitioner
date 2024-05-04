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
    - [AWS Well-Architected Framework Overview](#aws-well-architected-framework-overview)
    - [Exam Tips](#exam-tips)



## CapEx vs OpEx
- **Capital Expenditure (CapEx)**: Upfront investment in physical infrastructure, such as data centers and servers.
- **Operational Expenditure (OpEx)**: Pay-as-you-go pricing model, such as AWS, where you pay only for what you use.

## Cloud Computing Advantages and Benefits
### Advantages:
- **Global in Minutes**: Deploy applications in multiple regions around the world in minutes.
- **No Data Center Spending**: No need to spend money on data centers, servers, and other physical infrastructure.
- **Economies of Scale**: Cloud providers can offer lower prices due to economies of scale.
- **Speed and Agility**: Quickly deploy resources and scale up or down as needed.
- **Stop Guessing Capacity**: No need to guess how much capacity you need. Scale up or down as needed.
- **CapEx for Variable Expenses**: Pay only for what you use, rather than investing in physical infrastructure.
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
- **Private Cloud**: Cloud infrastructure is dedicated to a single organization.
- **Advantages**: More control over security and compliance.
### Public Cloud
- **Public Cloud**: Cloud infrastructure is shared by multiple organizations.
- **Advantages**: Economies of scale, pay-as-you-go pricing.
### Hybrid Cloud
- **Hybrid Cloud**: Combination of private and public cloud infrastructure.
- **Advantages**: Support by Direct Connect, VPN, and other technologies.

## Exploring Regions and Availability Zones
### AWS Regions
- **Region**: physical location in the world with multiple Availability Zones.
Aws groups regions into geographic areas. And can include several regions. which each location. 
- **Examples**: Ohio & N.Virginia regions resides in the US East (N. Virginia) region.
### Region Characteristics
- **Independent**: Each region is isolated from other regions.
- **Resource and Service Specific**: Not all services are available in all regions.
### AWS Availability Zones
- **Availability Zone**: One or more discrete data centers with redundant power, networking, and connectivity in an AWS region.
- **Examples**: us-east-1a, us-east-1b.
### Availability Zone Characteristics
- **Highly Available**: Availability Zones are designed to be highly available.
- **Fault Tolerant**: Availability Zones are designed to be fault tolerant.

### Region Quick Quiz!
#### **Who have been asked by an executive if the application lanuched in fault tolerant. You investigate and see that it is currently in us-east-1a only. Is the application fault tolerant?**
<details>
  <summary>Answer</summary>
    <b>No</b>, the application is not fault tolerant because it is only in one Availability Zone.
</details>

#### **You have your application running accross multiple AZs, but it has gone down! What could be the reason?**
<details>
  <summary>Answer</summary>
    The application could have gone down due to a <b>regional issue</b>, such as a power outage.
</details>

### Region Exam Tips
- **Region**: A Region is global and is made up of two or more AZs(Availability Zones).
- **Availability Zone(AZ)**: An AZ is made up of multipe data centers.
- **Multi-AZ**: Such depolyment provides High Availability and Fault Tolerance. 

## Reviewing Edge Locations
### Latency Explained
- **Latency**: Time it takes for data to travel from the source to the destination.
- **Factors**: Distance, Bandwidth, Network Congestion.
### Local Zones
- **Local Zones**: AWS infrastructure deployments that are closer to large population, industry, and IT centers.
- **Examples**: Los Angeles, California.
### Edge Locations
- **Edge Locations**: AWS infrastructure deployments that cache content for faster delivery to users.
- **Examples**: CloudFront, Route 53.
### Edge Quick Quiz!
#### **You have been tasked with ensuring that there is millisecond latency on the latest application launched. What can you use to ensure this?**
<details>
  <summary>Answer</summary>
    You can use <b>Local Zones</b> to ensure millisecond latency.
</details>

#### **You need to lower latency on a website that is available on two continents. What can you use to do this?**
<details>
  <summary>Answer</summary>
    You can use <b>Edge Locations</b> to lower latency.
</details>

### Edge Exam Tips
- **Edge Locations**: Edge Locations ensures low latency by placing content closer to users.
- **Local Zones**: is an extension of a region enabling things like real-time gaming.

## Introducing the frameworks
### Cloud Adoption Framework Overview
- **Cloud Adoption Framework**: Focuses on using AWS to digitally transform and accelerate business outcomes.
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
        - Incedent Response
        - Threat Detection
    - Business
        - Management
            - Finance
            - Portfolio
            - Inovation
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


### AWS Well-Architected Framework Overview
- **Well-Architected Framework**: Focuses on building secure, high-performing, resilient, and efficient infrastructure.
- **Five Pillars**:
    - **Operational Excellence**: Run and monitor systems to deliver business value and improve processes.
    - **Security**: Protect information, systems, and assets while delivering business value.
    - **Reliability**: Ensure a system can recover from failures and meet demand.
    - **Performance Efficiency**: Use IT and computing resources efficiently.
    - **Cost Optimization**: Avoid unnecessary costs and optimize spending.

### Exam Tips
    


