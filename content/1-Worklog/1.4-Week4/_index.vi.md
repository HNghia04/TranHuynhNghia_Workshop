---
title: "Week 4 Worklog"
date: 2026-05-26
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

{{% notice warning %}}
⚠️ Nội dung dưới đây được xây dựng phục vụ báo cáo thực tập và ghi nhận quá trình thực hiện trong tuần.
{{% /notice %}}

## Mục tiêu tuần 4

* Nghiên cứu kiến trúc Backend dành cho game multiplayer.
* Tìm hiểu cơ chế Matchmaking và quản lý Game Session.
* Nghiên cứu phương pháp đồng bộ trạng thái giữa nhiều người chơi.
* Phân tích luồng dữ liệu trong một trận đấu trực tuyến.
* Xác định các thành phần chính của hệ thống Live-Service Game Backend.

## Công việc thực hiện

| Ngày | Nội dung | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| Thứ 3 | Nghiên cứu kiến trúc tổng thể của hệ thống game multiplayer và phân biệt Game Client, Metagame Backend với Game Server. | 26/05/2026 | 26/05/2026 | AWS Game Tech Documentation |
| Thứ 4 | Tìm hiểu cơ chế Matchmaking, hàng đợi người chơi, điều kiện ghép trận và quá trình tạo phòng chơi. | 27/05/2026 | 27/05/2026 | Tài liệu kiến trúc game multiplayer |
| Thứ 5 | Phân tích vòng đời của một Game Session từ lúc người chơi đăng nhập đến khi trận đấu kết thúc. | 28/05/2026 | 28/05/2026 | Ghi chú phân tích hệ thống |
| Thứ 6 | Nghiên cứu cơ chế đồng bộ vị trí, trạng thái và sự kiện giữa các Game Client thông qua Game Server. | 29/05/2026 | 29/05/2026 | WebSocket và Realtime Networking Documentation |
| Thứ 7 | Tìm hiểu các vấn đề về độ trễ, mất kết nối, tái kết nối và xử lý xung đột trạng thái trong game. | 30/05/2026 | 30/05/2026 | Tài liệu kỹ thuật về multiplayer networking |
| Chủ nhật | Phân tích cách lưu trữ Player State, Match State và Match Result trong cơ sở dữ liệu. | 31/05/2026 | 31/05/2026 | Amazon DynamoDB Documentation |
| Thứ 2 | Xây dựng sơ đồ kiến trúc sơ bộ và xác định các luồng Authentication, Matchmaking, Game Session và Post-match Processing. | 01/06/2026 | 01/06/2026 | Tài liệu dự án |

## Kết quả đạt được

* Hiểu được cấu trúc cơ bản của một hệ thống game multiplayer gồm:

  * Game Client
  * Authentication Service
  * Matchmaking Service
  * Game Session
  * Game Server
  * Player Data Store
  * Analytics Processing

* Nắm được quy trình Matchmaking:

  * Tiếp nhận yêu cầu tìm trận
  * Kiểm tra thông tin người chơi
  * Đưa người chơi vào hàng đợi
  * Ghép các người chơi phù hợp
  * Khởi tạo Game Session
  * Phân bổ Game Server
  * Trả về địa chỉ kết nối

* Hiểu vòng đời của một phiên chơi trực tuyến từ khi đăng nhập đến khi kết thúc trận đấu.

* Nắm được nguyên tắc Game Server đóng vai trò là nguồn dữ liệu chính để xác nhận trạng thái trận đấu.

* Phân tích được các nhóm dữ liệu cần đồng bộ:

  * Vị trí người chơi
  * Trạng thái nhân vật
  * Điểm số
  * Sự kiện trong trận
  * Thời gian trận đấu
  * Kết quả cuối trận

* Nhận diện được các rủi ro kỹ thuật:

  * Độ trễ mạng
  * Mất kết nối
  * Trùng lặp sự kiện
  * Sai lệch trạng thái
  * Quá tải Game Server
  * Người chơi thoát giữa trận

* Hoàn thành sơ đồ kiến trúc sơ bộ cho hệ thống Backend Game Multiplayer.