---
name: workflow-node-tu-chinh
description: "Use when designing editable staged AI workflows with nodes, prompts, variables and review gates."
---

# Thiết kế workflow tạo truyện dạng node

**Nguồn năng lực được tổng hợp:** AI Novel Generator; InkOS; Pagekin. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Tác vụ sáng tác, node hiện có, yêu cầu đầu vào/đầu ra, mô hình hoặc công cụ.

## Các bước bắt buộc
1. Mô hình hóa DAG: tạo ý tưởng, worldbook, characters, factions, volumes, arcs, scenes, plans, prose, checks.
2. Với mỗi node định nghĩa inputs, prompt contract, structured outputs, model assignment và lỗi có thể xảy ra.
3. Tạo gate xác nhận của tác giả trước lưu các entity và chương chính thức.
4. Thêm checkpoint và idempotency để chạy lại không nhân bản chương hoặc ghi đè canon.
5. Chỉ lập mô tả tương thích phần mềm gốc; không nói có visual canvas đang chạy trừ khi thực sự kết nối app.

## Đầu ra
workflow-dag.md + node-contracts.json + acceptance-plan.md.

## Tiêu chí nghiệm thu
DAG không vòng phụ thuộc và có bước phục hồi/duyệt rõ ràng.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
