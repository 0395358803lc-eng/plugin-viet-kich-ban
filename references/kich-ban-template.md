# Hợp đồng giao sản phẩm — KỊCH BẢN HOÀN CHỈNH

Dùng template này làm **khung chất lượng và thứ tự**, không biến thành dàn ý rỗng: mọi mục phải có thông tin thật của câu chuyện. Không hiện placeholder trong bản bàn giao.

## 1. Thông tin tác phẩm
- **Tên**, thể loại, cảm xúc, khán giả, tỷ lệ hình (nếu chốt), hình thức tạo hình, ngôn ngữ, thời lượng đích, thời lượng kịch bản dự kiến, tình trạng bản nháp/được chốt.

## 2. Cốt truyện
- **Logline:** một câu; **Tóm tắt toàn bộ:** đầu, xung đột, bước ngoặt, cao trào, kết; **thông điệp/cảm xúc chủ đạo**. Tác giả chưa chốt thì phân biệt đề xuất.

## 3. Nhân vật
| ID | Tên | Vai trò/mục tiêu | Ngoại hình và tạo hình | Giọng nói, cách xưng hô | Cung cảm xúc |
|---|---|---|---|---|---|

## 4. Danh sách cảnh và thời lượng
| Cảnh | Timecode (từ–đến) | Giây | Nội/ngoại–bối cảnh | Chuyển biến/chức năng | Nhân vật |
|---|---|---:|---|---|---|

Bắt đầu ở 00:00; cảnh kế bắt đầu đúng lúc cảnh trước kết thúc; cộng tất cả cảnh phải bằng thời lượng kịch bản đã giao. Nếu phân đoạn đồng thời (đối thoại trên hình) thì **không cộng lặp**.

## 5. Kịch bản chi tiết từ đầu đến cuối
### SC001 — INT./EXT. ĐỊA ĐIỂM — THỜI ĐIỂM — [00:00–00:XX, XX giây]
**Mục tiêu:** điều gì thay đổi khi cảnh kết thúc.

**HÌNH ẢNH / ACTION:** mô tả đầy đủ ai ở đâu, đang làm gì, thể hiện cảm xúc ra sao, điểm vào/ra cảnh. Không ghi “nhiều cảnh sinh hoạt” rồi bỏ trống hành động.

**LỜI THOẠI / VO / OS (nguyên văn):**

**NHÂN VẬT (cách nói/cảm xúc):** “Lời thoại nguyên văn.”

**[VO — người đọc]** “Lời dẫn thực tế, nếu có.”

**HƯỚNG DẪN HÌNH:** lựa chọn khung hình, cỡ cảnh, shot ID, góc máy/động tác máy, ánh sáng, tính liên tục trang phục/đạo cụ, điểm nối cảnh. Khi cần từng shot: `SHOT-SC001-01 — 00:00–00:XX — ...`.

**HƯỚNG DẪN ÂM:** voice/tâm trạng, ambience, SFX kèm thời điểm tương đối, âm nhạc (cảm xúc, nhạc cụ, điểm vào/ra/duck), im lặng có chủ đích; không tự bịa tệp media đã tồn tại.

**TIẾP:** chuyển sang cảnh nào và nhịp nối quan trọng.

[LẶP CHO MỌI CẢNH TỚI KẾT THÚC — không dùng dòng này trong bản chính thức]

## 6. QC ngắn
Bảng `G0...G5` với ĐẠT/CẦN SỬA/CHƯA KIỂM CHỨNG và 1 câu bằng chứng; tổng thời lượng + sai số so với mục tiêu, xác định các giả định có thể sửa.

## Timing
- Thời lượng biểu diễn là **dự tính** khi chưa có ghi âm, diễn thử hoặc footage. Thoại tiếng Việt có thể ước lượng theo nhịp nói dự kiến rồi kiểm tra chéo với thời gian hành động; không bê tốc độ đọc ký tự tiếng Trung sang tiếng Việt.
- Định dạng timecode `MM:SS` dưới 60 phút; `HH:MM:SS` trên 60 phút. Thời gian cảnh được tính từ 0 và toàn bộ chính xác theo `duration_s`; không có gap ẩn.
- Mục tiêu khác tổng ước tính: trước hết chỉnh nội dung/độ dài cảnh, không làm giả số giây. Khi bất khả thi, ghi rõ mức sai lệch.
