---
title: "Week 8 Worklog"
date: 2026-06-23
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


## Mục tiêu tuần 8

* Xây dựng chức năng xác thực bằng Amazon Cognito.
* Tích hợp Amazon API Gateway với AWS Lambda.
* Phát triển Matchmaker Lambda.
* Thiết kế và triển khai bảng dữ liệu DynamoDB.
* Hoàn thiện luồng đăng nhập và tìm trận.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Tạo Amazon Cognito User Pool, cấu hình thuộc tính người dùng và chính sách mật khẩu. | 23/06/2026 | 23/06/2026 | Amazon Cognito Documentation |
| Thứ 4 | Tạo App Client, kiểm thử đăng ký, xác nhận tài khoản và đăng nhập để nhận JWT Token. | 24/06/2026 | 24/06/2026 | Cognito User Pool Documentation |
| Thứ 5 | Tạo API Gateway HTTP API, Route và Cognito Authorizer để bảo vệ API Matchmaking. | 25/06/2026 | 25/06/2026 | API Gateway Documentation |
| Thứ 6 | Xây dựng Matchmaker Lambda để tiếp nhận thông tin người chơi và xử lý yêu cầu tìm trận. | 26/06/2026 | 26/06/2026 | AWS Lambda Documentation |
| Thứ 7 | Tạo DynamoDB Table và triển khai cấu trúc lưu Player, Queue, Match Session và Server State. | 27/06/2026 | 27/06/2026 | DynamoDB Documentation |
| Chủ nhật | Tích hợp Lambda với DynamoDB, xây dựng chức năng tạo Match và cập nhật trạng thái người chơi. | 28/06/2026 | 28/06/2026 | AWS SDK Documentation |
| Thứ 2 | Kiểm thử toàn bộ luồng Cognito, API Gateway, Lambda và DynamoDB bằng Game Client hoặc công cụ API. | 29/06/2026 | 29/06/2026 | Postman và CloudWatch Logs |

## Kết quả đạt được

* Tạo và cấu hình thành công Amazon Cognito User Pool.

* Triển khai các chức năng xác thực:

  * Đăng ký tài khoản
  * Xác nhận tài khoản
  * Đăng nhập
  * Nhận JWT Token
  * Làm mới Token
  * Kiểm tra Token hết hạn

* Tạo API Gateway và cấu hình Cognito Authorizer.

* Đảm bảo chỉ người dùng đã xác thực mới có thể gửi yêu cầu Matchmaking.

* Xây dựng Matchmaker Lambda có khả năng:

  * Nhận thông tin người chơi
  * Kiểm tra dữ liệu đầu vào
  * Thêm người chơi vào hàng đợi
  * Tìm người chơi phù hợp
  * Tạo Match Session
  * Cập nhật trạng thái trận đấu
  * Trả thông tin phiên chơi

* Tạo bảng DynamoDB theo hướng Single-Table Design.

* Lưu trữ được các dữ liệu:

  * Thông tin người chơi
  * Yêu cầu tìm trận
  * Trạng thái hàng đợi
  * Match Session
  * Thông tin Game Server

* Kiểm thử thành công luồng:

  * Game Client đăng nhập
  * Nhận JWT Token
  * Gửi yêu cầu đến API Gateway
  * Lambda xử lý Matchmaking
  * DynamoDB lưu trạng thái
  * API trả kết quả cho Game Client