# Compute Technology and Services
- [EC2](#ec2)
- [Containers](#containers)
    - [Containers Overview](#containers-overview)
    - [ECS vs EKS](#ecs-vs-eks)
    - [Quick Quiz!](#containers-quick-quiz)
    - [Exam Tips](#containers-exam-tips)
- [Serverless](#serverless)
    - [What is Serverless?](#what-is-serverless)
    - [Lambda Overview](#lambda-overview)
        - [Lambda Use Cases](#lambda-use-cases)
    - [Faragate Overview](#faragate-overview)
        - [Faragate Use Cases](#faragate-use-cases)
    - [Exam Tips](#serverless-exam-tips)
- [Serveless Pricing](#serveless-pricing)
    - [Lambda Pricing](#lambda-pricing)
    - [Fargate Pricing](#fargate-pricing)
    - [Exam Tips](#serveless-pricing-exam-tips)
- [Additional Compute Services](#additional-compute-services)
    - [Outposts](#outposts)
    - [Lightsail](#lightsail)
    - [Batch](#batch)
    - [Wavelegth](#wavelegth)
    - [Quick Quiz!](#additional-compute-services-quick-quiz)
    - [Exam Tips](#additional-compute-services-exam-tips)

---

<div style="text-align: center; margin: 20px 0;">
    <div style="display: inline-block; margin: 0 10px;">
        <a href="https://docs.aws.amazon.com/ec2/index.html">
            <img src="https://icon.icepanel.io/AWS/svg/Compute/EC2.svg" alt="EC2">
        </a>
    </div>
    <div style="display: inline-block; margin: 0 10px;">
        <a href="https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html">
            <img src="https://icon.icepanel.io/AWS/svg/Containers/Elastic-Container-Service.svg" alt="Elastic-Container-Service(ECS)">
        </a>
    </div>
    <div style="display: inline-block; margin: 0 10px;">
        <a href="https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html">
            <img src="https://icon.icepanel.io/AWS/svg/Containers/Elastic-Container-Registry.svg" alt="Elastic-Container-Registry(ECR)">
        </a>
    </div>
    <div style="display: inline-block; margin: 0 10px;">
        <a href="https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html">
            <img src="https://icon.icepanel.io/AWS/svg/Containers/Elastic-Kubernetes-Service.svg" alt="Elastic-Kubernetes-Service(EKS)">
        </a>
    </div>
    <div style="display: inline-block; margin: 0 10px;">
        <a href="https://docs.aws.amazon.com/lambda/">
            <img src="https://icon.icepanel.io/AWS/svg/Compute/Lambda.svg" alt="Lambda">
        </a>
    </div>
    <div style="display: inline-block; margin: 0 10px;">
        <a href="https://docs.aws.amazon.com/AmazonECS/latest/userguide/what-is-fargate.html">
            <img src="https://icon.icepanel.io/AWS/svg/Containers/Fargate.svg" alt="Fargate">
        </a>
    </div>
    <div style="display: inline-block; margin: 0 10px;">
        <a href="https://docs.aws.amazon.com/outposts/">
            <img src="https://icon.icepanel.io/AWS/svg/Compute/Outposts-rack.svg" alt="Outposts">
        </a>
    </div>
</div>


## EC2
- **Connecting to EC2:** [![Connecting to EC2](https://icon.icepanel.io/AWS/svg/Compute/EC2.svg)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html)
    - AWS Management Console
    - EC2 Instance Connect (EIC)
    - Secure Shell (SSH) and Remote Desktop Protocol (RDP)
    - AWS Systems Manager

## Containers
### Continers Overview**
- **what is containers?** - Containers are a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.
- **Benefits of containers**
        - Portability
        - Operational consistency
        - Efficiency
        - Application development
        - less overhead
- **Use cases for containers**
    - "Lift and shift" applications
    - Refactoring applications
    - Support for microservices architecture
    - Support for CI/CD deployment
    - Easier deployment of repettive tasks
- **Containers on AWS**
    - **Amazon Elastic Container Service (ECS)** [![Amazon Elastic Container Service](https://icon.icepanel.io/AWS/svg/Containers/Elastic-Container-Service.svg)](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)
    - **Amazon Elastic Container Registry (ECR)** [![Amazon Elastic Container Registry](https://icon.icepanel.io/AWS/svg/Containers/Elastic-Container-Registry.svg)](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html)
    - **Amazon Elastic Kubernetes Service (EKS)** [![Amazon Elastic Kubernetes Service](https://icon.icepanel.io/AWS/svg/Containers/Elastic-Kubernetes-Service.svg)](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html)

    

### ECS vs EKS

```mermaid
graph TD;
    A[ECS vs EKS Comparison] --> B[ECS]
    A --> C[EKS]
    B --> D[Fully managed and serverless using Fargate]
    B --> E[Can run with EC2, Fargate, Outposts, or ECS Anywhere]
    B --> F[Supports Docker and Docker Compose CLI]
    C --> G[Fully managed open-source system]
    C --> H[Can run with EC2, Fargate, EKS on Outposts, Local Zones, Wavelength, and EKS Anywhere]
    C --> I[Supports Kubernetes]
```

**Elastic Container Service (ECS):**
- Fully managed and serverless using Fargate
- Can run with EC2, Fargate, Outposts, or ECS Anywhere
- Supports Docker and Docker Compose CLI

**Elastic Kubernetes Service (EKS):**
- Fully managed open-source system
- Can run with EC2, Fargate, EKS on Outposts, Local Zones, Wavelength, and EKS Anywhere
- Supports Kubernetes

### Containers Quick Quiz!
#### **You need to use Docker to manage your newly deployed container-based application. Which AWS service can help you manage the app?**
<details>
  <summary>Answer</summary>
    <b>Elastic Container Service (ECS)</b>
</details>

### Containers Exam Tips
- **Know**: The differences between **Elastic Container Service** and **Elastic Kubernetes Service**.
- **Understand**: When you would use container: **"Lift and shifts"**, **microservices architecture**, **CI/CD**, and **refactoring applications**.

## Serverless
### What is Serverless?
- **Serverless** is a cloud computing model that allows you to build and run applications and services without thinking about servers.
### Lambda Overview
- AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers. the you write in Lambda is called a **Lambda function**. can use alot of languages like: Node.js, Python, Ruby, Java, Go, .NET Core, and custom runtime. Lambda scales automatically, and you pay only for the compute time you consume.

#### Lambda Use Cases
- Real-time file processing - Lambda can process files as they are uploaded to S3.
    - **Example**:
        ```mermaid
            graph LR;
                A[S3] -- file upload triggers --> B[Lambda]
                B -- processes and stores data in --> C[DynamoDB]
        ```
- Sending notifications - Lambda can send notifications to users via email, SMS, or push notifications.
    - **Example**:
        ```mermaid
            graph LR;
                A[CodeCommit] -- triggers --> B[CloudWatch]
                B -- invokes --> C[Lambda]
                C -- sends notification to --> D[SNS]
                D -- delivers notification to --> E[Email]
        ```
- Backend Business Logic - Lambda can be used to run backend business logic for web and mobile applications.
    - **Example**: 
        ```mermaid
            graph LR;
                J[Alexa Skill] -- sends request to --> K[Lambda]
                K -- sends data to --> L[DynamoDB]
                L -- retrieves data for --> K
                K -- responds to --> J
        ```

### Faragate Overview
- **AWS Fargate** is a serverless compute engine for containers that works with both **Elastic Container Service (ECS)** and **Elastic Kubernetes Service (EKS)**. Fargate allows you to run containers without having to manage the underlying infrastructure.

#### Faragate Use Cases
- **Message-Driven Workloads** - Fargate can be used to process messages from a queue.
    - **Example**:
        ```mermaid
            graph LR;
                A[SQS] -- sends message to --> B[Fargate]
                B -- processes message and stores data in --> C[DynamoDB]
        ```
- **Event-Driven Workloads** - Code scanned for sensitive information like account numbers or credentials.
    - **Example**:
        ```mermaid
            graph LR;
                A[CodeCommit] -- commits trigger --> B[Lambda]
                B -- triggers task on --> C[Fargate]
                C -- sends notifications to --> D[SNS]
        ```
- # Lambda vs Fargate
    - The key here that sets Fargate aprt from Lambda.
    Lambda is used for short-lived, event-driven workloads, while Fargate is used for long-running, persistent workloads. If you need to run a process that takes more than 15 minutes, you should use Fargate.

        | Service  | Time Limit       |
        |----------|------------------|
        | [![Lambda](https://icon.icepanel.io/AWS/svg/Compute/Lambda.svg)](https://docs.aws.amazon.com/lambda/) **Lambda**  | < 15 minutes |
        | [![Fargate](https://icon.icepanel.io/AWS/svg/Containers/Fargate.svg)](https://docs.aws.amazon.com/AmazonECS/latest/userguide/what-is-fargate.html) **Fargate** | > 15 minutes |

### Serverless Exam Tips
- **Know**: Your responsibility when **using serverless services** like ** Lambda**
- **Understand**: **Fargate** is considered **serverless**, and is used to manage containers.

## Serveless Pricing
### Lambda Pricing
- **Number of requests**: You are charged based on the number of requests for your functions.
- **Duration**: You are charged based on the time it takes for your code to execute.
- **No charge**: If your code is not running, you are not charged.
- **Free tier**: 1 million requests per month.

### Fargate Pricing
- **No upfront costs**: You pay only for the vCPU and memory that you use.
- **Pay resources**: You pay for the resources you use, per second.
- **No free tier**: Fargate does not have a free tier.

### Serveless Pricing Exam Tips
- **Know**: **Lambda** has an **always Free tier** that includes **1 million** requests per month.
- **Understand**: **Fargate** has no **upfront costs**. Payonly for the **resources used**.

## Additional Compute Services
### Outposts [![AWS Outposts](https://icon.icepanel.io/AWS/svg/Compute/Outposts-rack.svg)](https://docs.aws.amazon.com/outposts/)
- **AWS Outposts**  - is a fully managed service that extends AWS infrastructure, services, and tools to virtually any datacenter, co-location space, or on-premises facility for a truly consistent hybrid experience.

### Lightsail [![AWS Lightsail](https://icon.icepanel.io/AWS/svg/Compute/Lightsail.svg)](https://docs.aws.amazon.com/lightsail/index.html)
- **Amazon Lightsail** - is the easiest way to get started with AWS for developers who just need virtual private servers. Lightsail includes everything you need to launch your project quickly - a virtual machine, SSD-based storage, data transfer, DNS management, and a static IP - for a low, predictable price.

### Batch [![AWS Batch](https://icon.icepanel.io/AWS/svg/Compute/Batch.svg)](https://docs.aws.amazon.com/batch/index.html)
- **AWS Batch** - enables developers, scientists, and engineers to easily and efficiently run hundreds of thousands of batch computing jobs on AWS. AWS Batch dynamically provisions the optimal quantity and type of compute resources (e.g., CPU or memory-optimized instances) based on the volume and specific requirements of the batch jobs submitted.

### Wavelegth [![AWS Wavelegth](https://icon.icepanel.io/AWS/svg/Compute/Wavelength.svg)](https://docs.aws.amazon.com/wavelength/index.html)
- **AWS Wavelength** - brings AWS services to the edge of the 5G network, minimizing the latency to connect to an application from a mobile device. Wavelength embeds AWS compute and storage services at the edge of telecommunications providers' 5G networks.

### Additional Compute Services Quick Quiz!
#### **You need to select a service to implement a quick deployment of a small temporary test environment. What service can you use to accomplish this?**
<details>
  <summary>Answer</summary>
    <b>Lightsail</b> is perfect for quick launches of small projects like test environments or preconfigured WordPress websites.
</details>

#### **You need to suggest a service that will allow your data to reside in your data center and support a hybrid deployment model. What can you use to do this?**
<details>
  <summary>Answer</summary>
    <b>Outpost</b> provide low latency and meet data residency or sovereighty regulations while still supporting a hybrid deployment model.
</details>

### Additional Compute Services Exam Tips
- **Outposts** support hybrid deployment models.
- **Lightsail** is a compute service used to **quickly launch small projects**.
- **Batch** is a compute service that processes **large workloads** in **smaller batches**.
- **Wavelength** allows users to reach application servers **without leaving** the **5G mobile network**.