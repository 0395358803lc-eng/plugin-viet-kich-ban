---
name: dich-thuat-dai
description: "Use when translating long stories, manuscripts, scripts or serialized works between languages."
---

# Dịch truyện dài và nhất quán thuật ngữ

**Nguồn năng lực được tổng hợp:** InkOS. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Nguồn người dùng cung cấp, ngôn ngữ đích, độc giả, danh mục tên riêng.

## Các bước bắt buộc
1. Xác định giọng, cấp độ bản địa hóa, hạn chế về quyền và glossary tên, địa danh, chức danh, phép thuật.
2. Chia tác phẩm thành đoạn/chuơng có ranh giới đánh dấu và mã thứ tự để chống mất đoạn.
3. Dịch giữ ẩn ý, quan hệ xưng hô, cấu trúc, dụng ý nhân vật; không tự viết thêm hoặc sửa lỗi gốc mà không báo.
4. QC đối chiếu lượt theo 1–1 các phân đoạn, thông tin số, thoại, tên riêng, tình tiết bị cắt và tính trôi chảy.
5. Xuất glossary cập nhật và bảng tiến độ; bản nào chưa được dịch không ghi là hoàn thành.

## Đầu ra
translated-chapter.md + glossary.csv + QA-translation.md.

## Tiêu chí nghiệm thu
Không bỏ sót đoạn; thuật ngữ nhất quán và giữ intent của người viết.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
