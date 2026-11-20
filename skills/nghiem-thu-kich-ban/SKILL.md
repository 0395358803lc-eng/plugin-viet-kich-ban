---
name: nghiem-thu-kich-ban
description: "Use at final stage to verify and assemble a complete screenplay with plot, characters, full dialogue, scene list, exact time budget, audiovisual directions and QC."
---


# TẦNG 4 — Nghiệm thu, hợp nhất và bàn giao KỊCH BẢN HOÀN CHỈNH

**Không phải** “xong dàn ý” hoặc “hết lượt”. Kịch bản chỉ đạt khi người dùng có thể mang tài liệu này vào công đoạn dựng storyboard/đọc thoại/thu âm mà không phải nhờ viết lại toàn bộ lời thoại hay danh sách cảnh.

## Sáu điều kiện nghiệm thu bất biến
1. **CỐT TRUYỆN**: logline + synopsis có mở, xung đột, biến cố, cao trào và kết, khớp kịch bản.
2. **NHÂN VẬT**: danh sách nhân vật quan trọng gồm vai trò, mục tiêu, tính cách/giọng, ngoại hình/đặc điểm tạo hình nếu có; tên thoại phải khớp cast.
3. **LỜI THOẠI**: từng câu thực tế đầy đủ, có người nói, đánh dấu VO/OS/SFX rõ; không có dấu `...` hoặc “tự viết tiếp” thay phần thoại cần giao (trừ cố tình nhân vật bỏ lửng trong tác phẩm).
4. **DANH SÁCH CẢNH**: mỗi `SCnnn` có bối cảnh, thời gian trong chuyện, mục đích, hành động/thoại, chuyển cảnh; ID duy nhất, không mất cảnh, không đứt động cơ và hành động.
5. **THỜI LƯỢNG**: cho mỗi cảnh `duration_s` nguyên dương và timecode `[start,end)` liên tục từ 0; `sum(duration_s) == total_s`, không chồng/khuyết, không ép người nói nhanh vô lý. Nhãn “dự kiến”, sai lệch yêu cầu thì giải thích, đề nghị chỉnh hoặc sửa trước khi bàn giao.
6. **HÌNH + ÂM**: mỗi cảnh có hướng dẫn hình (nhân vật, bố cục/cỡ cảnh, góc máy, hành động, ánh sáng, nối cảnh) và âm (thoại/VO, nhạc, SFX/ambience hoặc chủ ý im lặng). Không có shot vượt duration, cue sai sự kiện, một nhân vật vừa thoại trong vừa bị gán giọng nhân vật khác.

## Quy trình soát lỗi
- Gate **G0 brief**: theo yêu cầu, giữ giới hạn (thể loại, ngôn ngữ, thời lượng, bản quyền/canon).
- **G1 Story**: có nguyên nhân-hậu quả, biến đổi nhân vật, cao trào/điểm kết không vô lý; không tạo cảnh kể suông.
- **G2 Screenplay**: đủ cảnh đầy đủ thoại, vị trí/đạo cụ/mặc đồ hợp lý, hành động có thể thể hiện, dàn nhịp.
- **G3 Polish**: lời nói nghe tự nhiên và khác nhau theo người; hook không giật tít, không thêm tình tiết chưa được duyệt.
- **G4 Timing/A-V**: tổng giây/timecodes khớp, thực hiện được bằng hình/âm, cảnh và shot khớp ngữ nghĩa.
- **G5 Final**: tài liệu theo `../../references/kich-ban-template.md`; không còn mẩu TODO/placeholder/viết tắt thay nội dung chính.
- Mỗi gate ghi `ĐẠT` nếu có bằng chứng trong bản thảo; `CẦN SỬA` nếu thấy lỗi; `CHƯA KIỂM CHỨNG` nếu cần bản ghi âm/dựng để khẳng định. Chỉnh trong phạm vi tác giả cho phép và kiểm tra lại, không đánh dấu ĐẠT khi chưa hoàn thành.

## Kiểm tra bổ sung khi bàn giao trên máy chủ (v1.2.0)
- Với yêu cầu lưu trên máy chủ, **7 tệp là bắt buộc**, không phải tùy chọn: `KICH_BAN_HOAN_CHINH.md`, `COT_TRUYEN.md`, `NHAN_VAT.md`, `LOI_THOAI.md`, `DANH_SACH_CANH.csv`, `HUONG_DAN_HINH_ANH_AM_THANH.md`, `BAO_CAO_NGHIEM_THU.md`.
- Thực hiện ghi và readback qua công cụ máy đích, đối chiếu thông tin giữa các tệp theo `../luu-kich-ban-may-chu/SKILL.md` và `../../references/remote-workspace.md`. Ghi rõ tệp nào thiếu, lỗi, hoặc chưa đọc được; chỉ chốt **ĐÃ LƯU TRÊN MÁY CHỦ — ĐẠT** khi đầy đủ bằng chứng.
- Không thể truy cập máy? Kịch bản soạn trong chat/tệp tải về vẫn hữu ích, nhưng trạng thái **CHƯA LƯU TRÊN MÁY CHỦ**; không thể thay thế bằng việc chỉ báo tên đường dẫn dự kiến.

## Xuất kết quả
- **Mặc định:** duy nhất **một bản KỊCH BẢN HOÀN CHỈNH** trong hội thoại hoặc file `.md` có thật khi công cụ cho phép, kèm bảng scene/timecodes và QC ngắn.
- **Tùy chọn với công việc không sử dụng máy chủ:** có thể xuất file riêng theo phạm vi người dùng yêu cầu; với máy chủ, dùng đúng 7 tên đã quy định; tạo file xong xác minh tồn tại và đọc lại mới báo thành công. Không yêu cầu người dùng nhấn duyệt qua 4 lần để có kết quả khi họ đã yêu cầu tạo trọn gói.
- Nếu quá dài cho một lần trả lời, bàn giao phần đã hoàn tất rõ ràng cùng cảnh chưa xong; **không** dùng tiêu đề hoàn chỉnh cho bản thiếu nội dung.
