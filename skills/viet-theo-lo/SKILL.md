---
name: viet-theo-lo
description: "Use when writing multiple chapters, a serial batch or long tasks prone to interruption."
---

# Sáng tác nhiều chương có điểm tiếp tục

**Nguồn năng lực được tổng hợp:** InkOS; Webnovel Writer; Pagekin; Oh Story. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Khoảng chương, độ dài, giới hạn phiên, nguồn canon và quyền auto-commit.

## Các bước bắt buộc
1. Chia lô theo thời lượng/khối lượng thực tế: mỗi chương là transaction độc lập; không giả định có tiến trình chạy nền.
2. Ghi checklist và checkpoint ở đầu/cuối chương: outline, draft, review, revision, commit, backup.
3. Không đồng thời cập nhật hai phiên bản canon cạnh tranh; chương N+1 lấy state đã xác nhận của chương N.
4. Nếu vượt giới hạn phiên, xuất bàn giao recovery-pack chứa chapter target, canon revision, task state, links/paths.
5. Tại mỗi gate cung cấp đúng phần việc và yêu cầu phê duyệt khi cần sáng tác quan trọng hoặc ghi đè.

## Đầu ra
batch-plan.md + checkpoints.json + resume-instructions.md.

## Tiêu chí nghiệm thu
Báo số chương đã nghiệm thu thực tế, không đánh dấu toàn lô đạt khi lô còn dang dở.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
