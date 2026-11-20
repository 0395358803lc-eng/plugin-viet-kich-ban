---
name: truyen-tuong-tac
description: "Use when designing interactive films, choose-your-path narratives or branching dialogue with multiple endings."
---

# Truyện phân nhánh và phim tương tác

**Nguồn năng lực được tổng hợp:** InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Thế giới, người chơi, mục tiêu, điều kiện nhánh và độ dài trải nghiệm.

## Các bước bắt buộc
1. Định nghĩa các node có ID ổn định, nội dung cảnh, lựa chọn, điều kiện mở khóa, biến cờ, hệ quả.
2. Vẽ đồ thị nhánh; quản lý nhánh hội tụ, nhánh chết, vòng lặp, tài sản hình/âm nhân vật qua các nhánh.
3. Define state transitions rõ ràng, kiểm tra mọi lựa chọn có đường đi, mọi ending có thể đạt tới.
4. Tạo mô tả cảnh quay/cảnh đồ họa cho từng node theo kịch bản thống nhất.
5. Chạy thử ít nhất ba hành trình người chơi đại diện, ghi lỗi logic và kết cục.

## Đầu ra
branch-graph.md + nodes.json + test-paths.md.

## Tiêu chí nghiệm thu
Không có nhánh không thể tới, biến mất không lý do hay ending thiếu điều kiện.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
