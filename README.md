### NAME: SURYA P <br>
### REG NO: 212224230280 <br> 
### Date: 16/02/2026

## EX. No. 2 : Build a VPC and launching a webserver
---
## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)


1. Log in to the AWS Management Console and create a new VPC with CIDR block 10.0.0.0/16.
2. Create a public subnet (10.0.1.0/24) inside the VPC, enable auto-assign public IP, create and attach an Internet Gateway,  and configure a Route Table with a default route (0.0.0.0/0) to the Internet Gateway.
3. Create a Security Group allowing inbound traffic on port 22 (SSH) and port 80 (HTTP).
4. Launch an EC2 instance (Amazon Linux 2, t2.micro) in the public subnet and attach the Security Group and key pair.
5. Connect to the EC2 instance, install and start the Apache web server, create a simple HTML page, and verify the web server using the public IP address in a browser.---

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1246" height="355" alt="image" src="https://github.com/user-attachments/assets/5ad198f3-bbfb-4265-a7c4-02a266470395" />

---

### Screenshot 2: EC2 Instance Running

<img width="1250" height="390" alt="image" src="https://github.com/user-attachments/assets/2ff2a50f-5f5d-4b59-8099-388f249c3ed3" />

---

### Screenshot 3: Web Server Output in Browser

<img width="1131" height="443" alt="image" src="https://github.com/user-attachments/assets/29b3bd67-3118-42e5-a5e2-817c67e8780e" />

---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
