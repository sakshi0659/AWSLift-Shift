# ☁️ Lift-and-Shift Application Workload on AWS

## 📘 Overview
This project demonstrates a *Lift and Shift migration strategy* for a multi-tier web application stack — migrating workloads from a traditional data center to the *AWS Cloud*.  
The goal is to modernize infrastructure with *IaaS, enabling **automation, cost efficiency, and operational simplicity*.

---
## ❗ Problem Statement
Traditional on-premises applications often face challenges such as limited scalability, high maintenance costs, hardware dependency, and manual infrastructure management. These issues lead to poor agility, downtime during peak loads, and complex operational overhead.

## 💡 Solution
To overcome these challenges, the application workload was *migrated to AWS using a Lift-and-Shift approach*.  
By rehosting existing virtual machines onto *Amazon EC2* and integrating *Elastic Load Balancing, **Auto Scaling, and **S3 storage*, the solution achieves:
- *High availability* and *fault tolerance*  
- *Automated scaling* during traffic fluctuations  
- *Reduced operational complexity*  
- *Improved cost efficiency* and *cloud-based flexibility*  

This enables a smoother transition to the cloud with minimal architectural change while leveraging the core benefits of AWS infrastructure.

---

### 🎯 Objective
Migrate a traditional, data-center-hosted multi-tier application to *AWS*, ensuring:
- High Availability  
- Fault Tolerance  
- Scalability  
—all with *minimal architectural change*.

---

### 🚚 Lift-and-Shift Approach
- Migrate compute workloads to *Amazon EC2 Instances*  
- Use *Elastic Load Balancer (ELB)* for intelligent traffic distribution  
- Implement *Auto Scaling Groups* for dynamic resource scaling  
- Store static content and backups in *Amazon S3*  
- Manage DNS using *Amazon Route 53*  
- Secure setup via *Key Pairs* & *Security Groups*

---

## 🧩 AWS Services Used

| *Service* | *Purpose* |
|--------------|-------------|
| *EC2* | Host web and application servers |
| *Elastic Load Balancer (ELB)* | Distribute incoming traffic for high availability |
| *Auto Scaling Group* | Automatically scale compute resources |
| *S3 (Simple Storage Service)* | Store static content, backups, and deployment artifacts |
| *Route 53* | Manage domain names & DNS (integrated with GoDaddy) |
| *EFS (Elastic File System)* | Provide shared storage across EC2 application servers (optional) |

---
## 🏗️ Architecture

The project follows a *three-tier Lift-and-Shift architecture* — consisting of the web tier, application tier, and database tier — migrated from an on-premises environment to AWS.

### 🧱 Architecture Description
- *Web Tier:* Hosted on EC2 instances behind an *Elastic Load Balancer (ELB)* to evenly distribute incoming HTTP/HTTPS traffic.  
- *Application Tier:* Runs business logic on EC2 instances within an *Auto Scaling Group*, ensuring high availability and elasticity based on load.  
- *Database Tier:* Can be migrated to *Amazon RDS* (for managed relational databases) or remain on EC2 for a true lift-and-shift approach.  
- *Storage:* Static files, logs, and backups are stored securely in *Amazon S3*.  
- *Networking:* All resources are deployed within a *VPC* with *public and private subnets, **Internet Gateway, and **NAT Gateway* for controlled access.  
- *DNS Management:* *Amazon Route 53* maps the custom domain to the ELB endpoint for seamless access.  
- *Security:* Enforced through *Security Groups, **IAM roles, and **Key Pairs* ensuring least-privilege access.

### 🗺️ Data Flow
1. User requests hit the *Elastic Load Balancer (ELB)*.  
2. ELB routes traffic to healthy *EC2 web/application instances*.  
3. Application instances access data from the *database tier* or static files in *S3*.  
4. Auto Scaling automatically adds or removes instances based on demand.  
5. DNS resolution and traffic routing are managed by *Route 53*.

This architecture ensures *scalability, high availability, and fault tolerance* while preserving the legacy application’s original design — achieving true Lift-and-Shift migration.


--- 
## ⚙️ Architecture Diagram  

![Architecture Diagram](https://github.com/user-attachments/assets/c27ded08-d444-44d0-aa36-8d36401502b7)

---

## 🚀 Key Learnings
- Hands-on implementation of *Lift-and-Shift migration* on AWS  
- Configured *load balancing, **auto scaling, **DNS, and **secure networking*  
- Gained practical exposure to *fault-tolerant, **cost-optimized* cloud setups  
- Understood enterprise-level *migration workflows*

---

## 🧾 Future Improvements
- Integrate *Amazon CloudWatch* for monitoring and alerting  
- Add *Amazon CloudFront* for faster edge content delivery  
- Automate provisioning using *CloudFormation, **CDK, or **Terraform*  
- Enhance *CI/CD* pipelines with improved automation  

---

## 🔗 Project Links
💼 *LinkedIn Post:*  https://www.linkedin.com/posts/sakshisharma48_aws-cloudcomputing-liftandshift-activity-7370149757861867520-NXks  


---

## 💬 About the Project
This project presents a *scalable, production-ready AWS environment* for hosting legacy workloads.  
It represents a *real-world enterprise migration path, maintaining **security, **reliability, and **modern cloud standards*.

---

## 👩‍💻 Author
*Sakshi Sharma*  
📫 [Connect on LinkedIn] : www.linkedin.com/in/sakshisharma48
