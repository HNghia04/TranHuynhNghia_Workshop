---
title: "Week 2 Worklog"
date: 2026-05-12
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

{{% notice warning %}}
⚠️ Nội dung dưới đây được xây dựng phục vụ báo cáo thực tập và ghi nhận quá trình thực hiện trong tuần.
{{% /notice %}}

## Mục tiêu tuần 2

* Nghiên cứu kiến trúc Serverless trên AWS.
* Tìm hiểu cơ chế xác thực người dùng bằng Amazon Cognito.
* Tìm hiểu Amazon API Gateway và AWS Lambda.
* Nghiên cứu Amazon DynamoDB và mô hình dữ liệu NoSQL.
* Xây dựng luồng xử lý cơ bản của Backend Game Multiplayer.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
|------|-----------|--------------|-----------------|-------------------|
| Thứ 2 | Tìm hiểu khái niệm Authentication, Authorization và cơ chế hoạt động của JSON Web Token (JWT). | 12/05/2026 | 12/05/2026 | Amazon Cognito Documentation |
| Thứ 3 | Nghiên cứu Amazon Cognito User Pool, quy trình đăng ký, đăng nhập, xác thực người dùng và cấp phát JWT Token. | 13/05/2026 | 13/05/2026 | AWS Cognito Developer Guide |
| Thứ 4 | Nghiên cứu Amazon Cognito Identity Pool và cơ chế cấp Temporary IAM Credentials cho người dùng đã xác thực. | 14/05/2026 | 14/05/2026 | AWS Cognito Documentation |
| Thứ 5 | Tìm hiểu Amazon API Gateway, HTTP API, Route, Method và Cognito Authorizer. | 15/05/2026 | 15/05/2026 | AWS API Gateway Documentation |
| Thứ 6 | Nghiên cứu AWS Lambda, cơ chế Event-driven, IAM Role, Environment Variables và CloudWatch Logs. | 16/05/2026 | 16/05/2026 | AWS Lambda Documentation |
| Thứ 7 | Nghiên cứu Amazon DynamoDB, thiết kế bảng dữ liệu NoSQL cho Player, Matchmaking và Game Session. Xây dựng sơ đồ luồng xử lý giữa Cognito, API Gateway, Lambda và DynamoDB. | 17/05/2026 | 18/05/2026 | AWS DynamoDB Documentation |

## Kết quả đạt được

* Hiểu được sự khác biệt giữa Authentication và Authorization.

* Nắm được cơ chế hoạt động của JSON Web Token gồm:

  * ID Token
  * Access Token
  * Refresh Token

* Hiểu quy trình xác thực người dùng bằng Amazon Cognito User Pool.

* Hiểu cách Amazon Cognito Identity Pool cấp Temporary IAM Credentials để truy cập tài nguyên AWS.

* Nắm được vai trò của Amazon API Gateway trong việc tiếp nhận và định tuyến yêu cầu từ Game Client đến Backend Serverless.

* Hiểu cơ chế hoạt động của AWS Lambda:

  * Serverless Computing
  * Event-driven Processing
  * IAM Execution Role
  * Environment Variables
  * CloudWatch Logging

* Nghiên cứu được mô hình dữ liệu của Amazon DynamoDB:

  * Partition Key
  * Sort Key
  * Item
  * Attribute
  * Single Table Design

* Thiết kế sơ bộ cấu trúc dữ liệu cho:

  * Player
  * Matchmaking Queue
  * Match Session
  * Game Server
  * Match State

* Xây dựng sơ đồ luồng xử lý Backend ban đầu:

  * Game Client → Amazon Cognito
  * Amazon Cognito → API Gateway
  * API Gateway → AWS Lambda
  * AWS Lambda → Amazon DynamoDB

* Hoàn thành nền tảng kỹ thuật để triển khai hệ thống Matchmaking và Backend Serverless trong các tuần tiếp theo.