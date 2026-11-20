---
name: quan-ly-phien-ban
description: "Use when saving drafts, finalizing, reopening chapters, recovering deleted work or managing backups."
---

# Phiên bản, sao lưu và hoàn nguyên

**Nguồn năng lực được tổng hợp:** Pagekin; InkOS; Webnovel Writer. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Danh sách chương, revision, trạng thái draft/final, yêu cầu khôi phục.

## Các bước bắt buộc
1. Định danh bản nháp, review, final, reopen với revision và thời điểm rõ ràng; không lấy số phiên bản ngẫu nhiên.
2. Chốt chương khi qua nghiệm thu, tạo snapshot bất biến hoặc lịch sử thay đổi trước sửa.
3. Xóa mềm đưa vào Trash khi có filesystem; nêu tác động tới chương kế cận và cho phép restore.
4. Khôi phục không ghi đè nếu phát hiện xung đột phiên bản, lập phương án merge.
5. Backup manifest kèm checksum và cấu trúc tệp; xác minh bản sao có thể đọc lại.

## Đầu ra
version-log.jsonl + backups/ + trash/ nếu có quyền file.

## Tiêu chí nghiệm thu
Khôi phục kiểm tra bản nguồn và revision, không xóa vĩnh viễn khi chưa được phép.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
