---
name: thiet-ke-hinh-anh-am-thanh
description: "Use when creating production-ready visual, shot, staging, voiceover, sound design and music guidance for each screenplay scene, without generating media."
---


# Thiết kế hình ảnh và âm thanh đồng bộ từng cảnh

**Đầu vào:** cảnh và thoại từ tầng 2; **Đầu ra:** hướng dẫn để họa sĩ/đạo diễn/AI animation/TTS/dựng phim có thể thực hiện. Đây là **chỉ dẫn**, không phải video, ảnh hay audio đã render.

## Thiết kế hình ảnh
- Trước tiên chốt tỷ lệ ảnh (9:16, 16:9 hoặc theo người dùng), chất liệu hình (2D, 3D, live-action, motion graphics), màu, ánh sáng, mức độ hoạt hình. Nếu chưa rõ, đề xuất một phương án có nhãn GIẢ ĐỊNH; không đóng khung toàn bộ phim thành một hình thức mặc định.
- Mỗi cảnh: nêu LOCATION/SET, tạo hình nhân vật và trạng thái đạo cụ, vị trí tương đối, ánh sáng, ít nhất 1 shot có mục đích kể chuyện: `SHOT-SC001-01`, cỡ cảnh, góc máy, camera đứng/di chuyển, tiêu điểm, hành động mở–đóng và thời lượng ước tính. Nếu scene dài, chia shot đủ để quay/dựng.
- Duy trì continuity: khuôn mặt, trang phục, đạo cụ, tay cầm, hướng nhìn và nguồn sáng. Chuyển cảnh/ánh sáng thay đổi do thời gian/nội dung phải có lý do; đừng khóa cứng khi cảnh hồi tưởng có chủ đích.
- Với AI video, ưu tiên hành động đơn giản, dễ nhìn và có điểm bắt đầu/kết thúc; hướng dẫn khác nhau giữa **khung hình tham chiếu**, **shot** và **mô tả chuyển động**. Không tự tạo prompt cụ thể cho vendor nếu không được yêu cầu.

## Thiết kế âm thanh
- **DIALOGUE:** nguyên văn từng lời thoại cùng nhân vật phát ngôn, VO/OS nếu có, thái độ, chỗ nghỉ/nhấn; cung cấp bản thoại đọc riêng khi được yêu cầu.
- **SFX:** hành động nghe được (bước chân, tiếng cốc, cửa mở, chuông...), định vị trên timecode, mức độ nổi, cắt/duck nhạc khi cần.
- **AMBIENCE:** âm trường bối cảnh (đêm, gió, xe xa...), chỉ bật nếu phù hợp không gian.
- **MUSIC:** mood, nhịp, nhạc cụ, điểm vào/ra, khi nào giảm hoặc im để nhường thoại; không chèn nhạc triền miên nếu nhịp kịch tính cần khoảng lặng. Nhạc được mô tả nguyên gốc, không yêu cầu sao chép tác phẩm có bản quyền.
- Chú ý soundbridge/cut, diegetic/phi diegetic và sự thay đổi vật lý. Khi sửa hành động, rà lại cue âm thanh gắn với hành động đó.

## Giao nhận per-scene
`visual`: mã shot; frame mở, frame đóng; diễn xuất/di chuyển; loại cảnh; máy quay; ánh sáng; continuity.
`audio`: từng cue loại thoại/VO/SFX/ambience/music, thời điểm tương đối, mục đích, ưu tiên trộn.
**Bắt buộc:** cue âm không vượt thời lượng cảnh, shot không lệch kịch bản, không phát sinh hình/âm được gọi là “đã tạo” khi chưa có media.
