---
title: "Week 7 Worklog"
date: 2026-06-16
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

{{% notice warning %}}
⚠️ Nội dung dưới đây được xây dựng phục vụ báo cáo thực tập và ghi nhận quá trình thực hiện trong tuần.
{{% /notice %}}

## Mục tiêu tuần 7

* Triển khai hạ tầng mạng trên AWS.
* Cấu hình Amazon EC2 và Security Group.
* Cài đặt môi trường Node.js trên Game Server.
* Xây dựng WebSocket Server phục vụ giao tiếp thời gian thực.
* Kiểm tra khả năng kết nối giữa nhiều Game Client.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Tạo Amazon VPC, Public Subnet, Private Subnet, Route Table và Internet Gateway. | 16/06/2026 | 16/06/2026 | Amazon VPC Documentation |
| Thứ 4 | Cấu hình Security Group cho Game Server, giới hạn cổng SSH và cổng WebSocket. | 17/06/2026 | 17/06/2026 | EC2 Security Group Documentation |
| Thứ 5 | Khởi tạo EC2 Instance, cấu hình Key Pair, IAM Instance Profile và kết nối bằng SSH. | 18/06/2026 | 18/06/2026 | Amazon EC2 Documentation |
| Thứ 6 | Cài đặt Node.js, npm, Git và các thư viện cần thiết trên EC2 Instance. | 19/06/2026 | 19/06/2026 | Node.js Documentation |
| Thứ 7 | Xây dựng WebSocket Server, xử lý kết nối, ngắt kết nối và gửi thông điệp giữa các Client. | 20/06/2026 | 20/06/2026 | WebSocket Documentation |
| Chủ nhật | Xây dựng cơ chế tạo phòng chơi và quản lý danh sách người chơi trong từng Game Session. | 21/06/2026 | 21/06/2026 | Source code dự án |
| Thứ 2 | Thực hiện kiểm thử nhiều Client, ghi log kết nối và xử lý các lỗi mạng phát sinh. | 22/06/2026 | 22/06/2026 | Amazon CloudWatch và ghi chú kiểm thử |

## Kết quả đạt được

* Triển khai được hạ tầng mạng cơ bản trên AWS.

* Cấu hình các thành phần:

  * Amazon VPC
  * Public Subnet
  * Private Subnet
  * Route Table
  * Internet Gateway
  * Security Group

* Khởi tạo và cấu hình thành công Amazon EC2 Instance.

* Cài đặt thành công môi trường Node.js trên EC2.

* Xây dựng WebSocket Server có các chức năng cơ bản:

  * Tiếp nhận kết nối từ Client
  * Xác định Client ID
  * Tạo phòng chơi
  * Thêm người chơi vào phòng
  * Gửi thông điệp đến một người chơi
  * Phát thông điệp đến toàn bộ phòng
  * Xử lý khi người chơi ngắt kết nối

* Kiểm thử kết nối đồng thời từ nhiều Game Client.

* Ghi nhận và xử lý một số vấn đề:

  * Cổng kết nối bị chặn bởi Security Group
  * WebSocket Server bị dừng khi phiên SSH kết thúc
  * Client mất kết nối khi IP thay đổi
  * Thông điệp không đúng định dạng

* Hoàn thành nền tảng Game Server để tích hợp với Matchmaking.