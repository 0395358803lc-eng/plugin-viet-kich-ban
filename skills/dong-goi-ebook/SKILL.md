---
name: dong-goi-ebook
description: "Use when compiling a complete manuscript into EPUB and other book delivery formats."
---

# Biên soạn sách và EPUB

**Nguồn năng lực được tổng hợp:** GPT-Author; InkOS; Pagekin. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Các chương được duyệt, thứ tự, tác giả, tiêu đề, ảnh bìa tùy chọn.

## Các bước bắt buộc
1. Chuẩn hóa metadata, mục lục, thứ tự chương, mã UTF-8 và kiểu đầu chương.
2. Tạo bản thảo sạch, tránh đưa ghi chú nội bộ, secret hoặc prompt vào sách.
3. Nếu có công cụ file/python và thư viện epub, sinh EPUB; nếu không, xuất bản thảo/cấu trúc HTML và báo chưa dựng EPUB.
4. Kiểm tra CRC/zip entries, nav, spine, chapter contents, số chương, unicode, mở thử bằng thư viện hỗ trợ nếu có.
5. Ghi báo cáo đóng gói và đường dẫn tệp thực sự tồn tại.

## Đầu ra
book.epub khi xây dựng thành công; hoặc export-ready manuscript.

## Tiêu chí nghiệm thu
File EPUB kiểm tra đọc/đủ chương trước khi tuyên bố hoàn tất.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
