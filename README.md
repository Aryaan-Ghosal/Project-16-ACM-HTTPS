
# Project 16 – Enable HTTPS Using AWS Certificate Manager

## Objective

Configure HTTPS access to an Apache web application hosted on EC2 using an Application Load Balancer and AWS Certificate Manager.

## AWS Services

- Amazon VPC

- Internet Gateway

- Public Subnets

- Amazon EC2

- Security Groups

- AWS Systems Manager

- AWS Certificate Manager

- Application Load Balancer

- Target Groups

## Architecture

Client → HTTPS (443) → ALB → HTTP (80) → Target Group → EC2 Apache

## Implementation

1. Created a dedicated VPC and two public subnets.

2. Configured internet routing through an Internet Gateway.

3. Launched Ubuntu EC2 and installed Apache.

4. Configured Systems Manager access.

5. Generated a self-signed certificate and imported it into ACM.

6. Created an Application Load Balancer and target group.

7. Configured an HTTPS listener on port 443.

8. Tested HTTPS connectivity using curl.

## Certificate Disclaimer

The certificate was self-signed and imported into ACM. It was not publicly issued by ACM and is not automatically trusted by browsers. HTTPS testing used curl -k to skip certificate validation.

See docs/Project-16-Documentation.md for implementation details and interview questions.

