---
name: khoi-tao-du-an
description: "Use when starting a new novel, webnovel, series, screenwriting or other organized writing project."
---

# Khởi tạo dự án viết

**Nguồn năng lực được tổng hợp:** Webnovel Writer; Pagekin; AI Novel Generator; InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Thể loại, độc giả, ngôn ngữ, nền tảng, ý tưởng, độ dài hoặc khoảng lựa chọn.

## Các bước bắt buộc
1. Xây brief: chủ đề, thông điệp, giọng kể, ngôi kể, quy mô chương, nhịp ra chương, điều cấm và tiêu chí thành công.
2. Tạo thư mục VIET_LACH_WORKSPACE/<slug> nếu được phép ghi file, hoặc xuất mẫu thư mục nếu chat không có quyền ghi.
3. Tạo hồ sơ tác phẩm, author_intent, worldbook, dàn ý, các thư mục nhân vật, chương, review, tracking, exports, backups.
4. Khởi tạo canon rỗng có revision, sổ sự kiện, danh sách câu hỏi chưa quyết; không biến gợi ý AI thành sự thật tác phẩm khi chưa xác nhận.
5. Phân biệt giai đoạn setup, plan, write, review, finalize; ưu tiên mở khóa từng giai đoạn sau khi có đủ dữ liệu.
6. Xuất giấy xác nhận khởi tạo và 3 bước tiếp theo.

## Đầu ra
project-brief.md, story-bible.md, outline/, characters/, chapters/, reviews/, tracking/, exports/.

## Tiêu chí nghiệm thu
Kiểm tra tên file an toàn, mã hóa UTF-8, thư mục hiện hữu; không xóa hoặc ghi đè dự án cũ.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
