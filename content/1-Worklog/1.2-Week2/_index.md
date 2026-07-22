---
title: "Week 2 Worklog"
date: 2026-05-12
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

{{% notice warning %}}
⚠️ The content below was prepared for the internship report and documents the work completed during this week.
{{% /notice %}}

## Week 2 Objectives

* Study the Serverless architecture on AWS.
* Learn about user authentication using Amazon Cognito.
* Study Amazon API Gateway and AWS Lambda.
* Learn about Amazon DynamoDB and the NoSQL data model.
* Build the basic processing flow of a Multiplayer Game Backend.

## Tasks Performed

| Day | Task | Start Date | Completion Date | Reference |
|------|------|------------|-----------------|-----------|
| Monday | Studied the concepts of Authentication, Authorization, and the working mechanism of JSON Web Token (JWT). | 12/05/2026 | 12/05/2026 | Amazon Cognito Documentation |
| Tuesday | Studied Amazon Cognito User Pools, including the user registration, sign-in, authentication process, and JWT token issuance. | 13/05/2026 | 13/05/2026 | AWS Cognito Developer Guide |
| Wednesday | Studied Amazon Cognito Identity Pools and the mechanism for issuing temporary IAM credentials to authenticated users. | 14/05/2026 | 14/05/2026 | AWS Cognito Documentation |
| Thursday | Learned about Amazon API Gateway, including HTTP APIs, Routes, Methods, and Cognito Authorizers. | 15/05/2026 | 15/05/2026 | AWS API Gateway Documentation |
| Friday | Studied AWS Lambda, including the Event-driven architecture, IAM Roles, Environment Variables, and CloudWatch Logs. | 16/05/2026 | 16/05/2026 | AWS Lambda Documentation |
| Saturday | Studied Amazon DynamoDB and designed a NoSQL database schema for Player, Matchmaking, and Game Session data. Created the processing flow between Cognito, API Gateway, Lambda, and DynamoDB. | 17/05/2026 | 18/05/2026 | AWS DynamoDB Documentation |

## Achievements

* Understood the difference between Authentication and Authorization.

* Learned the working mechanism of JSON Web Tokens, including:

  * ID Token
  * Access Token
  * Refresh Token

* Understood the user authentication process using Amazon Cognito User Pools.

* Learned how Amazon Cognito Identity Pools issue temporary IAM credentials for accessing AWS resources.

* Understood the role of Amazon API Gateway in receiving and routing requests from the Game Client to the Serverless Backend.

* Learned the working principles of AWS Lambda, including:

  * Serverless Computing
  * Event-driven Processing
  * IAM Execution Role
  * Environment Variables
  * CloudWatch Logging

* Studied the Amazon DynamoDB data model, including:

  * Partition Key
  * Sort Key
  * Item
  * Attribute
  * Single Table Design

* Designed the initial data structures for:

  * Player
  * Matchmaking Queue
  * Match Session
  * Game Server
  * Match State

* Built the initial backend processing flow:

  * Game Client → Amazon Cognito
  * Amazon Cognito → Amazon API Gateway
  * Amazon API Gateway → AWS Lambda
  * AWS Lambda → Amazon DynamoDB

* Completed the technical foundation required for implementing the Matchmaking system and the Serverless Backend in the following weeks.