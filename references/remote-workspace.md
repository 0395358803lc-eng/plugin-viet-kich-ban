# Viết-Lách trên máy chủ — hợp đồng vận hành v1.3.0

## Mục tiêu, điều kiện tối thiểu
- **ChatGPT** sinh, kiểm tra và biên tập toàn bộ kịch bản bằng bộ kỹ năng Viết-Lách.
- **Remote Desktop Commander** (khi đã được kết nối và cho phép ghi) là phương tiện xem thư mục, tạo và đọc lại tệp trên máy chủ người dùng. Hai plugin/công cụ phải thực sự có sẵn trong phiên; không tự suy ra rằng gọi Viết-Lách sẽ tự kích hoạt quyền của app khác.
- Máy chủ chỉ lưu trữ văn bản: **không bắt buộc cài Python, Node.js, FFmpeg, Remotion, CUDA, model AI hay các ứng dụng nguồn**. Nếu cần xuất Word/PDF hoặc dựng phim thì đó là phạm vi khác, cần đánh giá sau.
- Không đòi quyền admin hoặc cài đặt toàn hệ thống. Không truy cập ngoài vùng được cấp phép.

## Thứ tự khi sử dụng — ưu tiên tuyệt đối việc hỏi yêu cầu sau khi kiểm tra workspace

```text
GỌI VIẾT-LÁCH VÀ CHỌN MÁY (xác minh Remote Desktop Commander)
  └─ NHẬN SELECTED_DIR — thư mục người dùng muốn làm việc
      └─ chuẩn hóa WORKSPACE_ROOT
          ├─ SELECTED_DIR == VIET_LACH_WORKSPACE? → dùng thư mục đó
          ├─ SELECTED_DIR đã thuộc VIET_LACH_WORKSPACE? → dùng workspace cha
          ├─ SELECTED_DIR/VIET_LACH_WORKSPACE đã có?
          │      └─ CÓ → READ-ONLY nhận diện danh sách dự án/dữ liệu cũ
          └─ CHƯA CÓ → tạo đúng SELECTED_DIR/VIET_LACH_WORKSPACE
                        → xác minh thư mục được tạo; không tạo dự án con
                         ↓
               BÁO KẾT QUẢ MỚI/CŨ VÀ NỘI DUNG NHẬN DIỆN
                         ↓
          HỎI: “Bạn muốn Viết-Lách thực hiện yêu cầu gì trong thư mục này?”
                         ↓
                  DỪNG CHỜ NGƯỜI DÙNG
                         ↓
           NHẬN YÊU CẦU → CHỌN DỰ ÁN / LẬP BRIEF
                         ↓
             4 TẦNG SÁNG TÁC → QC G0–G5
                         ↓
           LƯU 7 TỆP → ĐỌC LẠI TRÊN MÁY ĐÍCH → NGHIỆM THU
```

**Quy tắc bắt buộc:** Quy trình hỏi yêu cầu **sau khi** tìm hoặc tạo `VIET_LACH_WORKSPACE`; không hỏi ý tưởng sáng tác khi mới chọn máy, và không tự suy đoán yêu cầu từ dữ liệu cũ. Không tự chọn dự án cũ. Nếu thư mục vừa được tạo, thông báo “Workspace mới, chưa có dự án”; nếu đã có thì đưa danh sách ngắn các tác phẩm / hồ sơ được nhận diện, có bằng chứng (tên file, metadata). Dừng sau câu hỏi, chờ câu trả lời; không tạo file 7 đầu ra hay chạy bất cứ tầng sáng tác nào trong lượt chỉ giao thư mục.

**Tránh lặp thư mục:** Nếu người dùng chọn chính `VIET_LACH_WORKSPACE` hoặc một thư mục con của nó, nhận diện và tái sử dụng workspace hiện có; không tạo `.../VIET_LACH_WORKSPACE/VIET_LACH_WORKSPACE`. Nếu đường dẫn chưa đọc/không thể kết luận đã có hay chưa, dừng với trạng thái `CHƯA KIỂM CHỨNG` thay vì tạo thử. Workspace cũ chỉ đọc cho đến khi người dùng yêu cầu cụ thể; không ghi đè thành phẩm và canon.

