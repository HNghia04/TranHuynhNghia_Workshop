---
title: "Week 3 Worklog"
date: 2026-05-19
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

## Mục tiêu tuần 3

* Tìm hiểu dịch vụ Amazon EC2 và cách triển khai máy chủ trên AWS.
* Nghiên cứu cơ chế giao tiếp thời gian thực bằng WebSocket.
* Làm quen với môi trường phát triển Node.js.
* Tìm hiểu quy trình kết nối giữa Game Client và Game Server.
* Thực hành triển khai một WebSocket Server cơ bản trên Amazon EC2.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Tìm hiểu tổng quan về Amazon EC2, các loại EC2 Instance, Amazon Machine Image và phương thức tính phí. | 19/05/2026 | 19/05/2026 | <https://docs.aws.amazon.com/ec2/> |
| Thứ 4 | Nghiên cứu Amazon EBS, Key Pair, Elastic IP và các phương thức kết nối vào EC2 bằng SSH. | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/> |
| Thứ 5 | Tìm hiểu Amazon VPC, Public Subnet, Route Table, Internet Gateway và Security Group. | 21/05/2026 | 21/05/2026 | <https://docs.aws.amazon.com/vpc/> |
| Thứ 6 | Nghiên cứu giao thức WebSocket, quá trình thiết lập kết nối và sự khác biệt giữa WebSocket với HTTP truyền thống. | 22/05/2026 | 22/05/2026 | <https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API> |
| Thứ 7 | Cài đặt Node.js, npm và xây dựng WebSocket Server thử nghiệm trên môi trường phát triển cục bộ. | 23/05/2026 | 23/05/2026 | Node.js Documentation |
| Chủ nhật | Khởi tạo EC2 Instance, cấu hình Security Group, cài đặt Node.js và triển khai WebSocket Server lên AWS. | 24/05/2026 | 24/05/2026 | AWS EC2 Documentation |
| Thứ 2 | Kiểm tra kết nối giữa Game Client và WebSocket Server, ghi nhận lỗi kết nối và tổng hợp kết quả thực hành. | 25/05/2026 | 25/05/2026 | Tài liệu dự án và ghi chú cá nhân |

## Kết quả đạt được

* Hiểu được vai trò của Amazon EC2 trong việc cung cấp tài nguyên máy chủ cho Game Server.

* Nắm được các thành phần cơ bản của Amazon EC2:

  * Instance Type
  * Amazon Machine Image
  * Amazon EBS
  * Key Pair
  * Elastic IP
  * Security Group

* Hiểu được cấu trúc mạng cơ bản trên AWS:

  * Amazon VPC
  * Public Subnet
  * Route Table
  * Internet Gateway
  * Inbound Rule
  * Outbound Rule

* Hiểu cơ chế hoạt động của WebSocket và khả năng duy trì kết nối hai chiều giữa Client và Server.

* Phân biệt được hai phương thức giao tiếp:

  * HTTP Request/Response
  * WebSocket Persistent Connection

* Xây dựng được WebSocket Server cơ bản bằng Node.js.

* Triển khai thành công WebSocket Server thử nghiệm trên Amazon EC2.

* Thực hiện kết nối thử nghiệm giữa Client và Server thông qua địa chỉ IP và cổng được cấu hình.

* Xác định được các yêu cầu mạng và bảo mật cần thiết để triển khai Game Server trên AWS.