---
name: tao-storyboard
description: "Use when turning a story or screenplay into panels, shots, camera instructions and image/video prompts."
---

# Storyboard và shot list

**Nguồn năng lực được tổng hợp:** InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Kịch bản đã chốt, phong cách hình ảnh, tỷ lệ khung hình và thời lượng.

## Các bước bắt buộc
1. Phân rã theo shot: ID, thời điểm tương đối, bối cảnh, hành động, nhân vật, vật phẩm, khung hình, chuyển động máy.
2. Tạo bộ nhân vật và bối cảnh nhất quán giữa khung: khuôn mặt, trang phục, đạo cụ, ánh sáng, màu sắc.
3. Viết prompt tạo ảnh/clip có positive/negative constraints và ghi lời thoại, SFX, gợi ý nhạc riêng.
4. Xác thực sự liên tục về hướng nhìn, khoảng cách, vị trí và nguyên nhân chuyển cảnh.
5. Xuất storyboard dạng bảng và shotcraft brief; chỉ nói là hình/video đã tạo khi thực sự dùng công cụ tương ứng.

## Đầu ra
storyboard.csv hoặc storyboard.md + shot-prompts.md.

## Tiêu chí nghiệm thu
Mỗi panel có nguồn scene, đúng nội dung canon và đủ thông tin để đội video dựng.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
