---
name: mo-rong-xuat-sang-media
description: "Use when adapting novels into audio narration, animation scripts, episodic shorts or interactive media production briefs."
---

# Chuyển truyện thành nội dung đa phương tiện

**Nguồn năng lực được tổng hợp:** InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Truyện, số cảnh, mục tiêu video/audio, độ dài và tỷ lệ màn hình.

## Các bước bắt buộc
1. Tách phần có thể nhìn thấy/nghe được, lời thoại, lời dẫn, beat cảm xúc và cảnh hành động.
2. Chuyển truyện thành 4 tầng: scene script → shot list → voiceover text → production prompts/assets.
3. Gán ID cho nhân vật/đạo cụ/cảnh và nhất quán với canon, gợi ý đối thoại và SFX tại đúng scene.
4. Không khẳng định đã dựng video, tổng hợp TTS hay tạo ảnh nếu không có công cụ thực.
5. Bàn giao gói để công cụ bên ngoài như Remotion/GSAP/Three.js nhận xử lý khi người dùng yêu cầu.

## Đầu ra
media-adaptation-pack/ gồm screenplay, voiceover, shotlist, continuity-sheet.

## Tiêu chí nghiệm thu
Cảnh đồng bộ với bản thảo, thời lượng ước lượng có ghi giả định.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
