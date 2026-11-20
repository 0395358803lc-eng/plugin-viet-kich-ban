---
name: canon-va-bo-nho
description: "Use when managing story continuity, project state, context budgets, knowledge retrieval or chapter fact records."
---

# Canon, trí nhớ và truy hồi

**Nguồn năng lực được tổng hợp:** InkOS; Webnovel Writer; Oh Story; Pagekin. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Bản nguồn chương đã duyệt và các thực thể cần theo dõi.

## Các bước bắt buộc
1. Tạo source-of-truth được phiên bản hóa; phân biệt file canonical và bản đọc/tra cứu suy ra (projection).
2. Sau mỗi chương trích sự kiện và trạng thái: nhân vật, quan hệ, thời gian, không gian, đồ vật, cảm xúc, biết/chưa biết, hooks.
3. Ghi event log với chương/đoạn làm bằng chứng, ID và state_revision; không sửa im lặng quá khứ.
4. Biên soạn context gọn cho chương N: tóm tắt 1–3 chương, bible, tuyến nhân vật liên quan, lời hứa đến hạn.
5. Khi có công cụ DB, có thể chỉ dẫn rebuild BM25/FTS5/vector; trong ChatGPT thuần chỉ lập bảng và tra trên những file đã thực sự đọc.
6. Phát hiện mâu thuẫn giữa nguồn canon và projection; nguồn gốc và revision quyết định, không trộn phán đoán AI.

## Đầu ra
canon.json, events.jsonl, context/chapter-N.md, state-change-proposal.md.

## Tiêu chí nghiệm thu
Không để nhân vật biết tương lai; bản dẫn xuất không vượt quyền nguồn chính.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
