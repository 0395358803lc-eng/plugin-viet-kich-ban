---
name: kich-ban-4-tang
description: "Use when the user invokes Viết-Lách to create a complete film, animation, short drama or video screenplay from an idea or theme; orchestrates four scriptwriting stages into one deliverable."
---


# Quy trình mặc định Viết-Lách: KỊCH BẢN HOÀN CHỈNH QUA 4 TẦNG

## Quy tắc kích hoạt
Khi người dùng **gọi plugin Viết-Lách để viết kịch bản**, chuyển thể ý tưởng/truyện thành video/phim/hoạt hình, hoặc chỉ gọi Viết-Lách mà chưa nêu một nghiệp vụ khác, điều phối toàn bộ quy trình này. Nếu người dùng yêu cầu đích danh viết tiểu thuyết, nhập truyện, dịch, EPUB hoặc chỉ sửa một đoạn, ưu tiên kỹ năng chuyên dụng trong bộ 38 nền tảng; không ép biến tác phẩm văn xuôi thành kịch bản.

**Mục tiêu duy nhất:** giao **KỊCH BẢN HOÀN CHỈNH**, gồm cốt truyện + nhân vật + lời thoại thực tế + danh sách cảnh + thời lượng từng cảnh/tổng + hướng dẫn hình ảnh và âm thanh. Không coi chỉ có dàn ý, khung cảnh, prompt hoặc báo cáo là đã hoàn thành.

## Điểm vào khi làm việc trên máy chủ (v1.3.0)
Khi người dùng muốn kết quả nằm trên máy đích, **không bắt đầu tầng A ngay**: dùng `../luu-kich-ban-may-chu/SKILL.md` và đi đủ **R00 → R01 (nhận folder, kiểm tra/tạo `VIET_LACH_WORKSPACE`) → R02 (kiểm tra nhận diện nội dung cũ nếu có) → R02B (báo cáo & hỏi người dùng yêu cầu gì; dừng và chờ câu trả lời)**. Chỉ sau khi có yêu cầu nội dung cụ thể hoặc xác nhận đề bài đã nêu thì bắt đầu **tầng A → bốn tầng → QC**, và mới tiếp tục R04–R05 để ghi + đọc lại 7 tệp trên máy đích. Kết luận đúng theo R06 nếu thất bại. Không cài runtime/model để chỉ soạn văn bản; không coi bản thảo trong chat là đã lưu trên máy đích.

## A. Tiếp nhận ý tưởng/chủ đề/yêu cầu
- Ghi nhanh: chủ đề/premise, thể loại, thời lượng đích (giây/phút), đối tượng xem, nhân vật được yêu cầu, cảm xúc, kết thúc, tỷ lệ khung hình, hình thức (2D/3D/live action/kể chuyện), ngôn ngữ, mức độ lời dẫn, ràng buộc/canon.
- Thiếu chi tiết phụ thì chọn **giả định đề xuất, đánh dấu** rồi làm việc; không hỏi nhiều câu liên tục. Nếu chưa có *bất kỳ* chủ đề/đề bài nào và không đủ để viết, hỏi **một** câu về ý tưởng muốn kể. Giữ các giới hạn đã nêu; không tự bịa chi tiết có thật cho nội dung phi hư cấu.
- Nếu có file gốc, đọc tài liệu liên quan trước khi chuyển thể; không coi mô tả file như đã đọc file. Người dùng kiểm soát các quyết định thay đổi canon.

