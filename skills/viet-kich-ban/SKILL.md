---
name: viet-kich-ban
description: "Use when converting stories or briefs into screenplays, short films, dialogue scripts or video narration."
---

# Viết kịch bản phim và video

**Nguồn năng lực được tổng hợp:** InkOS; GPT-Author. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Truyện/brief, thời lượng, loại hình, khán giả, tỷ lệ thoại/lời dẫn.

## Quy trình sản xuất kịch bản trọn gói v1.1.0

Đối với yêu cầu **kịch bản hoàn chỉnh** từ ý tưởng hoặc chuyển thể truyện/phim hoạt hình, gọi `../kich-ban-4-tang/SKILL.md` trước để dùng 4 tầng và QC. Giữ các hướng dẫn bên dưới làm kỹ thuật nền, nhưng đầu ra trọn gói phải gồm **cốt truyện + nhân vật + thoại thực tế + bảng cảnh/timecode + hướng dẫn hình và âm cho từng cảnh**; không chỉ trả một file screenplay trống phần âm/hình.

## Các bước bắt buộc
1. Tính thời lượng ước lượng theo tốc độ đọc và nhịp hoạt cảnh, nói rõ là ước lượng nếu chưa đo audio.
2. Tách scene: INT/EXT, địa điểm, thời gian, mục tiêu nhân vật, action có thể quay, thoại, âm thanh và chuyển cảnh.
3. Chuyển độc thoại nội tâm thành hành động/ánh mắt/tình huống có thể thể hiện, tránh diễn giải không thể quay.
4. Viết bảng nhịp và điểm nhấn cứ mỗi cảnh, tránh nhảy thời gian bất hợp lý.
5. Đưa kịch bản ra định dạng scene script và phiên bản lời thuyết minh riêng nếu video kể chuyện.

## Đầu ra
screenplay.md + voice-over.txt + scene-list.csv.

## Tiêu chí nghiệm thu
Thoại tự nhiên, hành động nhìn thấy được, tổng thời lượng ước lượng được giải thích.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
