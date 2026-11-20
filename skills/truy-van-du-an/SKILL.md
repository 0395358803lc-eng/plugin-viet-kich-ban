---
name: truy-van-du-an
description: "Use when querying story state, entity relationships, project progress, plot threads or creating a read-only dashboard summary."
---

# Tra cứu tiến độ và quản trị tác phẩm

**Nguồn năng lực được tổng hợp:** Webnovel Writer; Pagekin; AI Novel Generator. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Tệp trạng thái, outline, bản thảo và nhật ký tiến độ đã truy cập được.

## Các bước bắt buộc
1. Tổng hợp toàn cảnh: số chương, số chương chốt, word count thực, characters, open threads, review còn lỗi.
2. Tra cứu theo tên nhân vật/ID/sự kiện/chương/bí mật và chỉ hồi đáp từ dữ liệu đã đọc.
3. Tạo chart/tables/relationship graph đọc-only từ dữ liệu nguồn khi công cụ hỗ trợ.
4. Không nhầm UI dashboard desktop/web có sẵn với tính năng native của plugin skills-only.
5. Chỉ dẫn cách mở dashboard gốc nếu người dùng đã cài dự án tương ứng; không khởi chạy chưa có quyền.

## Đầu ra
status-report.md + query-answer có nguồn; bảng hoặc sơ đồ theo dữ liệu.

## Tiêu chí nghiệm thu
Không tạo số liệu tiến độ giả; phản ánh lỗi đồng bộ và thiếu dữ liệu.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
