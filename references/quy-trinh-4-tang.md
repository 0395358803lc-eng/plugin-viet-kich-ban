# Quy trình một lệnh — Viết-Lách → Kịch bản hoàn chỉnh

**Tiếp nhận:** "Làm kịch bản cho chủ đề X dài Y phút, nhân vật ..., cảm xúc ..."; kiểm tra brief → chọn giả định (nếu thiếu và không quan trọng) → chạy các tầng liên tục.

```text
Ý TƯỞNG / CHỦ ĐỀ / YÊU CẦU NGƯỜI DÙNG
                    │
                    ▼
             InkOS + Oh Story
 Cốt truyện — tình huống — nhân vật — cao trào — ý định thoại
                    │ STORY_LOCK
                    ▼
         Shuohao Skills + Drama Skills
 Cảnh — action — hội thoại đầy đủ — tạo hình/shot — âm thanh
                    │ SCENE_PACK
                    ▼
          Humanizer + AI Copywriter
 Chỉnh giọng riêng, nhịp và hook; giữ nội dung và continuity
                    │ POLISH_LOG
                    ▼
       QC G0–G5 + KỊCH BẢN HOÀN CHỈNH
 CỐT TRUYỆN + NHÂN VẬT + THOẠI + CẢNH + THỜI LƯỢNG + HÌNH/ÂM
```

**Nguyên tắc:** dừng sửa lỗi ngay tại tầng gây lỗi, chứ không dồn mọi thiếu sót vào tầng sau. Tầng 3 chỉ sửa cách kể, không tự ý tạo canon khác; khi có đổi mới cốt truyện được duyệt, cập nhật từ Story Lock, scene, duration tới hình/âm.

## Quy tắc bàn giao
- Tập trung vào bản kịch bản cuối, không bắt người dùng ghép bốn bộ đầu ra riêng.
- Hình ảnh và âm thanh gắn mã cảnh/shot/thời gian và **mô tả có thể sản xuất**, không cần mặc định tạo media.
- Thời lượng dự kiến là tổng của cảnh, không ngụ ý đã đo bằng ghi âm.
- Truyện dài/kịch bản dài: chia tập/episode rõ và xuất đủ theo phạm vi đã yêu cầu; kịch bản chưa đủ toàn bộ không được đóng nhãn hoàn tất.

## Nhánh thực thi trên máy chủ (v1.2.0)

Khi người dùng yêu cầu lưu kết quả trên máy chủ: `REMOTE_PRECHECK → PROJECT_DIR → REUSE_READONLY → bốn tầng → QC → WRITE_7_FILES → READBACK_7_FILES → REPORT`. Đây là **giao kịch bản văn bản**, không phải dựng phim hay chạy bộ source trên máy.

Tên và cấu trúc 7 file dùng thống nhất trong `references/remote-workspace.md`; nếu không có Remote Desktop Commander đã kết nối và quyền ghi, **báo chưa lưu máy chủ**, không tự nhận đã hoàn thành.
