---
name: phan-tich-tac-pham-mau
description: "Use when analyzing an uploaded novel, chapter, sample, or reference story for plot, emotion, style and craft."
---

# Phân tích và bóc tách tác phẩm

**Nguồn năng lực được tổng hợp:** Oh Story; InkOS; Pagekin. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Văn bản thật, hoặc tệp tác giả có quyền cung cấp; khối lượng và mục đích phân tích.

## Các bước bắt buộc
1. Kiểm tra đã đọc tài liệu gốc; nếu chỉ có tóm tắt thì giới hạn phân tích theo tóm tắt và không bịa dẫn chứng.
2. Đánh dấu từng chương/đoạn: sự kiện, quan hệ nhân-quả, xung đột, bí mật, ngôi kể, nhịp cảm xúc và mức độ hook.
3. Phân tích ba chương đầu, đường cong trông đợi–thỏa mãn–chi phí, đảo chiều, điểm trả nợ cốt truyện, độ dài cảnh.
4. Với truyện dài lập timeline tình tiết và nhân vật; với truyện ngắn lập beat map và đồ thị cảm xúc.
5. Rút ra nguyên tắc có thể chuyển giao (không sao chép câu chữ, nhân vật hay cốt truyện cụ thể) và danh sách không nên bê nguyên.

## Đầu ra
analysis-report.md + plot-beats.csv hoặc bảng + style-fingerprint.md.

## Tiêu chí nghiệm thu
Mỗi nhận định chính có vị trí chương/đoạn nguồn, điểm đánh giá kèm giải thích.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
