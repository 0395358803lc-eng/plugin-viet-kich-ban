---
name: thiet-lap-the-gioi
description: "Use when defining worldbuilding, magic/power systems, politics, technology, locations, items or constraints."
---

# Worldbook và hệ thống quy tắc

**Nguồn năng lực được tổng hợp:** AI Novel Generator; Pagekin; InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Concept, thời đại, quy luật thế giới và giới hạn tác giả.

## Các bước bắt buộc
1. Tách worldbook thành bối cảnh, lịch sử, vị trí, vật phẩm, hệ năng lực, luật giới, logic nguồn lực và cấm kị.
2. Tạo bảng nguyên nhân–giới hạn–hệ quả cho mỗi quy tắc; nêu ngoại lệ có bằng chứng và chi phí sử dụng.
3. Thiết kế phe phái, địa điểm, vật phẩm thành thực thể có ID ổn định và thuộc tính gắn với chương hiệu lực.
4. Phân loại canon xác nhận, giả thuyết tác giả, và thông tin mà nhân vật/độc giả biết.
5. Kiểm tra tính tương thích với plot và tạo danh sách mâu thuẫn cần tác giả quyết định.

## Đầu ra
worldbook.md + entities.json + world_rules.md.

## Tiêu chí nghiệm thu
Không để quy tắc bị phá vô cớ hoặc nhân vật dùng vật phẩm/năng lực chưa sở hữu.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
