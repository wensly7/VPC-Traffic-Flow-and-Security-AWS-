<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-security)

**Author:** Narte, Wensly Anthony  
**Email:** wenslynarte@gmail.com

---

## VPC Traffic Flow and Security

![Image](http://nextwork.ai/sympathetic_brown_vibrant_date/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

I would use EC2 Global View when I need to monitor and manage EC2 and VPC resources across multiple AWS Regions. It helps me quickly find resources from one dashboard instead of switching between Regions, making resource management more organized and efficient.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to build a private network in AWS where I could organize and manage my cloud resources. I created a VPC, subnets, a route table, a security group, and a Network ACL to control network traffic, provide internet access, and improve the security of the network.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how many components are needed to make a VPC work properly. I thought creating a VPC was enough, but I learned that route tables, security groups, and Network ACLs all have different roles in controlling traffic and securing the network.

### This project took me...

This project took me almost two to three hours.

---

## Route tables

A route table works like a map or GPS for network traffic. It decides the path that data should take so it reaches the correct destination. For example, if a resource in a public subnet needs internet access, the route table directs its traffic to the internet gateway.

You need a route table to make a subnet public because it tells network traffic how to reach the internet. By adding a route to an internet gateway, resources in the public subnet can send and receive internet traffic. Without a route table, the subnet cannot access the internet even if an internet gateway is attached to the VPC.

![Image](http://nextwork.ai/sympathetic_brown_vibrant_date/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

The destination is where the network traffic is going, while the target is the resource that directs the traffic to that destination, such as an internet gateway or another network.

My new route's destination is 0.0.0.0/0, which means all internet traffic, and its target is the Internet Gateway (IGW), allowing resources in the public subnet to access the internet.

![Image](http://nextwork.ai/sympathetic_brown_vibrant_date/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are virtual firewalls that protect AWS resources, such as EC2 instances. They control which network traffic is allowed to enter or leave a resource by using rules based on IP addresses, protocols, and port numbers.

### Inbound vs Outbound rules

An inbound rule controls the traffic that is allowed to enter a resource. In my project, the security group's inbound rules did not allow any traffic by default, unless I added a rule to permit specific access.

An outbound rule controls the traffic that is allowed to leave a resource. In my project, the default outbound rule allowed all outbound traffic, so the resource could communicate with other networks or the internet.

![Image](http://nextwork.ai/sympathetic_brown_vibrant_date/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs (Network Access Control Lists) are a security feature in AWS that control incoming and outgoing traffic for an entire subnet in a VPC. They work by using rules to allow or deny traffic based on IP addresses, protocols, and port numbers.

### Security groups vs. network ACLs

Security Group = protects a specific resource (like an EC2 instance).
Network ACL = protects the entire subnet where those resources are located.

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL allows all inbound and outbound traffic. This means resources in the subnet can send and receive traffic unless the rules are changed.


A custom network ACL lets you choose which inbound and outbound traffic is allowed or denied. You can create rules based on IP addresses, protocols, and port numbers to control network access.

![Image](http://nextwork.ai/sympathetic_brown_vibrant_date/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

The three resources I deployed were a Virtual Private Cloud (VPC), an Internet Gateway, and a Security Group. I created them in a different AWS Region using AWS CloudShell and the AWS CLI to practice managing resources across multiple regions.

EC2 Global View is a feature that allows me to see and manage my EC2 and VPC resources across different AWS Regions from one dashboard. It makes it easier to track resources without switching between Regions, especially when working with deployments in multiple locations.

I would use EC2 Global View when I need to monitor and manage EC2 and VPC resources across multiple AWS Regions. It helps me quickly find resources from one dashboard instead of switching between Regions, making resource management more organized and efficient.

![Image](http://nextwork.ai/sympathetic_brown_vibrant_date/uploads/aws-networks-security_b03ea6162)

---

---