**Tôn trọng đầu vào:** Nếu người dùng đã nói máy và thư mục, không hỏi lại. Nếu họ đã cung cấp đầy đủ brief trong cùng lượt, sau khi kiểm tra workspace **tóm tắt đề bài có sẵn và hỏi xác nhận bắt đầu**, không yêu cầu nhập lại từ đầu. Nếu người dùng chưa đưa yêu cầu làm việc, luôn hỏi câu trên.

## Thư mục đầu ra mẫu trên Windows

```text
D:\VIET_LACH_WORKSPACE\<ten-du-an>\
    KICH_BAN_HOAN_CHINH.md
    COT_TRUYEN.md
    NHAN_VAT.md
    LOI_THOAI.md
    DANH_SACH_CANH.csv
    HUONG_DAN_HINH_ANH_AM_THANH.md
    BAO_CAO_NGHIEM_THU.md
    revisions\                     # chỉ dùng khi đã có tệp và cần tránh ghi đè
```

Đường dẫn mẫu không phải đường dẫn đã xác minh; folder thực được người dùng chọn. Có thể dùng ổ `E:` hoặc đường dẫn khác theo chỉ dẫn. Khi user chọn `D:\du-an\`, không tự chuyển sang ổ khác.

## CSV chuẩn cảnh

```csv
scene_id,start_time,end_time,duration_s,int_ext,location,time_of_day,characters,purpose,transition
SC001,00:00,00:12,12,INT,Phòng khách,Đêm,"Bố; Mẹ",Giới thiệu tình huống,CUT
SC002,00:12,00:28,16,INT,Bếp,Đêm,"Bố; Mẹ",Thắt nút,CUT
```

Ví dụ chỉ diễn giải schema, không phải kịch bản thật. Giá trị `start_time`/`end_time` sử dụng MM:SS (hoặc HH:MM:SS với tác phẩm dài); tổng thời lượng cộng chính xác theo `duration_s` và nói rõ đang *ước tính* trước ghi âm/render.

## Checklist kiểm tra
- **REMOTE-01**: đúng deviceId/máy, có phản hồi công cụ và đường dẫn được user chấp nhận.
- **REMOTE-02**: có quyền tạo/ghi/đọc trong project dir; workspace cũ chỉ đọc tới khi có quyết định đổi.
- **SCRIPT-01**: có đủ cốt truyện/nhân vật/thoại/cảnh/thời lượng/hình và âm.
- **SCRIPT-02**: mã cảnh nhất quán qua kịch bản, thoại, CSV, hướng dẫn; timeline không hở/chồng; người nói nằm trong cast.
- **FILES-01**: ghi 7 tệp, không trống, đọc lại từ *máy đích*, nội dung không bị cắt.
- **FILES-02**: file cũ được bảo vệ; nếu bản mới thì ghi revision riêng, không tự động xóa/cập nhật bản duyệt.
- **QC-REPORT**: nếu bất kỳ mục chưa kiểm tra, không kết luận mọi thứ đã đạt hoặc đã lưu đủ.

## Quy tắc kết luận
- `ĐÃ LƯU TRÊN MÁY CHỦ — ĐẠT`: 7 tệp đã kiểm tra đủ, kịch bản đạt QC.
- `ĐÃ LƯU MỘT PHẦN — CẦN SỬA`: còn thiếu/hỏng file hoặc nội dung chưa QC xong.
- `CHƯA LƯU TRÊN MÁY CHỦ — CHƯA KIỂM CHỨNG`: chưa có kết nối/quyền ghi/readback. Nếu bàn giao bằng chat/local file, tách trạng thái rõ.

Nguồn chuẩn nội dung: `skills/kich-ban-4-tang/SKILL.md`; mẫu văn bản: `references/kich-ban-template.md`; kỹ năng thao tác: `skills/luu-kich-ban-may-chu/SKILL.md`.
