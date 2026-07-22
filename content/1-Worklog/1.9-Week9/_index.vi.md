---
title: "Week 9 Worklog"
date: 2026-06-30
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

{{% notice warning %}}
⚠️ Nội dung dưới đây được xây dựng phục vụ báo cáo thực tập và ghi nhận quá trình thực hiện trong tuần.
{{% /notice %}}

## Mục tiêu tuần 9

* Tích hợp WebSocket vào Game Client.
* Kết nối người chơi đến Game Server sau khi Matchmaking thành công.
* Xây dựng cơ chế quản lý Game Session.
* Đồng bộ trạng thái giữa nhiều người chơi.
* Xử lý các tình huống mất kết nối và kết nối lại.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Tích hợp chức năng đăng nhập và lưu JWT Token trong Game Client. | 30/06/2026 | 30/06/2026 | Amazon Cognito Documentation |
| Thứ 4 | Tích hợp API Matchmaking và xử lý kết quả trả về gồm Match ID, Server IP và Port. | 01/07/2026 | 01/07/2026 | API Gateway Documentation |
| Thứ 5 | Xây dựng chức năng Game Client kết nối đến WebSocket Game Server sau khi ghép trận. | 02/07/2026 | 02/07/2026 | WebSocket Client Documentation |
| Thứ 6 | Xây dựng định dạng thông điệp cho Join Room, Player Update, Game Event và Disconnect. | 03/07/2026 | 03/07/2026 | Tài liệu thiết kế giao thức |
| Thứ 7 | Triển khai cơ chế đồng bộ trạng thái người chơi giữa nhiều Client trong cùng Game Session. | 04/07/2026 | 04/07/2026 | Source code dự án |
| Chủ nhật | Xử lý mất kết nối, kết nối lại và kiểm tra người chơi còn thuộc Game Session hay không. | 05/07/2026 | 05/07/2026 | Ghi chú kiểm thử |
| Thứ 2 | Kiểm thử End-to-End từ đăng nhập, Matchmaking, kết nối Game Server đến đồng bộ trạng thái. | 06/07/2026 | 06/07/2026 | CloudWatch Logs và báo cáo kiểm thử |

## Kết quả đạt được

* Tích hợp thành công Amazon Cognito vào Game Client.

* Game Client có thể:

  * Đăng nhập
  * Nhận JWT Token
  * Gửi yêu cầu Matchmaking
  * Nhận thông tin Game Session
  * Kết nối đến Game Server

* Xây dựng cấu trúc thông điệp WebSocket thống nhất:

  * JoinRoom
  * PlayerJoined
  * PlayerStateUpdate
  * GameEvent
  * MatchStarted
  * MatchEnded
  * PlayerDisconnected

* Thực hiện đồng bộ trạng thái giữa nhiều người chơi.

* Game Server có thể kiểm tra Match ID và Player ID khi Client tham gia phòng.

* Xây dựng cơ chế xử lý:

  * Người chơi mất kết nối
  * Người chơi kết nối lại
  * Người chơi thoát trận
  * Phòng chơi đủ người
  * Trận đấu kết thúc

* Hoàn thành luồng End-to-End cơ bản:

  * Authentication
  * Matchmaking
  * Session Allocation
  * WebSocket Connection
  * Realtime Synchronization
  * Match Completion