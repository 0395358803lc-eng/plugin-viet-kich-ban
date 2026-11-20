---
name: nhap-truyen-cu
description: "Use when importing an existing manuscript, txt/md/epub or an unfinished story for continuing work."
---

# Nhập bản thảo và tái dựng canon

**Nguồn năng lực được tổng hợp:** Pagekin; Oh Story; InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Tệp nguồn hoặc nội dung đã cung cấp, loại là bản tác giả hay tài liệu tham khảo.

## Các bước bắt buộc
1. Kiểm tra nguồn có thể đọc; phân biệt tác phẩm thuộc về người dùng với tài liệu tham chiếu của người khác.
2. Tách chương và ước lượng tiến độ; xây synopsis, nhân vật, thế giới, timeline, active hooks, unresolved items.
3. Không điền chỗ thiếu bằng phỏng đoán như dữ kiện canon; thêm unresolved question và source confidence.
4. Với bản gốc người dùng: có thể đưa chương vào finalized history và viết tiếp; với tài liệu tham khảo: chỉ dùng để phân tích kỹ thuật.
5. Đưa ra import report, mapping chương và những chỗ cần tác giả xác minh; hỗ trợ tiếp tục theo từng lô không lặp.

## Đầu ra
import-report.md + chapter-map.csv + canon-draft.json.

## Tiêu chí nghiệm thu
Tất cả dữ kiện có vị trí nguồn; không đánh đồng bản mẫu và bản quyền tác giả.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
