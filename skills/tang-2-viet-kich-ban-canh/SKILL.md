---
name: tang-2-viet-kich-ban-canh
description: "Use in stage 2 to transform the locked story into scene-based performable film/animation/drama scripts based on Shuohao novel-script and Drama short-drama writing."
---


# TẦNG 2 — Shuohao + Drama: biên kịch theo cảnh và thời lượng

**Nguồn ý tưởng:** Shuohao `novel-outline`, `novel-script`, `novel-characters`, `novel-art`, `novel-staging`, `novel-storyboard` và Drama `short-drama-develop`, `short-drama-write`, `short-drama-assets`, `short-drama-storyboard`, `short-drama-review`. Áp dụng phương pháp độc lập, không tuyên bố chạy tool kiểm định của source.

**Đầu vào:** `STORY_LOCK`, `BRIEF`; **Đầu ra:** `SCENE_PACK` có nội dung có thể diễn/thu âm/dựng.

1. **Chuyển beat thành cảnh thực:** `SC001...` kèm INT/EXT, địa điểm, thời điểm trong truyện, nhân vật hiện diện, trạng thái đầu → trạng thái cuối, mục tiêu và `Bxx` nhận trách nhiệm; không bẻ nhánh nguyên nhân của `STORY_LOCK`.
2. **Hành động phải nhìn/nghe được:** viết từng nhịp ACTION là cử chỉ, di chuyển, biểu cảm có thể diễn, phản ứng và thay đổi vật/không gian. Chuyển tâm lý trừu tượng thành hành vi/sự kiện phù hợp hình thức 2D, 3D hay live-action. Cân bằng lời thoại và hình; không để video thành “radio có ảnh tĩnh” khi người dùng cần hoạt hình.
3. **Lời thoại hoàn chỉnh:** mỗi câu có `NHÂN_VẬT (cảm xúc/diễn xuất): "..."`; quy định VO/OS rõ nếu là thuyết minh/ngoài khung. Nhân vật nói theo mục tiêu và cá tính, có đối đáp, ngắt nhịp, im lặng. Không thay bằng “hai người tranh cãi”. Chỉ chia câu quá dài khi lợi cho diễn xuất, không áp cứng giới hạn chữ tiếng Trung vào tiếng Việt.
4. **Tài sản nhất quán:** mô tả nhân vật, quần áo, đạo cụ, địa điểm, hướng nhìn/vị trí; nếu đạo cụ chuyển tay hay nhân vật đổi chỗ thì có nhịp diễn hợp lệ. Khóa đặc điểm không đổi giữa các cảnh.
5. **Dự toán thời lượng thực dụng:** mỗi cảnh có `duration_s` nguyên dương, timecode mở–đóng liên tục, ngân sách VO/thoại, hành động, im lặng và chuyển cảnh. Không cộng lời thoại và hành động hai lần khi chúng xảy ra đồng thời. Đọc thoại tiếng Việt chỉ ước lượng theo giọng/nhịp; nếu chưa đo/thu voice, gắn “dự kiến”.
6. **Gắn hình và âm:** giao `../thiet-ke-hinh-anh-am-thanh/SKILL.md`; mỗi cảnh phải có shot intent và audio cues khớp các hành động/thoại thật. Shot list có thể đưa chi tiết hơn nhưng không thay screenplay; user chỉ yêu cầu kịch bản thì không tự biến thành tài liệu prompt vendor phức tạp.
7. **Kiểm tra phần giao:** mọi scene ID có nội dung, nhân vật có mặt hợp lệ, có bước dẫn tới cao trào, người chưa biết sự thật không nói như đã biết; kịch bản không được kết thúc ở giữa một cảnh hoặc bỏ phần thoại cuối.

**Định dạng khuyến nghị:**

```
SC003 | 00:35–01:06 | 31 giây | INT. PHÒNG KHÁCH – ĐÊM
Mục tiêu cảnh: nhân vật B phát hiện dấu vết, A phải ứng biến.
ACTION: A đặt cốc xuống rồi nhìn ra cửa; B dừng ngay ngưỡng cửa.
B (ngờ vực): "..."
A (cố bình tĩnh): "..."
SFX: ...
VISUAL: ...
MUSIC/AMBIENCE: ...
```

Ví dụ chỉ minh họa cấu trúc, không phải nội dung giao người dùng. Chi tiết thời lượng, chuyển cảnh và khung hình theo `../../references/kich-ban-template.md`.
