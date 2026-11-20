---
name: the-gioi-nhap-vai
description: "Use when developing an open-world roleplay, quest world, character-driven simulation or interactive fiction session."
---

# Thế giới mở và nhập vai bằng văn bản

**Nguồn năng lực được tổng hợp:** InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** World contract, nhân vật/đồ vật, quy tắc thời gian, hành động người chơi.

## Các bước bắt buộc
1. Tạo thế giới xác định thời gian, phạm vi tri thức, quyền của nhân vật NPC, đồ dùng, bằng chứng và mối quan hệ.
2. Mỗi lượt người chơi: lấy state hiện tại → xét hành động hợp lệ → cập nhật thời gian/địa điểm/NPC → mô tả hệ quả.
3. Chỉ cho NPC hành động theo thông tin chúng biết; không thay đổi đồ vật/địa điểm tức thời vô cớ.
4. Ghi state delta và sổ sự kiện, có thể phục hồi lượt trước.
5. Tạo prompt ảnh tình huống phù hợp canon nếu được yêu cầu, nhưng không giả vờ hình đã render.

## Đầu ra
world-contract.md + play-state.json + transcript.md.

## Tiêu chí nghiệm thu
Mọi thay đổi state tái hiện được; lựa chọn không phá luật thế giới.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
