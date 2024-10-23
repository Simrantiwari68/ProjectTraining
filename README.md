# AWS Three Tier Web Architecture Workshop

## Description: 
This workshop is a hands-on walk through of a three-tier web architecture in AWS. We will be manually creating the necessary network, security, app, and database components and configurations in order to run this architecture in an available and scalable manner.

## Audience:
Although this is an introductory level workshop, it is intended for those who have a technical role. The assumption is that you have at least some foundational aws knowledge around VPC, EC2, RDS, S3, ELB and the AWS Console.  

## Pre-requisites:
1. An AWS account. If you don’t have an AWS account, follow the instructions [here](https://aws.amazon.com/console/) and
click on “Create an AWS Account” button in the top right corner to create one.
1. IDE or text editor of your choice.

## Architecture Overview
![Architecture Diagram](https://github.com/aws-samples/aws-three-tier-web-architecture-workshop/blob/main/application-code/web-tier/src/assets/3TierArch.png)

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

## Workshop Instructions:

See [AWS Three Tier Web Architecture](https://catalog.us-east-1.prod.workshops.aws/workshops/85cd2bb2-7f79-4e96-bdee-8078e469752a/en-US)


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.









## DAILY DIARY
# AWS Training: Daily Progress Diary (30 Days)

## Introduction
This repository documents my daily progress over a one-month AWS training program. The goal is to deepen my understanding of AWS cloud infrastructure and services, and to build hands-on experience through various labs and projects.

---

### Week 1: Foundations of AWS Cloud

#### Day 1: Introduction to AWS & Cloud Computing
- Topic:** Overview of Cloud Computing and AWS.
Key Concepts Learned: Cloud computing models (IaaS, PaaS, SaaS), AWS global infrastructure.
Hands-on Activity: Signed up for an AWS Free Tier account, explored the AWS Management Console.

#### Day 2: EC2 (Elastic Compute Cloud) Basics
Topic: Introduction to EC2, instance types, and pricing models.
Key Concepts Learned: EC2 instances, On-Demand, Reserved, and Spot instances.
Hands-on Activity: Launched an EC2 instance, connected via SSH.

#### Day 3: EC2 Configuration and Management
- **Topic:** EC2 security groups, key pairs, and AMIs.
- **Key Concepts Learned:** Security group rules, AMI creation, Elastic IPs.
- **Hands-on Activity:** Created a custom AMI, set up security groups, and assigned an Elastic IP.

#### Day 4: AWS Identity and Access Management (IAM)
- **Topic:** IAM users, groups, roles, and policies.
- **Key Concepts Learned:** Best practices for managing access to AWS resources.
- **Hands-on Activity:** Created IAM roles, groups, and users with specific policies.

#### Day 5: Elastic Block Store (EBS) and Snapshots
- **Topic:** EBS volumes, types, and snapshots.
- **Key Concepts Learned:** How to create and manage EBS volumes and snapshots for backup.
- **Hands-on Activity:** Attached EBS volumes to EC2, created snapshots for backup.

#### Day 6: Simple Storage Service (S3) Basics
- **Topic:** Introduction to S3, bucket creation, object storage.
- **Key Concepts Learned:** S3 buckets, object storage, and permissions.
- **Hands-on Activity:** Created and managed S3 buckets, set up versioning and lifecycle policies.

#### Day 7: S3 Security and Permissions
- **Topic:** S3 policies, ACLs, and encryption.
- **Key Concepts Learned:** Bucket policies, encryption mechanisms (SSE, KMS).
- **Hands-on Activity:** Configured S3 bucket policies and set up server-side encryption.

---

### Week 2: Networking & Database Services

#### Day 8: Virtual Private Cloud (VPC)
- **Topic:** Introduction to VPC, subnets, and internet gateways.
- **Key Concepts Learned:** Subnetting, route tables, and NAT gateways.
- **Hands-on Activity:** Set up a custom VPC with public and private subnets, attached an internet gateway.

#### Day 9: VPC Security & Peering
- **Topic:** Security groups vs NACLs, VPC peering.
- **Key Concepts Learned:** Network security with security groups and NACLs, VPC peering.
- **Hands-on Activity:** Configured NACLs, set up a VPC peering connection between two VPCs.

#### Day 10: Relational Database Service (RDS)
- **Topic:** Introduction to RDS, supported databases, and pricing models.
- **Key Concepts Learned:** RDS databases (MySQL, PostgreSQL, etc.), backups, and snapshots.
- **Hands-on Activity:** Launched an RDS instance, connected it to an EC2 instance.

#### Day 11: RDS Security and Backups
- **Topic:** RDS security groups, automated backups, and snapshots.
- **Key Concepts Learned:** Securing RDS instances, creating manual backups.
- **Hands-on Activity:** Configured security groups, set up automatic backups and snapshots.

#### Day 12: Amazon Route 53 - DNS and Domain Management
- **Topic:** Introduction to Route 53, DNS routing policies.
- **Key Concepts Learned:** DNS basics, routing policies (simple, weighted, failover).
- **Hands-on Activity:** Registered a domain with Route 53, set up DNS records for EC2 instances.

#### Day 13: High Availability with Auto Scaling
- **Topic:** Auto Scaling groups and policies.
- **Key Concepts Learned:** Launch configurations, scaling policies.
- **Hands-on Activity:** Set up Auto Scaling for an EC2 instance, tested scaling in/out.

#### Day 14: Load Balancing with ELB
- **Topic:** Elastic Load Balancing (ELB), types of load balancers.
- **Key Concepts Learned:** Application Load Balancer (ALB), Network Load Balancer (NLB).
- **Hands-on Activity:** Set up an ALB to distribute traffic between multiple EC2 instances.

---

### Week 3: Advanced AWS Services

#### Day 15: S3 Lifecycle and Glacier Storage
- **Topic:** S3 lifecycle rules, Glacier storage.
- **Key Concepts Learned:** Transitioning data between S3 and Glacier for cost efficiency.
- **Hands-on Activity:** Configured lifecycle policies to move objects from S3 to Glacier.

#### Day 16: CloudFront and CDN
- **Topic:** Content Delivery Networks (CDN) with CloudFront.
- **Key Concepts Learned:** Distributing content globally using CloudFront.
- **Hands-on Activity:** Set up a CloudFront distribution for an S3 bucket.

#### Day 17: Monitoring with CloudWatch
- **Topic:** Introduction to CloudWatch, metrics, and alarms.
- **Key Concepts Learned:** CloudWatch metrics, setting up alarms.
- **Hands-on Activity:** Created custom CloudWatch dashboards and set up alarms for EC2 instances.

#### Day 18: AWS Lambda and Serverless Computing
- **Topic:** Introduction to AWS Lambda, triggers, and execution.
- **Key Concepts Learned:** Serverless architecture, Lambda functions.
- **Hands-on Activity:** Created a Lambda function triggered by S3 events.

#### Day 19: AWS API Gateway
- **Topic:** Introduction to API Gateway, creating and deploying APIs.
- **Key Concepts Learned:** Setting up REST APIs with API Gateway, integration with Lambda.
- **Hands-on Activity:** Created a REST API using API Gateway and integrated it with a Lambda function.

#### Day 20: AWS CloudFormation
- **Topic:** Infrastructure as Code (IaC) with CloudFormation.
- **Key Concepts Learned:** CloudFormation templates, stacks.
- **Hands-on Activity:** Created a CloudFormation stack to provision EC2 and RDS resources.

#### Day 21: Elastic Beanstalk for App Deployment
- **Topic:** Introduction to Elastic Beanstalk, deploying applications.
- **Key Concepts Learned:** Deploying web apps with Elastic Beanstalk.
- **Hands-on Activity:** Deployed a Node.js application using Elastic Beanstalk.

---

### Week 4: Security, Cost Management, and Final Project

#### Day 22: AWS Security Best Practices
- **Topic:** Security best practices in AWS.
- **Key Concepts Learned:** AWS shared responsibility model, best practices for securing AWS accounts.
- **Hands-on Activity:** Enabled MFA for root and IAM users, reviewed IAM roles and policies.

#### Day 23: AWS Config and Compliance
- **Topic:** Introduction to AWS Config and compliance checks.
- **Key Concepts Learned:** Monitoring AWS resource configurations for compliance.
- **Hands-on Activity:** Set up AWS Config rules to monitor non-compliant resources.

#### Day 24: Cost Management with AWS Budgets and Cost Explorer
- **Topic:** Managing costs with AWS Budgets and Cost Explorer.
- **Key Concepts Learned:** Budget creation, using Cost Explorer for insights.
- **Hands-on Activity:** Created a budget to monitor and alert on AWS spending.

#### Day 25: Final Project Planning
Topic: Designing a final project using multiple AWS services.
Key Concepts Learned:Project planning, service selection.
Hands-on Activity: Drafted a project plan to use EC2, S3, RDS, and CloudFront.

#### Day 26: Final Project Implementation - Part 1
Topic: EC2, S3, and RDS integration.
*Key Concepts Learned: Integrating multiple AWS services.
Hands-on Activity:Deployed an application with EC2, connected to an RDS instance, and set up S3 for static file storage.

#### Day 27: Final Project Implementation - Part 2
Topic: CloudFront and Auto Scaling.
Key Concepts Learned: Adding CloudFront and Auto Scaling for performance and high availability.
Hands-on Activity: Integrated CloudFront with S3, set up Auto Scaling for the EC2 instances.

#### Day 28: Final Project Implementation - Part 3
Topic: Monitoring and Security.
Key Concepts Learned: CloudWatch monitoring, IAM security practices.
Hands-on Activity: Added CloudWatch metrics and alarms, reviewed IAM roles for least privilege access.

#### Day 29: Final Project Testing and Review
Topic: Testing and refining the final project.
Key Concepts Learned: Application testing and optimization.
Hands-on Activity: Performed load testing, optimized application performance, and fixed security issues.

#### Day 30: Final Project Presentation and Documentation
Topic: Final project documentation and GitHub upload.
 Key Concepts Learned: Writing documentation, sharing projects on GitHub.
Hands-on Activity: Uploaded final project code and documentation to GitHub.



## Conclusion
After a month of intensive AWS training, I