## B. Chạy 4 tầng theo đúng thứ tự, không nhảy tầng
1. **InkOS + Oh Story:** gọi `../tang-1-xay-dung-cau-chuyen/SKILL.md`. Tạo premise, logline, chủ đề, hồ sơ nhân vật, xung đột, trình tự nhân quả, mở đầu, điểm đảo chiều, cao trào, kết; chuyển giao `STORY_LOCK` được gắn phiên bản nội bộ. Dùng 38 kỹ năng nền: ý tưởng, kiến trúc truyện, nhân vật, canon, foreshadow, kiểm toán, biên tập.
2. **Shuohao Skills + Drama Skills:** gọi `../tang-2-viet-kich-ban-canh/SKILL.md` và `../thiet-ke-hinh-anh-am-thanh/SKILL.md`. Chuyển cốt truyện thành screenplay có thể sản xuất: SCENE-ID, bối cảnh, hành động nhìn/nghe được, nhịp tình huống, đầy đủ lời thoại, cảnh mở/đóng, shot gợi ý, âm thanh và ngân sách giây; đồng bộ theo `STORY_LOCK`.
3. **Humanizer + AI Copywriter:** gọi `../tang-3-bien-tap-loi-thoai/SKILL.md`. Tự nhiên hóa lời thoại theo giọng riêng từng nhân vật; tăng độ hấp dẫn thực chất của ấn tượng mở, tiết tấu và cái kết; **không đổi sự kiện, mục đích, trạng thái nhân vật, nhân quả, thời lượng đã khóa nếu chưa đồng bộ lại**.
4. **Kịch bản hoàn chỉnh + QA:** gọi `../nghiem-thu-kich-ban/SKILL.md`. Soát 6 hạng mục bắt buộc, đồng nhất hình/âm, đối chiếu thời lượng, sửa lỗi và bàn giao **một bản kịch bản từ đầu đến cuối** theo `../../references/kich-ban-template.md`.

## C. Hợp đồng dữ liệu liên tầng
- `BRIEF`: nguồn ý tưởng + các ràng buộc và giả định + thời lượng đích.
- `STORY_LOCK`: logline, tình tiết cốt lõi, nhân vật, tri thức từng nhân vật, tình trạng đạo cụ, sequence cảnh, cao trào và kết thúc, version; các quyết định của tác giả ưu tiên.
- `SCENE_PACK`: `SC001...SCnnn`, tiêu đề, INT/EXT, nơi/chốc, mục tiêu kịch tính, đầu-cuối cảnh, người tham gia, từng dòng ACTION/DIALOGUE/VO/OS/SFX/MUSIC, duration_s, thời điểm bắt đầu/kết thúc, hình/âm.
- `POLISH_LOG`: vùng thoại được biên tập, lý do, xác nhận không đổi nội dung có tính canon; thay đổi nhịp thì cập nhật ngân sách thời lượng và shot/âm thanh liên quan.
- `DELIVERY`: tập kịch bản toàn vẹn + bảng cảnh/timing + định hướng hình/âm + bản QC ngắn; nếu có quyền tạo tệp, có thể xuất bản `.md` và bảng `.csv`. **Không tuyên bố tệp hay media đã được tạo khi thực tế chỉ viết trong chat.**

## D. Những thứ không được nhầm lẫn
- Đây là **tổng hợp phương pháp viết**, không đồng nghĩa chạy source InkOS, Oh Story, Shuohao, Drama, Humanizer, AI Copywriter hay các script báo cáo/kiểm tra của dự án nguồn.
- Không tự gọi API trả phí, tạo ảnh/video/TTS hay xuất bản nếu người dùng chỉ yêu cầu kịch bản. Hướng dẫn hình/âm và prompt tham chiếu **không phải** hình/âm đã được sản xuất.
- Các luật con có thể mâu thuẫn (ví dụ chuẩn lời thoại rất ngắn của một công cụ) thì **thời lượng, thể loại, ngôn ngữ, tác phẩm của người dùng** và khả năng quay/hoạt hình là tiêu chuẩn ưu tiên; xem giới hạn dự án nguồn là khuyến nghị theo ngữ cảnh.

## Đầu ra bắt buộc
Một tài liệu theo thứ tự **thông tin dự án → cốt truyện → bảng nhân vật → bảng cảnh và timecode → kịch bản từng cảnh (ACTION/DIALOGUE/VO/OS) → hướng dẫn hình/âm cho mỗi cảnh → QC**. Nếu độ dài khiến phải chia nhiều lượt, nói rõ phạm vi đã làm và chưa làm; không đánh dấu toàn bộ kịch bản ĐẠT khi còn thiếu cảnh.
