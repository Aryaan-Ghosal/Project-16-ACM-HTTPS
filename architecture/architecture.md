# Project 16 Architecture
## Request Flow
Internet Client
   |
   | HTTPS :443
   v
Application Load Balancer
   |
   | TLS termination using ACM certificate
   |
   | HTTP :80
   v
Target Group
   |
   v
EC2 Ubuntu 24.04
   |
   v
Apache Web Server
## Network
VPC: 10.16.0.0/16
- Public subnet 1: 10.16.1.0/24 (ap-northeast-1a)
- Public subnet 2: 10.16.2.0/24 (ap-northeast-1c)
- Internet Gateway
- Public route table
## Security
- ALB accepts HTTPS on TCP 443.
- EC2 accepts HTTP on TCP 80 from the ALB security group.
- SSH was restricted to the administrator IP during setup.
- Systems Manager was used for instance administration.
## Certificate
A self-signed certificate was imported into ACM. It was not an ACM-issued public certificate.
