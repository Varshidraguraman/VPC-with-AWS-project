# VPC Project

This project demonstrates the setup of a Virtual Private Cloud (VPC) on AWS with public and private subnets, an internet gateway, and a web server running in the public subnet with an HTML file.

## Project Overview

In this project, I created a VPC with the following configuration:
- **VPC**: Virtual network infrastructure.
- **Public Subnet**: Hosts resources that are accessible from the internet.
- **Private Subnet**: Hosts resources that are not directly accessible from the internet.
- **Internet Gateway**: Allows communication between the public subnet and the internet.
- **Route Tables**: Configure routing between subnets and the internet gateway.

I also created an **HTML file** that is served by a web server in the public subnet. The public subnet is accessible from the internet, and the private subnet is used for secure backend operations.

## Steps Taken in the Project

1. **Set Up AWS VPC**:
   - Created a new **VPC** in AWS with CIDR block `10.0.0.0/16`.
   - Created two subnets:
     - **Public Subnet** (e.g., `10.0.1.0/24`)
     - **Private Subnet** (e.g., `10.0.2.0/24`)

2. **Internet Gateway (IGW)**:
   - Created and attached an **Internet Gateway** (IGW) to the VPC.
   - Configured the route table for the public subnet to route internet traffic via the IGW.

3. **Launch Web Server**:
   - Launched an **EC2 instance** (Ubuntu/Linux) in the public subnet.
   - Installed a simple web server (Apache or Nginx).
   - Placed an **HTML file** in `/var/www/html/` on the server to serve as the website.

4. **Route Tables Configuration**:
   - Associated the **public subnet** route table with the IGW to allow internet access.
   - Configured the **private subnet** to route internal traffic only.

5. **Security Groups & Networking**:
   - Configured security groups to allow HTTP traffic on port 80 for the web server.
   - Ensured the private subnet's resources (such as databases) were not exposed to the internet.

## How to Access the Project

1. Launch the project using your AWS account (if needed).
2. Ensure that the EC2 instance in the public subnet is running and accessible via the public IP address.
3. Visit the public IP in your browser to view the HTML file being served by the server.

## Tools and Technologies Used

- **AWS VPC**: Virtual Private Cloud for network isolation.
- **AWS EC2**: Elastic Compute Cloud for hosting the web server.
- **Apache Web Server**: For serving the HTML file.
- **HTML**: For the webpage content.
- **Security Groups**: For controlling traffic flow.

## Project Demo

You can view a live demo of the project here:  
[Your LinkedIn or Project Link](https://www.linkedin.com)

##Thanks for watching 
