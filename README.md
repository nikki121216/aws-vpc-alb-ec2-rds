# aws-vpc-alb-ec2-rds
AWS VPC Production Style Architecture

This repository documents a hands on implementation of a secure AWS network architecture.

Architecture Overview

VPC with custom CIDR
Public subnet hosting Application Load Balancer
Private subnet hosting EC2 web servers
Private subnet hosting RDS database
NAT Gateway for outbound internet access
Bastion Host for secure SSH access
Security Group chaining for controlled traffic flow

Traffic Flow

Internet -> ALB (public subnet)
ALB -> EC2 (private subnet)
EC2 -> RDS (private subnet)
Private instances access internet via NAT Gateway
SSH access only via Bastion Host

Security Practices Used

No public IP on EC2 or RDS
Inbound access restricted using security groups
Database accessible only from application layer
No open ports to the internet

Validation

ALB health checks working
EC2 accessible only through ALB
RDS not publicly accessible
Outbound internet confirmed via NAT Gateway

This setup was deployed manually on AWS console for learning real world cloud networking.
