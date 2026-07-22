---
title: "Week 10 Worklog"
date: 2026-07-07
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

## Mục tiêu tuần 10

* Kiểm thử toàn bộ hệ thống.
* Phát hiện và xử lý lỗi đồng bộ thời gian thực.
* Đánh giá hiệu năng của Matchmaker và Game Server.
* Tối ưu thời gian phản hồi và tài nguyên sử dụng.
* Cập nhật tài liệu kỹ thuật của dự án.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Xây dựng danh sách Test Case cho Authentication, Matchmaking, Game Session và WebSocket. | 07/07/2026 | 07/07/2026 | Tài liệu kiểm thử dự án |
| Thứ 4 | Kiểm thử luồng đăng ký, đăng nhập, JWT Token và API Authorization. | 08/07/2026 | 08/07/2026 | Cognito và API Gateway Logs |
| Thứ 5 | Kiểm thử Matchmaker với nhiều yêu cầu đồng thời và kiểm tra dữ liệu trong DynamoDB. | 09/07/2026 | 09/07/2026 | DynamoDB và CloudWatch |
| Thứ 6 | Kiểm thử WebSocket với nhiều Client, đo thời gian phản hồi và phát hiện lỗi đồng bộ. | 10/07/2026 | 10/07/2026 | Công cụ kiểm thử WebSocket |
| Thứ 7 | Sửa lỗi trùng lặp sự kiện, sai trạng thái phòng và mất kết nối giữa trận. | 11/07/2026 | 11/07/2026 | Source code và ghi chú lỗi |
| Chủ nhật | Tối ưu truy vấn DynamoDB, giảm số lần gọi API và cải thiện xử lý bất đồng bộ. | 12/07/2026 | 12/07/2026 | AWS Performance Guidelines |
| Thứ 2 | Tổng hợp kết quả kiểm thử và cập nhật tài liệu kiến trúc, triển khai và vận hành. | 13/07/2026 | 14/07/2026 | Báo cáo kỹ thuật dự án |

## Kết quả đạt được

* Xây dựng bộ Test Case cho các nhóm chức năng:

  * Authentication
  * Authorization
  * Matchmaking
  * Game Session
  * WebSocket Connection
  * State Synchronization
  * Match Completion

* Kiểm thử thành công luồng hoạt động tổng thể của hệ thống.

* Phát hiện và xử lý các lỗi:

  * JWT Token hết hạn
  * Người chơi gửi yêu cầu Matchmaking nhiều lần
  * Một người chơi bị thêm vào nhiều Match
  * Trạng thái Match chưa được cập nhật kịp thời
  * WebSocket gửi trùng sự kiện
  * Client không nhận được thông báo ngắt kết nối
  * Dữ liệu trận đấu chưa được lưu đầy đủ

* Tối ưu truy vấn DynamoDB bằng cách sử dụng đúng Partition Key và Sort Key.

* Bổ sung kiểm tra điều kiện trước khi cập nhật trạng thái Match.

* Cải thiện khả năng xử lý lỗi và cấu trúc phản hồi API.

* Bổ sung CloudWatch Logs để hỗ trợ theo dõi và khắc phục sự cố.

* Hoàn thiện phiên bản đầu tiên của tài liệu kỹ thuật.