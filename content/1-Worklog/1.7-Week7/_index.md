---
title: "Week 7 Worklog"
date: 2026-06-16
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---


## Week 7 Objectives

* Deploy the network infrastructure on AWS.
* Configure Amazon EC2 and Security Groups.
* Install the Node.js development environment on the Game Server.
* Develop a WebSocket Server for real-time communication.
* Test connectivity among multiple Game Clients.

## Tasks Performed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Tuesday | Created an Amazon VPC, Public Subnet, Private Subnet, Route Tables, and an Internet Gateway. | 16/06/2026 | 16/06/2026 | Amazon VPC Documentation |
| Wednesday | Configured Security Groups for the Game Server, restricting SSH access and WebSocket ports. | 17/06/2026 | 17/06/2026 | Amazon EC2 Security Group Documentation |
| Thursday | Launched an Amazon EC2 Instance, configured the Key Pair, IAM Instance Profile, and established an SSH connection. | 18/06/2026 | 18/06/2026 | Amazon EC2 Documentation |
| Friday | Installed Node.js, npm, Git, and the required dependencies on the EC2 instance. | 19/06/2026 | 19/06/2026 | Node.js Documentation |
| Saturday | Developed the WebSocket Server to handle client connections, disconnections, and message exchange between connected clients. | 20/06/2026 | 20/06/2026 | WebSocket Documentation |
| Sunday | Implemented the game room creation mechanism and managed the list of players within each Game Session. | 21/06/2026 | 21/06/2026 | Project Source Code |
| Monday | Performed multi-client connection testing, collected connection logs, and resolved network-related issues. | 22/06/2026 | 22/06/2026 | Amazon CloudWatch and Testing Notes |

## Achievements

* Successfully deployed the basic AWS network infrastructure.

* Configured the following AWS networking components:

  * Amazon VPC
  * Public Subnet
  * Private Subnet
  * Route Table
  * Internet Gateway
  * Security Group

* Successfully launched and configured an Amazon EC2 instance.

* Successfully installed the Node.js development environment on the EC2 instance.

* Developed a WebSocket Server with the following core functionalities:

  * Accept client connections
  * Identify connected clients using Client IDs
  * Create game rooms
  * Add players to game rooms
  * Send messages to individual players
  * Broadcast messages to all players within a game room
  * Handle player disconnections

* Successfully tested concurrent connections from multiple Game Clients.

* Identified and resolved several issues, including:

  * Connection ports blocked by Security Group rules
  * WebSocket Server terminating after the SSH session ended
  * Client disconnections caused by IP address changes
  * Incorrect message formats exchanged between clients

* Completed the foundational Game Server implementation, preparing it for integration with the Matchmaking system.