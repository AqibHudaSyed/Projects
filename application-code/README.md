AWS Three‑Tier Web Architecture Project 🏗️
<img width="2000" height="2588" alt="image" src="https://github.com/user-attachments/assets/ff0a32f6-8d45-487d-af20-72716883f781" />


Documentation - https://github.com/AqibHudaSyed/Projects/blob/main/AWS%20Three-tier%20project.pdf

This repository contains the source code and documentation for a scalable, highly available, and fault-tolerant three-tier web application on AWS.

The project demonstrates how to build a three-tier architecture using core AWS services and best practices for cloud applications.

📌 Architecture Overview

The project implements a three-tier cloud application with the following layers:

Web Tier

Hosts static and dynamic web content

Uses Nginx on EC2 to serve UI and proxy API calls

Application Tier

Handles business logic

Runs a Node.js backend behind an internal Load Balancer

Database Tier

Stores persistent data in Amazon Aurora MySQL (Multi‑AZ)

Traffic flow:

Users access the application via a public Application Load Balancer (ALB)

ALB forwards requests to the Web Tier EC2 instances

Web Tier proxies API calls to the internal load balancer → Application Tier

App Tier queries the Aurora MySQL database and returns results to the web tier

The architecture includes Auto Scaling, Health Checks, and Security Groups to ensure redundancy, resiliency, and secure communication between tiers.

🛠️ Features

✔ Highly Available — multiple EC2 instances managed by Auto Scaling
✔ Fault Tolerant — multi‑AZ database setup with Aurora
✔ Scalable — Load Balancing and Auto Scaling between the tiers
✔ Secure — VPC with public/private subnets and tightly scoped security groups
✔ Hands-On Implementation — full end-to-end deployment on AWS

🧾 Contents
├── app-tier/           # Node.js backend API
├── web-tier/           # HTML/React UI + Nginx config
├── nginx.conf          # Web server reverse proxy config
├── README.md           # Project overview (this file)
└── architecture.png    # Diagram of the 3-tier setup (optional)

🚀 Getting Started

Clone this repo

Set up AWS resources:

Custom VPC with public/private subnets

EC2 instances for web and app tiers

Application and internal load balancers

Aurora MySQL cluster

Configure security groups and environment variables

Deploy and test the application

🧠 What I've Learned

Designing secure and scalable cloud architectures

Creating multi-tier deployments on AWS

Auto Scaling and Load Balancing fundamentals

Networking with VPC, Public/Private subnets, and Security Groups

Connecting application code to managed databases

