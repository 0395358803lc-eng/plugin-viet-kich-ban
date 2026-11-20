---
name: quan-ly-foreshadow
description: "Use when tracking story clues, setups, payoffs, cliffhangers and overdue story threads."
---

# Theo dõi伏笔 và các lời hứa cốt truyện

**Nguồn năng lực được tổng hợp:** Pagekin; Oh Story; Webnovel Writer; InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Dàn ý, các chương đã viết và danh mục hook.

## Các bước bắt buộc
1. Đặt ID cho từng tuyến/foreshadow; ghi chương gieo, chủ sở hữu, trạng thái, chương dự kiến trả, mức độ ưu tiên.
2. Chia trạng thái open, progressing, deferred, resolved; phân biệt đã xác nhận trả với AI gợi ý trả.
3. Tại chương N hiển thị overdue, due, scheduled và new; đề xuất cách đẩy tiến trình hợp lý.
4. Khi định dời chapter due hoặc hủy hook, đưa tác giả quyết định nếu ảnh hưởng dài hạn.
5. Rà soát hậu chương: cái gì đã gieo/tiến/thu hồi, có lời hứa treo hay không.

## Đầu ra
hooks.csv + chapter-N-hook-check.md.

## Tiêu chí nghiệm thu
Mỗi payoff có nguồn thực tế; không đóng hook chỉ vì nhân vật nói sẽ làm.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
