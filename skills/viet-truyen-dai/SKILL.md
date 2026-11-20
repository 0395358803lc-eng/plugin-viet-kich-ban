---
name: viet-truyen-dai
description: "Use when writing a long-form novel chapter, serial chapter or a batch of long-form prose."
---

# Sáng tác tiểu thuyết dài kỳ

**Nguồn năng lực được tổng hợp:** InkOS; Oh Story; Webnovel Writer; Pagekin. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Dàn ý được duyệt, canon, chương gần nhất và mục tiêu số từ.

## Các bước bắt buộc
1. Chọn ngôi kể, điểm nhìn, lời thoại và giọng văn phù hợp người đọc; dùng dữ liệu liên quan, không ép toàn bộ bộ nhớ vào prompt.
2. Viết chương có chuỗi hành động–phản ứng–lựa chọn–hệ quả, đan xen miêu tả và thoại, tránh kể tóm tắt thay vì cảnh.
3. Kiểm soát độ dài bằng đếm từ/ký tự theo quy ước của tác giả; không báo đạt con số nếu chưa đếm.
4. Chạy kiểm tra sáng tác: lặp ý, văn AI, logic thời gian, biến đổi nhân vật, chi tiết trái canon, trùng lặp chương trước.
5. Lưu draft và review trước khi commit bản chính thức; chỉ tăng revision canon khi tác giả chấp thuận hoặc đã ủy quyền rõ.
6. Khi xuất nhiều chương, tuần tự commit từng chương; lỗi giữa chừng không được ghi trạng thái như đã hoàn thành cả lô.

## Đầu ra
chapters/chapter-XXXX.md + review + chapter-commit đề xuất.

## Tiêu chí nghiệm thu
Không gửi chương cắt ngang, lỗi bắt buộc xử lý trước final; lưu trạng thái và điểm tiếp tục.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
