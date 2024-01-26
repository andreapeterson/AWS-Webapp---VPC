# AWS-Webapp---VPC
Secure Web Application Hosting in AWS VPC with Bastion Host and ELB.

![IMG_584B9AB6B83D-1](https://github.com/andreapeterson/AWS-Webapp---VPC/assets/134665743/a6e2871a-2bf0-41b5-932b-67e7f1de2bd6)

In this project, my main goal was to get hands-on with best practices for security in separating public-facing components from private ones. I created my own private VPC with 4 subnets in two availability zones. I created two route tables, one for the public subnets that allows internal traffic and traffic to the internet gateway, and one for the private subnets that allow internal traffic and traffic to the NAT gateway. It also includes 3 security groups: one for the bastion host in subnet B(ssh access from my IP), the ELB in public subnet B (http&https access), and one for the 2 private instances(only inbound access from the other 2 security groups). The private instance, web01, runs my webpage and is secure, only accessible from the ELB and Bastion host security group!
