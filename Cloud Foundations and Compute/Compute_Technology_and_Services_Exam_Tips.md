# Compute Technology and Services Exam Tips

## Review Time!
- **EC2 Pricing Options**
    - **On-Demand Instances**: There is no upfront payment. Pay for what you use.
    - **Spot Instances**: Bid for unused EC2 capacity, can save up to 90%.
    - **Dedicated Hosts**: A physical EC2 server dedicated to your use can help meet compliance requirements.

    - **Reserved Instances**: Reserved capacity for 1 or 3 years, significant discount.
    - **Saving Plans**: Commit to consistent usage over 1 or 3 years with a significant discount.

- **Real-World Uses for EC2***:
    - **Application**: Run web applications, mobile backends, etc.

    - **Database**: Run databases like MySQL, PostgreSQL, etc.

- **Scaling Types and Benefits**
    - **Vertical Scaling**: Increase the size of the instance.
    - **Horizontal Scaling**: Increase the number of instances.
    
    - **Benefits**: High availability, fault tolerance, cost-effectiveness, and performance.

- **Load Balancers**
    - **Classic Load Balancer (CLB)**: Layer 4, supports TCP and SSL and supports sticky sessions.

    - **Gateway Load Balancer (GWLB)**: Layer 3, supports static IP addresses and supports routing to multiple ports.

    - **Application Load Balancer (ALB)**: Layer 7, intelligent routing, and supports path-based routing.

    - **Network Load Balancer (NLB)**: Layer 4, high performance, and supports static IP addresses.

- **How to Connect to an EC2 Instance**
    - **Console**: Browser-based SSH connection.
    
    - **Instance Connect**: Browser-based SSH connection.
    - **SSH**: Command-line SSH connection.
        - **How the key pair utilized with ssh access**
    - **Session Manager**: Browser-based SSH connection.

- **ECS vs. EKS**
    - **ECS**: Amazon Elastic Container Service managed by AWS and supports Docker.
    
    - **EKS**: Amazon Elastic Kubernetes Service, a fully managed open-source system, supports Kubernetes.

- **Think Containers for**:
    - **Lift and Shift**: Migrate applications to the cloud.
    
    - **Microservices**: Break applications into smaller services.
    - **CI/CD**: Automate the software delivery process.
    - **Refactoring applications**: Improve the application's performance.

- **Serverless**
    - **You are Responsible for code only!**
    
    - **Fargate** is considered serverless and is used to manage containers.
    - **Fargate** has no **upfront costs**. Pay only for **resources used**.
    - **Fargate** is **fully managed** and **scales automatically**.
    - **Lambda** has an always-free tier with 1M free monthly requests.
    - **Lambda** supports multiple languages like Node.js, Python, Java, etc.
    - **Lambda** has a maximum execution time of 15 minutes.
    - **Lambda** can be triggered by multiple services like S3, DynamoDB, etc.
    
- **Additional Compute Services**
    - **Outposts** support **Hybrid** deployment models.
    
    - **Lightsail** us used to **quickly launch small projects**.
    - **Batch** processes **large workloads** in **smaller batches**.
    - **Wavelenght** allows users to reach application servers **without leaving** the **5G mobile network**.
