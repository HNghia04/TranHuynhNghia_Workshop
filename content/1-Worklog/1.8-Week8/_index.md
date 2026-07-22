---
title: "Week 8 Worklog"
date: 2026-06-23
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

{{% notice warning %}}
⚠️ The content below was prepared for the internship report and documents the work completed during this week.
{{% /notice %}}

## Week 8 Objectives

* Implement user authentication using Amazon Cognito.
* Integrate Amazon API Gateway with AWS Lambda.
* Develop the Matchmaker Lambda function.
* Design and deploy the Amazon DynamoDB database schema.
* Complete the login and matchmaking workflow.

## Tasks Performed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Tuesday | Created an Amazon Cognito User Pool and configured user attributes and password policies. | 23/06/2026 | 23/06/2026 | Amazon Cognito Documentation |
| Wednesday | Created an App Client and tested user registration, account confirmation, and sign-in to obtain JWT tokens. | 24/06/2026 | 24/06/2026 | Amazon Cognito User Pool Documentation |
| Thursday | Created an Amazon API Gateway HTTP API, configured routes, and integrated a Cognito Authorizer to secure the Matchmaking APIs. | 25/06/2026 | 25/06/2026 | Amazon API Gateway Documentation |
| Friday | Developed the Matchmaker Lambda function to receive player information and process matchmaking requests. | 26/06/2026 | 26/06/2026 | AWS Lambda Documentation |
| Saturday | Created Amazon DynamoDB tables and implemented the data model for Player, Queue, Match Session, and Server State. | 27/06/2026 | 27/06/2026 | Amazon DynamoDB Documentation |
| Sunday | Integrated AWS Lambda with Amazon DynamoDB, implemented Match creation, and updated player states. | 28/06/2026 | 28/06/2026 | AWS SDK Documentation |
| Monday | Tested the complete workflow involving Amazon Cognito, Amazon API Gateway, AWS Lambda, and Amazon DynamoDB using the Game Client and API testing tools. | 29/06/2026 | 29/06/2026 | Postman and Amazon CloudWatch Logs |

## Achievements

* Successfully created and configured an Amazon Cognito User Pool.

* Implemented the following authentication features:

  * User Registration
  * Account Confirmation
  * User Sign-in
  * JWT Token Issuance
  * Token Refresh
  * Token Expiration Validation

* Successfully deployed Amazon API Gateway with a Cognito Authorizer.

* Ensured that only authenticated users could access the Matchmaking API.

* Developed the Matchmaker Lambda function with the following capabilities:

  * Receive player information
  * Validate input data
  * Add players to the matchmaking queue
  * Match compatible players
  * Create Match Sessions
  * Update match status
  * Return game session information

* Designed and implemented the Amazon DynamoDB database using the Single-Table Design approach.

* Successfully stored the following data:

  * Player Information
  * Matchmaking Requests
  * Queue Status
  * Match Sessions
  * Game Server Information

* Successfully tested the complete backend workflow:

  * Game Client signs in
  * Receives a JWT token
  * Sends requests to Amazon API Gateway
  * AWS Lambda processes matchmaking requests
  * Amazon DynamoDB stores the current state
  * The API returns the matchmaking result to the Game Client