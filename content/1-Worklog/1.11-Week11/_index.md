---
title: "Week 11 Worklog"
date: 2026-07-15
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

{{% notice warning %}}
⚠️ The content below was prepared for the internship report and documents the work completed during this week.
{{% /notice %}}

## Week 11 Objectives

* Complete the remaining system functionalities.
* Improve the stability of the Backend and Game Server.
* Test exceptional and failure scenarios.
* Optimize AWS performance and operational costs.
* Finalize the technical documentation and deployment guide.

## Tasks Performed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Wednesday | Reviewed the project feature list and identified the remaining implementation tasks. | 15/07/2026 | 15/07/2026 | Project Implementation Plan |
| Thursday | Completed the end-of-match workflow, including storing match results and updating the Game Session status. | 16/07/2026 | 16/07/2026 | Project Source Code |
| Friday | Implemented Amazon DynamoDB Streams and AWS Lambda functions to process post-match data asynchronously. | 17/07/2026 | 17/07/2026 | Amazon DynamoDB Streams Documentation |
| Saturday | Tested failure scenarios involving Game Server failures, player disconnections, and Amazon EC2 Spot Instance interruptions. | 18/07/2026 | 18/07/2026 | Amazon EC2 Spot Instances Documentation |
| Sunday | Optimized AWS Lambda memory allocation, timeout settings, Amazon DynamoDB capacity mode, and Game Server startup time. | 19/07/2026 | 19/07/2026 | AWS Cost Optimization Guidance |
| Monday | Finalized the deployment guide, environment variable configuration, IAM Roles, and testing instructions. | 20/07/2026 | 20/07/2026 | Project Technical Documentation |
| Tuesday | Performed full regression testing across the entire system and verified the final implementation results. | 21/07/2026 | 21/07/2026 | Testing Report |

## Achievements

* Successfully completed the core functionalities of the system.

* Implemented the complete match completion workflow:

  * The Game Server detects the end of a match.
  * Match results are submitted to the Backend.
  * Amazon DynamoDB updates the Match State.
  * Amazon DynamoDB Streams trigger an AWS Lambda function.
  * AWS Lambda processes post-match statistics asynchronously.

* Implemented asynchronous processing to ensure that post-match operations do not affect Matchmaking latency.

* Successfully tested various exceptional scenarios, including:

  * Players leaving before the match starts
  * Player disconnections during a match
  * Game Server failures
  * Insufficient players for matchmaking
  * Duplicate match creation requests
  * Amazon EC2 Spot Instance interruptions

* Proposed strategies to minimize the impact of Spot Instance interruptions:

  * Using Amazon EC2 Auto Scaling Groups
  * Maintaining a pool of warm standby instances
  * Deploying across multiple Availability Zones
  * Storing Match State outside the Game Server
  * Preventing new matches from being assigned to instances scheduled for interruption

* Optimized AWS Lambda and Amazon DynamoDB configurations to improve performance and reduce operational costs.

* Completed the project documentation, including:

  * System Architecture
  * Deployment Guide
  * Configuration Guide
  * API Documentation
  * Data Model
  * Test Report
  * Troubleshooting Guide