---
title: "Week 5 Worklog"
date: 2026-06-02
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


## Mục tiêu tuần 5

* Phân tích yêu cầu của đề tài thực tập.
* Xác định phạm vi chức năng và yêu cầu phi chức năng.
* Xây dựng kiến trúc tổng thể cho hệ thống.
* Lựa chọn các dịch vụ AWS phù hợp.
* Lập kế hoạch triển khai theo từng giai đoạn.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Phân tích mục tiêu đề tài và xác định bài toán cần giải quyết của hệ thống Backend Game Multiplayer. | 02/06/2026 | 02/06/2026 | Tài liệu yêu cầu đề tài |
| Thứ 4 | Xác định các yêu cầu chức năng: đăng ký, đăng nhập, matchmaking, tạo phòng, kết nối Game Server và lưu kết quả trận đấu. | 03/06/2026 | 03/06/2026 | Ghi chú phân tích nghiệp vụ |
| Thứ 5 | Xác định yêu cầu phi chức năng về hiệu năng, bảo mật, khả năng mở rộng, độ sẵn sàng và chi phí vận hành. | 04/06/2026 | 04/06/2026 | AWS Well-Architected Framework |
| Thứ 6 | Phân tích và lựa chọn AWS Cognito, API Gateway, Lambda, DynamoDB, EC2, S3, CloudFront và AWS WAF. | 05/06/2026 | 05/06/2026 | AWS Documentation |
| Thứ 7 | Thiết kế kiến trúc logic và mô tả mối quan hệ giữa các thành phần trong hệ thống. | 06/06/2026 | 06/06/2026 | Sơ đồ kiến trúc dự án |
| Chủ nhật | Chuẩn bị môi trường phát triển, cấu trúc source code, công cụ quản lý mã nguồn và tài khoản AWS. | 07/06/2026 | 07/06/2026 | GitHub và AWS Documentation |
| Thứ 2 | Lập kế hoạch triển khai theo giai đoạn, xác định đầu ra, mốc thời gian và tiêu chí hoàn thành. | 08/06/2026 | 08/06/2026 | Kế hoạch thực hiện đồ án |

## Kết quả đạt được

* Xác định được tên và định hướng của đề tài:

  **Serverless & Spot Instance Backend Architecture for Live-Service Games on AWS**

* Xác định được các chức năng chính:

  * Xác thực người chơi
  * Phân quyền truy cập
  * Phân phối tài nguyên game
  * Matchmaking
  * Khởi tạo Game Session
  * Cấp phát Game Server
  * Đồng bộ trạng thái thời gian thực
  * Lưu kết quả trận đấu
  * Xử lý dữ liệu sau trận đấu

* Xác định được các yêu cầu phi chức năng:

  * Khả năng mở rộng
  * Độ trễ thấp
  * Tính sẵn sàng
  * Bảo mật
  * Tối ưu chi phí
  * Tự động triển khai
  * Khả năng giám sát

* Lựa chọn các dịch vụ AWS dự kiến sử dụng:

  * Amazon Cognito
  * Amazon API Gateway
  * AWS Lambda
  * Amazon DynamoDB
  * Amazon EC2 Spot Instance
  * Amazon S3
  * Amazon CloudFront
  * AWS WAF
  * AWS CodeDeploy
  * Amazon CloudWatch

* Hoàn thành kiến trúc logic ban đầu của hệ thống.

* Xây dựng kế hoạch triển khai theo các giai đoạn:

  * Thiết kế kiến trúc và bảo mật
  * Xây dựng Serverless Backend
  * Phát triển Matchmaker
  * Triển khai Game Server
  * Xây dựng GitOps Pipeline
  * Kiểm thử và tối ưu