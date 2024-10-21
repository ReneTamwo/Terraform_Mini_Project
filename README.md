This project uses Terraform to deploy AWS infrastructure by leveraging reusable modules for security groups, EC2 instances, EBS volumes, and Elastic IPs (EIP). 
Each module manages a specific AWS resource, making the configuration modular and scalable.

Project Structure:
Security Group (SG): Defines firewall rules (inbound/outbound traffic) using dynamic ingress rules.
EBS Volume: Creates an Elastic Block Store (EBS) volume with configurable size and availability zone.
Elastic IP (EIP): Allocates an elastic IP to associate with an EC2 instance.
EC2 Instance: Deploys an EC2 instance running Ubuntu, with NGINX installed and accessible via SSH and HTTP.

Modules Overview:
SG Module: Configures security groups with allowed ports (default: 80, 22, 443).
EBS Module: Creates a volume with customizable disk size and tags.
EIP Module: Allocates an elastic IP in the VPC domain.
EC2 Module: Launches an EC2 instance with a public IP and connects the security group, EBS volume, and elastic IP.
