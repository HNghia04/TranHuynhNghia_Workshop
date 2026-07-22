---
title: "Week 6 Worklog"
date: 2026-06-09
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

## Mục tiêu tuần 6

* Bắt đầu triển khai chính thức đề tài.
* Hoàn thiện phân tích yêu cầu và kiến trúc hệ thống.
* Xác định luồng tích hợp giữa các dịch vụ AWS.
* Thiết kế mô hình dữ liệu cho Player, Match và Game Server.
* Chuẩn hóa cấu trúc source code và môi trường phát triển.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Rà soát yêu cầu và chia hệ thống thành các module Authentication, Matchmaking, Game Server và Analytics. | 09/06/2026 | 09/06/2026 | Tài liệu yêu cầu hệ thống |
| Thứ 4 | Thiết kế luồng xác thực bằng Amazon Cognito và cơ chế truyền JWT Token đến API Gateway. | 10/06/2026 | 10/06/2026 | Amazon Cognito Documentation |
| Thứ 5 | Thiết kế luồng Matchmaking qua API Gateway, AWS Lambda và Amazon DynamoDB. | 11/06/2026 | 11/06/2026 | API Gateway và Lambda Documentation |
| Thứ 6 | Thiết kế luồng kết nối từ Game Client đến EC2 Game Server sau khi Matchmaker cấp phát phiên chơi. | 12/06/2026 | 12/06/2026 | Amazon EC2 Documentation |
| Thứ 7 | Xây dựng mô hình dữ liệu DynamoDB cho Player, Matchmaking Request, Match Session và Game Server. | 13/06/2026 | 13/06/2026 | DynamoDB Single-Table Design |
| Chủ nhật | Thiết kế IAM Role, quyền truy cập và nguyên tắc Least Privilege giữa các thành phần. | 14/06/2026 | 14/06/2026 | AWS IAM Documentation |
| Thứ 2 | Chuẩn hóa repository, cấu trúc source code, biến môi trường và tài liệu cài đặt dự án. | 15/06/2026 | 15/06/2026 | GitHub và tài liệu dự án |

## Kết quả đạt được

* Phân chia hệ thống thành các module độc lập:

  * Player Authentication
  * Asset Distribution
  * Matchmaking
  * Session Provisioning
  * Game Server
  * Post-match Processing
  * Monitoring and Logging

* Hoàn thiện luồng xác thực:

  * Người chơi đăng nhập bằng Cognito User Pool
  * Cognito cấp JWT Token
  * Game Client gửi Token đến API Gateway
  * Cognito Authorizer kiểm tra Token
  * API Gateway chuyển yêu cầu hợp lệ đến Lambda

* Hoàn thiện luồng Matchmaking ở mức thiết kế:

  * Nhận yêu cầu tìm trận
  * Kiểm tra trạng thái người chơi
  * Tạo hoặc tham gia hàng đợi
  * Tạo Match Session
  * Phân bổ Game Server
  * Trả về IP và Port cho Game Client

* Xây dựng mô hình dữ liệu DynamoDB theo hướng Single-Table Design.

* Xác định các thực thể dữ liệu:

  * Player
  * Match Queue
  * Match
  * Game Session
  * Game Server
  * Match Result

* Thiết kế sơ bộ IAM Role cho:

  * Matchmaker Lambda
  * Game Server EC2
  * Cognito Identity Pool
  * Post-match Lambda

* Hoàn thành cấu trúc dự án để chuyển sang giai đoạn triển khai hạ tầng.