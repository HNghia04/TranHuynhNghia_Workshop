---
title: "Week 3 Worklog"
date: 2026-05-19
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

## Week 3 Objectives

* Study Amazon EC2 and learn how to deploy servers on AWS.
* Learn the real-time communication mechanism using WebSocket.
* Become familiar with the Node.js development environment.
* Understand the connection workflow between the Game Client and the Game Server.
* Practice deploying a basic WebSocket Server on Amazon EC2.

## Tasks Performed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Tuesday | Studied the fundamentals of Amazon EC2, including EC2 Instance types, Amazon Machine Images (AMI), and pricing models. | 19/05/2026 | 19/05/2026 | <https://docs.aws.amazon.com/ec2/> |
| Wednesday | Studied Amazon EBS, Key Pairs, Elastic IPs, and SSH connection methods for accessing EC2 instances. | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/> |
| Thursday | Learned about Amazon VPC, Public Subnets, Route Tables, Internet Gateways, and Security Groups. | 21/05/2026 | 21/05/2026 | <https://docs.aws.amazon.com/vpc/> |
| Friday | Studied the WebSocket protocol, the connection establishment process, and the differences between WebSocket and traditional HTTP communication. | 22/05/2026 | 22/05/2026 | <https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API> |
| Saturday | Installed Node.js and npm, and built a basic WebSocket Server in the local development environment. | 23/05/2026 | 23/05/2026 | Node.js Documentation |
| Sunday | Launched an EC2 Instance, configured the Security Group, installed Node.js, and deployed the WebSocket Server to AWS. | 24/05/2026 | 24/05/2026 | AWS EC2 Documentation |
| Monday | Tested the connection between the Game Client and the WebSocket Server, identified connection issues, and summarized the implementation results. | 25/05/2026 | 25/05/2026 | Project Documentation and Personal Notes |

## Achievements

* Understood the role of Amazon EC2 in providing server resources for the Game Server.

* Learned the fundamental components of Amazon EC2, including:

  * Instance Type
  * Amazon Machine Image (AMI)
  * Amazon Elastic Block Store (Amazon EBS)
  * Key Pair
  * Elastic IP
  * Security Group

* Understood the basic AWS networking architecture, including:

  * Amazon VPC
  * Public Subnet
  * Route Table
  * Internet Gateway
  * Inbound Rules
  * Outbound Rules

* Understood how WebSocket works and its ability to maintain persistent bidirectional communication between the client and the server.

* Distinguished between the following communication methods:

  * HTTP Request/Response
  * WebSocket Persistent Connection

* Successfully built a basic WebSocket Server using Node.js.

* Successfully deployed a test WebSocket Server on Amazon EC2.

* Performed connection testing between the client and the server using the configured IP address and port.

* Identified the networking and security requirements necessary for deploying a Game Server on AWS.