# AWS-Assignment

In the current Project, we have following AWS structure,
- 1 custom VPC 
- 4 Subnet with 2 public and 2 private.
- Public subnet hosts LB and EC2 bastion host.
- Private Subnet is having the Web Server Instances with outgoing only internet access. It has the EBS volume mounted /var/log to have the logs on it and also the volume is encrypted.
- 3 security gp, 1 for Bastion host allowing ssh only from defined IP range, 1 Web server Instance allowing ssh from bastion sg only and HTTP traffic on port 80 from LB security group, and LB security gp with access tp pulic on port 80.
- 1 LC with the Web server configurations and user data to run the Web server application.
- 1 ASG to manage the Application server Instance.
- Load balancer to access the Web application GUI.

# Configurable items are as below-

- Web server Instance type
- Bastion Instancce type
- Key pair to login
- Number of Web server instance needed at the start time of creation
- VPC CIDR
- 2 Public Subnet CIDR
- 2 Private Subnet CIDR
- IP Range who will be able to login to Bastion host
