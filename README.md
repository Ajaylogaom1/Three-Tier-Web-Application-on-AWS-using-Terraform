# Three-Tier Web Application Deployment on AWS using Terraform

An end-to-end Three-Tier E-Commerce Web Application deployed on AWS using Terraform, Docker, Nginx, Amazon EC2 and Amazon RDS (MySQL).

This project demonstrates Infrastructure as Code (IaC), cloud infrastructure provisioning, containerization and deployment of a web application using AWS services.


## Technologies Used

| Technology | Purpose |
|---|---|
| AWS | Cloud infrastructure |
| Terraform | Infrastructure as Code |
| Amazon EC2 | Application hosting |
| Amazon RDS | Managed MySQL database |
| Amazon VPC | Network isolation |
| Security Groups | Network traffic control |
| Docker | Application containerization |
| Docker Compose | Container orchestration |
| Nginx | Reverse proxy |
| Python Flask | Backend application |
| MySQL | Database |
| Git & GitHub | Version control |

## Project Overview

The objective of this project is to deploy a three-tier web application on AWS while automating infrastructure provisioning using Terraform.

The application and infrastructure code are maintained in a single GitHub repository.

### Application Architecture

**1. Presentation Layer**
- Nginx web server.
- Handles incoming HTTP requests.
- Routes requests to the backend application.

**2. Application Layer**
- Python Flask application.
- Handles business logic and user requests.
- Communicates with the database.

**3. Database Layer**
- Amazon RDS MySQL.
- Stores application data.
- Hosted separately from the application EC2 instance.

##  AWS Infrastructure

The infrastructure is provisioned using Terraform.

Main components:

- AWS VPC for network isolation.
- EC2 instance for hosting the application.
- Amazon RDS MySQL for database management.
- Security Groups for controlling network access.
- Networking resources required for application and database connectivity.

## Repository Structure

```text
Three-Tier-Web-Application-on-AWS-using-Terraform/
│
├── application/
│   ├── app.py
│   ├── config.py
│   ├── models.py
│   ├── dockerfile
│   ├── docker-compose.yml
│   ├── nginx/
│   ├── static/
│   ├── templates/
│   └── requirements.txt
│
├── aws-terraform-infrastructure/
│   └── Terraform infrastructure files
│
└── README.md
```

## Deployment Workflow

1. Write Terraform configuration files.
2. Initialize Terraform using `terraform init`.
3. Validate infrastructure configuration.
4. Review the execution plan using `terraform plan`.
5. Provision AWS infrastructure using `terraform apply`.
6. Connect to the EC2 instance using SSH.
7. Install and configure Docker.
8. Clone the application repository or use the application code.
9. Configure the application environment variables with RDS connection details.
10. Build and start containers using Docker Compose.
11. Access the deployed application using the EC2 public endpoint.

##  Terraform Commands

Navigate to the Terraform infrastructure directory:

```bash
cd aws-terraform-infrastructure
```

Initialize Terraform:

```bash
terraform init
```

Validate Terraform configuration:

```bash
terraform validate
```

Review the infrastructure plan:

```bash
terraform plan
```

Create AWS infrastructure:

```bash
terraform apply
```

Destroy infrastructure when it is no longer required:

```bash
terraform destroy
```


## Docker Deployment

Navigate to the application directory:

```bash
cd application
```

Build and start the containers:

```bash
docker compose up -d --build
```

Check running containers:

```bash
docker ps
```

View container logs:

```bash
docker compose logs
```

Stop the containers:

```bash
docker compose down
```

##  Security Considerations

- Keep AWS credentials outside the repository.
- Use environment variables for database credentials.
- Never commit `.env` files or private SSH keys.
- Restrict SSH access using Security Groups.
- Allow database access only from the application security group.
- Avoid exposing the RDS database publicly.
- Use least-privilege IAM permissions.


## Key Learnings

By completing this project, I gained hands-on experience in:

- Provisioning AWS infrastructure using Terraform.
- Understanding AWS VPC and networking.
- Deploying applications on EC2.
- Connecting EC2-hosted applications to Amazon RDS.
- Containerizing applications using Docker.
- Managing multiple containers using Docker Compose.
- Configuring Nginx as a reverse proxy.
- Managing cloud infrastructure through Infrastructure as Code.
- Deploying and troubleshooting cloud-hosted applications.


## Author

**Ajay**

Aspiring DevOps / Cloud Engineer

GitHub: [Ajaylogaom1](https://github.com/Ajaylogaom1)

---
