---
name: tang-3-bien-tap-loi-thoai
description: "Use in stage 3 for natural dialogue, character voice, emotionally engaging hook and ending, with Humanizer plus AI Copywriter techniques while preserving story facts."
---


# TẦNG 3 — Humanizer + AI Copywriter: biên tập tự nhiên, có sức hút

**Đầu vào:** screenplay tầng 2 + `STORY_LOCK` + mục tiêu cảm xúc/khán giả; **Đầu ra:** screenplay đã biên tập cùng `POLISH_LOG`.

1. **Giữ nội dung, sửa cách thể hiện:** tái viết thoại/VO để hợp tiếng Việt nói, độ tuổi, nghề, tình huống, quan hệ, trạng thái cảm xúc và giọng riêng từng nhân vật. Chỉ sửa dữ kiện diễn đạt khi không thay đổi ý nghĩa; tuyệt đối không tự sửa sự kiện đã khóa, thời điểm nhân vật biết một bí mật, lý do ra quyết định hay điểm kết.
2. **Humanizer có chọn lọc:** tìm lặp nghĩa, độc thoại giải thích, những câu chung chung/công thức, từ ngữ quảng cáo trong lời kể, cách nói “diễn thuyết”, 3 vế cân xứng rập khuôn, lời tóm tắt thay hành động, thoại giống nhau giữa các nhân vật. Giữ chỗ ngập ngừng, câu cụt, tiếng lóng, nhịp riêng khi **có lý do diễn xuất**; không ép văn xuôi/truyện dân gian phải “nói như quảng cáo hiện đại”. Không nhận diện AI bằng phỏng đoán chắc chắn.
3. **AI Copywriter đúng vai trò:** đánh giá khán giả lúc mở video đang cảm thấy gì, 3–10 giây đầu đưa tín hiệu thu hút nào *có thật trong câu chuyện*; dòng đầu dễ hiểu, cụ thể và gợi câu hỏi hợp lý; chuyển nhịp giữa cảnh không nhàm; cuối mang payoff, dư âm hoặc câu hỏi tùy thể loại. Viết tiêu đề/1 dòng giới thiệu chỉ khi có ích, tránh giật tít sai sự thật/ép CTA không thuộc nhân vật.
4. **Tăng tính điện ảnh:** thay câu “tôi rất tức giận” bằng cách đối đáp/hành động có sức diễn khi phù hợp, thêm khoảng lặng/đối tượng nhìn/nhịp phản ứng. Tránh âm thanh tràn chồng làm mất câu thoại.
5. **Bảo toàn hợp đồng:** phân loại từng sửa `WORDING_ONLY` hoặc `STORY_CHANGE`. Tự áp dụng chỉ `WORDING_ONLY`. Với `STORY_CHANGE`, nêu đề xuất và đợi sự cho phép nếu đụng canon; nếu user giao quyền sáng tác từ đầu, có thể sửa để tăng chất lượng nhưng phải đồng bộ lại toàn bộ story+scene+timing.
6. **Sync lại:** mỗi câu đổi độ dài cập nhật thời lượng dự kiến, shot nếu chuyển động/nhịp lời thay đổi, cue nhạc/tiếng có liên quan. Đọc thử thành tiếng trong tưởng tượng; nếu môi trường có TTS/audio được phép, có thể đo thực tế, không giả là đã thu âm.

## QC phân biệt người với nhãn “humanized”
- Không phóng đại “100% người viết”, “không thể bị phát hiện bởi AI detector”. Tiêu chí thực tế là câu nghe tự nhiên, không rỗng, có cá tính, và giữ ý định người viết.
- Đối thoại phải diễn được; tạo biến hóa dựa trên tâm lý nhân vật, không dùng một bộ quy tắc máy móc để xóa mọi câu cảm thán.

**Handoff:** `POLISH_LOG` gồm scene ID, chỗ chỉnh, lý do, tác động lời thoại/nhịp/timing, kết quả so với `STORY_LOCK`. Ở đầu ra cuối, chỉ trình bày bản đã chốt chứ không bắt người dùng ráp bản thô và bản sửa.
