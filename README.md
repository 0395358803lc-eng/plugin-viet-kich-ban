# Viết-Lách v1.3.0 — Nhận thư mục, kiểm tra workspace, hỏi yêu cầu rồi mới sáng tác

**Thay đổi thứ tự thao tác trên máy chủ:** sau khi xác minh Remote Desktop Commander và nhận `SELECTED_DIR`, plugin sẽ nhận diện `VIET_LACH_WORKSPACE` nằm ngay trong thư mục đó (hoặc workspace hiện hành khi người dùng chọn đúng nó/một dự án con). Nếu thiếu, tạo thư mục workspace và đọc lại xác minh; nếu có, đọc nhận diện dự án cũ ở chế độ **read-only**. **Cả hai nhánh đều tóm tắt và hỏi người dùng muốn làm gì, dừng chờ yêu cầu trước khi mở quy trình sáng tác**. Không coi việc chọn thư mục là lệnh tạo kịch bản.

Bản này giữ **45 kỹ năng**, 4 tầng sáng tác, đầu ra **7 tệp** và cơ chế đọc lại nghiệm thu của v1.2.0. Không yêu cầu tải/cài AI cục bộ cho tác vụ kịch bản văn bản. Các chi tiết và tình huống biên: `skills/luu-kich-ban-may-chu/SKILL.md` R00–R02B, `references/remote-workspace.md`.

---

# Viết-Lách v1.2.0 — Soạn kịch bản trong ChatGPT, lưu thành phẩm trên máy chủ

**Bổ sung:** kỹ năng `luu-kich-ban-may-chu` để xác minh Remote Desktop Commander, chọn máy, hỏi thư mục dự án, kiểm tra dữ liệu cũ để tái sử dụng theo phạm vi, chạy đủ 4 tầng, lưu **7 tệp** và đọc lại từ máy đích trước khi nghiệm thu. Xem `references/remote-workspace.md`.

**Thành phần:** giữ nguyên 44 kỹ năng v1.1.0 (38 kỹ năng nền và 6 kỹ năng quy trình), thêm 1 kỹ năng giao tệp lên máy chủ = **45 kỹ năng**. Không cài AI hay app nguồn trên máy chủ cho tác vụ chỉ soạn văn bản. Cần Remote Desktop Commander có quyền ghi để thực sự đặt tệp trên máy chủ; nếu không, chỉ có thể soạn và giao ngoài máy chủ.

---

# Viết-Lách v1.1.0 — Quy trình viết kịch bản 4 tầng

**Mới:** ngoài 38 kỹ năng v1.0.0 còn nguyên, plugin bổ sung 6 kỹ năng hướng đến kịch bản phim/video/hoạt hình từ một chủ đề theo đúng chuỗi **InkOS + Oh Story → Shuohao + Drama → Humanizer + AI Copywriter → Kịch bản hoàn chỉnh**. Xem `skills/kich-ban-4-tang/SKILL.md`, `references/quy-trinh-4-tang.md` và `references/kich-ban-template.md`.

**Bàn giao theo mặc định:** cốt truyện, nhân vật, lời thoại, danh sách cảnh, timecode và hướng dẫn hình ảnh/âm thanh. Đây là plugin kỹ năng văn bản, không tích hợp runtime/SDK/API của 10 kho nguồn.

---

# Viết-Lách · Plugin bản 1.0.0

Gói kỹ năng tiếng Việt biên soạn trên cơ sở kiểm tra **6 ZIP nguồn**: InkOS, Oh Story, Webnovel Writer, AI Novel Generator, Pagekin, GPT-Author.

**Gồm 38 kỹ năng độc lập** trong `skills/`. Nội dung được tổng hợp thành workflow có thể gọi trong ChatGPT thay vì chép nguyên dự án phần mềm.

## Cách dùng
Gọi plugin và mô tả tác vụ bằng tiếng Việt: "Hãy mở dự án truyện dài kỳ", "Viết dàn ý chương 5", "Kiểm tra logic chương 12", "Nhập bản thảo rồi tiếp nối", "Tạo kịch bản video", "Soạn metadata và xuất EPUB".

Kỹ năng `viet-lach` là entrypoint, tự chọn kỹ năng chuyên sâu. Khi làm một tác phẩm dài kỳ, lưu hồ sơ và canon ở workspace khi có quyền truy cập tệp; nếu không có quyền, giao đủ nội dung trong chat để người dùng lưu.

## Tệp hướng dẫn
- `references/architecture.md`: cấu trúc workspace, canon và chapter commit.
- `references/workflows.md`: đường đi theo loại dự án.
- `references/quality-gates.md`: phương pháp nghiệm thu.
- `references/feature-matrix.md`: nguồn và tính năng ánh xạ.
- `references/source-map.md`: đầy đủ dấu vết file ZIP và source skills.
- `references/boundaries.md`: giới hạn của plugin skills-only.

## Giới hạn
**Không tự cài/khởi chạy sáu ứng dụng nguồn, không đi kèm source code và không có giao diện/dashboard backend riêng.** Những thứ đó cần môi trường và phần mềm riêng; kỹ năng hướng dẫn thiết kế và vận hành khi được cấp quyền. Không auto-post hay tự dùng API có phí.

## Nguồn và giấy phép
InkOS AGPL-3.0; Oh Story MIT; Webnovel Writer GPL-3.0; AI Novel Generator AGPL-3.0; Pagekin GPL-3.0; GPT-Author MIT. Gói này viết lại hướng dẫn độc lập và ghi công nguồn, không đưa mã nguồn/tài sản gốc vào archive.
