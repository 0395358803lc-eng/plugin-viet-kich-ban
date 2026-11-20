---
name: doctor-du-an
description: "Use when auditing a writing workspace or investigating missing files, invalid state, stalled writing jobs or sync errors."
---

# Kiểm tra sức khỏe dự án và phục hồi

**Nguồn năng lực được tổng hợp:** Webnovel Writer; InkOS; Pagekin; AI Novel Generator. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Đường dẫn dự án nếu có quyền truy cập, log và manifest liên quan.

## Các bước bắt buộc
1. Chạy read-only trước: xác minh project root, file thiết yếu, bản thảo, JSON/CSV, revision, nhánh chưa commit.
2. Tìm chapter commit thiếu, state/index/summaries không cùng phiên bản, vòng lặp workflow thất bại, tệp đang bị khóa.
3. Phân cấp: lỗi dữ liệu, thiếu quyền, lỗi công cụ, dữ liệu chỉ là bản dự phóng; đề xuất sửa ít tác động nhất.
4. Không cài dependency, sửa môi trường, chạy migration hoặc xóa dữ liệu nếu chưa được ủy quyền.
5. Báo cáo ĐẠT/CẦN SỬA/CHƯA XÁC MINH với các lệnh chỉ đọc đã thực hiện hoặc thủ tục để người dùng chạy.

## Đầu ra
doctor-report.md + repair-plan.md.

## Tiêu chí nghiệm thu
Không hứa kiểm thử chạy nếu chỉ mới đọc tài liệu.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
