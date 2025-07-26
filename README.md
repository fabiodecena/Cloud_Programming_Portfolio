# Cloud Programming Portfolio

A comprehensive AWS cloud infrastructure project that demonstrates the implementation of a scalable web architecture using Infrastructure as Code (IaC) with Terraform/OpenTofu.

## 🏗️ Infrastructure Overview

This project deploys:

- **VPC Network Architecture**
    - Custom VPC with public subnets
    - Internet Gateway and routing configuration
    - Multi-AZ deployment for high availability

- **Web Hosting Infrastructure**
    - S3 static website hosting
    - CloudFront CDN distribution
    - Auto-scaling EC2 web servers
    - Application Load Balancer (ALB)

- **Security**
    - Configured security groups
    - Public/private network segmentation
    - SSL/TLS support via CloudFront

## 🚀 Getting Started

### Prerequisites

- AWS Account
- Terraform installed
- AWS CLI configured with appropriate credentials

### Quick Start

1. Clone the repository

2. Initialize Terraform

3. Deploy the infrastructure

## 🛠️ Features

### Network Layer
- VPC with custom CIDR block
- Public subnets across multiple availability zones
- Automated routing configuration

### Application Layer
- Auto Scaling Group of EC2 instances
- Apache web server pre-configured via user data
- Health checks and dynamic scaling
- Application Load Balancer for traffic distribution

### Content Delivery
- S3 bucket for static content hosting
- CloudFront distribution for global content delivery
- Support for HTML and image content

### Security
- Isolated network segments
- Controlled inbound access
- Security group rules for ALB and EC2 instances

## 🔧 Configuration

The infrastructure can be customized through variables in `variables.tf`:

- Environment name
- VPC CIDR range
- Availability zones
- Instance types and capacities
- Auto-scaling parameters

## 📝 Architecture Details

- **EC2 Instances**: t2.micro running Amazon Linux 2
- **Auto Scaling**: Maintains 2 instances (min: 1, max: 4)
- **Load Balancer**: Application Load Balancer with HTTP support
- **Storage**: S3 with public website hosting
- **CDN**: CloudFront with default SSL certificate

## 🔐 Security Considerations

1. All EC2 instances are placed in public subnets with security groups
2. ALB accepts traffic on ports 80/443
3. EC2 instances only accept traffic from ALB
4. S3 bucket configured for website hosting with public read access
5. CloudFront provides additional security layer

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

free license

## ✨ Author

Fabio De Cena

---
For more information or questions, please open an issue in the repository.
