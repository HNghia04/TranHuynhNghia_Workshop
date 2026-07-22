---
title: "Week 11 Worklog"
date: 2026-07-15
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

{{% notice warning %}}
⚠️ Nội dung dưới đây được xây dựng phục vụ báo cáo thực tập và ghi nhận quá trình thực hiện trong tuần.
{{% /notice %}}

## Mục tiêu tuần 11

* Hoàn thiện các chức năng còn lại của hệ thống.
* Tăng độ ổn định của Backend và Game Server.
* Kiểm thử các trường hợp ngoại lệ.
* Tối ưu hiệu năng và chi phí sử dụng AWS.
* Hoàn thiện tài liệu kỹ thuật và hướng dẫn triển khai.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 4 | Rà soát danh sách chức năng và xác định các hạng mục chưa hoàn thành. | 15/07/2026 | 15/07/2026 | Kế hoạch thực hiện dự án |
| Thứ 5 | Hoàn thiện xử lý kết thúc trận đấu, lưu kết quả và cập nhật trạng thái Game Session. | 16/07/2026 | 16/07/2026 | Source code dự án |
| Thứ 6 | Bổ sung DynamoDB Streams và Lambda xử lý dữ liệu sau trận đấu. | 17/07/2026 | 17/07/2026 | DynamoDB Streams Documentation |
| Thứ 7 | Kiểm thử các trường hợp Game Server lỗi, người chơi thoát trận và Spot Instance bị gián đoạn. | 18/07/2026 | 18/07/2026 | EC2 Spot Instance Documentation |
| Chủ nhật | Tối ưu Lambda Memory, Timeout, DynamoDB Capacity Mode và thời gian khởi động Game Server. | 19/07/2026 | 19/07/2026 | AWS Cost Optimization Guidance |
| Thứ 2 | Hoàn thiện tài liệu triển khai, biến môi trường, IAM Role và hướng dẫn kiểm thử. | 20/07/2026 | 20/07/2026 | Tài liệu kỹ thuật dự án |
| Thứ 3 | Thực hiện kiểm thử hồi quy toàn bộ hệ thống và xác nhận kết quả cuối cùng. | 21/07/2026 | 21/07/2026 | Báo cáo kiểm thử |

## Kết quả đạt được

* Hoàn thiện các chức năng chính của hệ thống.

* Xây dựng quy trình kết thúc trận đấu:

  * Game Server xác định trận đấu kết thúc
  * Kết quả được gửi về Backend
  * DynamoDB cập nhật Match State
  * DynamoDB Streams kích hoạt Lambda
  * Lambda xử lý thống kê sau trận đấu

* Bổ sung xử lý bất đồng bộ để không ảnh hưởng đến độ trễ của Matchmaking.

* Kiểm thử các trường hợp ngoại lệ:

  * Người chơi thoát trước khi trận bắt đầu
  * Người chơi mất kết nối giữa trận
  * Game Server không phản hồi
  * Matchmaking không tìm đủ người
  * Trùng yêu cầu tạo trận
  * Spot Instance bị thu hồi

* Đề xuất phương án giảm ảnh hưởng của Spot Instance Interruption:

  * Sử dụng Auto Scaling Group
  * Duy trì một số Warm Instance
  * Phân bổ đa Availability Zone
  * Lưu Match State bên ngoài Game Server
  * Không phân bổ trận mới cho Instance chuẩn bị bị thu hồi

* Tối ưu các cấu hình AWS Lambda và DynamoDB.

* Hoàn thiện tài liệu:

  * System Architecture
  * Deployment Guide
  * Configuration Guide
  * API Description
  * Data Model
  * Test Report
  * Troubleshooting Guide