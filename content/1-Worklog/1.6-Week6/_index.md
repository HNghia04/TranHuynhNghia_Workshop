---
title: "Week 6 Worklog"
date: 2026-06-09
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

{{% notice warning %}}
⚠️ The content below was prepared for the internship report and documents the work completed during this week.
{{% /notice %}}

## Week 6 Objectives

* Officially begin the implementation phase of the internship project.
* Finalize the system requirements analysis and architecture.
* Define the integration workflow among AWS services.
* Design the data model for Player, Match, and Game Server.
* Standardize the source code structure and development environment.

## Tasks Performed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Tuesday | Reviewed the system requirements and divided the solution into Authentication, Matchmaking, Game Server, and Analytics modules. | 09/06/2026 | 09/06/2026 | System Requirements Documentation |
| Wednesday | Designed the authentication workflow using Amazon Cognito and the mechanism for passing JWT tokens to Amazon API Gateway. | 10/06/2026 | 10/06/2026 | Amazon Cognito Documentation |
| Thursday | Designed the Matchmaking workflow using Amazon API Gateway, AWS Lambda, and Amazon DynamoDB. | 11/06/2026 | 11/06/2026 | API Gateway and AWS Lambda Documentation |
| Friday | Designed the connection workflow from the Game Client to the Amazon EC2 Game Server after the Matchmaker allocates a game session. | 12/06/2026 | 12/06/2026 | Amazon EC2 Documentation |
| Saturday | Designed the DynamoDB data model for Player, Matchmaking Request, Match Session, and Game Server using a Single-Table Design approach. | 13/06/2026 | 13/06/2026 | DynamoDB Single-Table Design |
| Sunday | Designed IAM Roles, access permissions, and applied the Principle of Least Privilege across system components. | 14/06/2026 | 14/06/2026 | AWS IAM Documentation |
| Monday | Standardized the project repository, source code structure, environment variables, and project setup documentation. | 15/06/2026 | 15/06/2026 | GitHub and Project Documentation |

## Achievements

* Divided the system into independent modules:

  * Player Authentication
  * Asset Distribution
  * Matchmaking
  * Session Provisioning
  * Game Server
  * Post-match Processing
  * Monitoring and Logging

* Completed the authentication workflow:

  * Players authenticate through Amazon Cognito User Pools.
  * Amazon Cognito issues JWT tokens.
  * The Game Client sends the JWT token to Amazon API Gateway.
  * The Cognito Authorizer validates the token.
  * Amazon API Gateway forwards authorized requests to AWS Lambda.

* Completed the Matchmaking workflow design:

  * Receive matchmaking requests.
  * Validate player status.
  * Create or join a matchmaking queue.
  * Create a Match Session.
  * Allocate a Game Server.
  * Return the Game Server IP address and port to the Game Client.

* Designed the Amazon DynamoDB data model using the Single-Table Design approach.

* Defined the primary data entities:

  * Player
  * Match Queue
  * Match
  * Game Session
  * Game Server
  * Match Result

* Designed the initial IAM Roles for:

  * Matchmaker Lambda
  * Game Server EC2
  * Cognito Identity Pool
  * Post-match Lambda

* Completed the project structure and development environment, preparing the project for the infrastructure implementation phase.