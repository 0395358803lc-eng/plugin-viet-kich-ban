---
name: sua-ban-thao
description: "Use when rewriting chapters or passages following editorial notes, reader comments or explicit author changes."
---

# Sửa đổi, viết lại, chú thích

**Nguồn năng lực được tổng hợp:** Pagekin; InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Bản gốc, nhận xét, phạm vi sửa và quyền ghi đè.

## Các bước bắt buộc
1. Chốt phạm vi: sửa câu, mở rộng/thu gọn, chuyển thành thoại, sửa cảnh hay viết lại toàn chương.
2. Tạo change list theo từng đoạn, đánh dấu vấn đề nguồn và tác động đến chương sau.
3. Viết candidate riêng; đưa diff theo đoạn để tác giả chấp nhận/từ chối hoặc duyệt hàng loạt khi ủy quyền.
4. Khi mở lại chương đã chốt, phải cảnh báo các dữ kiện và blueprint phía sau bị ảnh hưởng.
5. Ghi lịch sử phiên bản, review sau sửa; chỉ thay bản chính khi đồng ý.

## Đầu ra
revision-proposal.md + revised-candidate.md + diff + impact list.

## Tiêu chí nghiệm thu
Không xóa bản gốc và không commit sửa ngoài phạm vi.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
