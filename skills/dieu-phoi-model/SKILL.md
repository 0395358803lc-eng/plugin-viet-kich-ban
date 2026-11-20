---
name: dieu-phoi-model
description: "Use when mapping writing tasks to LLM agents/models, planning local model workflows or adapting external novel-generation systems."
---

# Thiết kế pipeline AI và mô hình

**Nguồn năng lực được tổng hợp:** InkOS; AI Novel Generator; Pagekin; Webnovel Writer. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Hạ tầng hiện có, yêu cầu chất lượng/chi phí, runtime và model khả dụng.

## Các bước bắt buộc
1. Tách tác vụ Planner, Writer, Reviewer, Continuity Auditor, Fact Extractor, Editor, Translator, Cover Prompt.
2. Tạo bảng nguồn vào–đầu ra–khóa kiểm tra–điểm phải duyệt–mô hình đề xuất (không cần API ngoài nếu ChatGPT xử lý trực tiếp).
3. Nếu gắn với AI Novel Generator, lưu ý MongoDB replica set cần cho transaction và có các node workflow tùy chỉnh; không gọi là sẵn chạy trong ChatGPT.
4. Nếu gắn Pagekin, lưu ý mô hình/khóa được cấu hình bởi người dùng hoặc Ollama local; không tự download model.
5. Tối ưu context theo truy hồi có chứng cứ, dự trù phân đoạn dài, fallback khi thiếu embedding/reranker.
6. Không tiết lộ API key trong tài liệu hoặc tự ý dùng trả phí.

## Đầu ra
pipeline-plan.md + model-matrix.md + dependencies checklist.

## Tiêu chí nghiệm thu
Nêu rõ thực tế đã nối model/API hay chỉ mới thiết kế; tránh yêu cầu ngoài quyền.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
