---
name: viet-lach
description: "Use when the user asks to write, plan, analyze, review, continue, translate, publish or adapt a story, novel, script, webnovel or interactive fiction."
---

# Điều phối Viết-Lách

**Nguồn năng lực được tổng hợp:** Tổng hợp cả sáu dự án. Đây là quy trình độc lập, không phải lời khẳng định đã chạy ứng dụng nguồn.

**Đầu vào cần dùng:** Yêu cầu của tác giả; dự án hoặc bản thảo nếu có.

## Ưu tiên máy chủ & điểm chờ yêu cầu (v1.3.0)

**Nếu người dùng yêu cầu dùng Viết-Lách trên máy chủ, lưu kịch bản trên máy chủ, hoặc đã kết nối Remote Desktop Commander:** **bắt buộc** mở `../luu-kich-ban-may-chu/SKILL.md` và đi theo thứ tự: **xác minh máy → nhận SELECTED_DIR → xác định WORKSPACE_ROOT → kiểm tra `VIET_LACH_WORKSPACE` (thiếu thì tạo; có rồi thì nhận diện dữ liệu cũ ở chế độ đọc) → báo trạng thái → HỎI YÊU CẦU NGƯỜI DÙNG → chờ câu trả lời → mới phân tuyến sáng tác → QC → ghi 7 tệp → đọc lại và nghiệm thu**.

**Chốt chặn ưu tiên cao:** chỉ có yêu cầu chọn máy hoặc thư mục **không phải** là yêu cầu sáng tác. Tuyệt đối không tự chạy quy trình 4 tầng, không tạo thư mục dự án con, không chọn một tác phẩm cũ để tiếp tục cho đến khi người dùng nói họ muốn làm gì sau khi được báo tình trạng workspace. Cả workspace mới tạo lẫn workspace cũ đều phải đi qua `R02B — AWAITING_USER_REQUIREMENT`. Khi máy/folder đã được nêu, không hỏi lại. Nếu thông điệp ban đầu đã nói rõ yêu cầu nội dung, sau kiểm tra workspace xác nhận lại trên cơ sở dữ kiện sẵn có, không bắt người dùng viết lại đề bài.

Không khởi động AI tại máy hoặc cài thêm runtime/model cho việc viết kịch bản `.md`/`.csv`.

Mặc định bàn giao **7 tệp** với tên cố định theo `../../references/remote-workspace.md`; ưu tiên bản kịch bản hoàn chỉnh. Chỉ xác nhận “đã lưu trên máy chủ” sau khi có bằng chứng từ Remote Desktop Commander về **ghi và đọc lại** trên đúng máy; nếu công cụ không hiện diện/quyền ghi thất bại, báo CHƯA LƯU và vẫn có thể tạo nội dung trong chat. Không coi file sandbox ChatGPT là file máy chủ.

## Chế độ mặc định khi gọi plugin để viết kịch bản (v1.1.0)

Nếu yêu cầu là **viết kịch bản từ một ý tưởng, truyện hoặc chủ đề** hoặc chỉ gọi Viết-Lách mà không chỉ định nghiệp vụ khác, **ưu tiên mở `../kich-ban-4-tang/SKILL.md`** và chạy liền mạch **InkOS + Oh Story → Shuohao + Drama → Humanizer + AI Copywriter → KỊCH BẢN HOÀN CHỈNH**. 38 kỹ năng từ phiên bản 1.0.0 vẫn là nền tảng để lập cốt truyện, quản lý nhân vật, canon, diễn đạt và kiểm toán; không bỏ hoặc thay thế chúng.

**Đầu ra của chế độ này bắt buộc có đủ:** cốt truyện + nhân vật + lời thoại nguyên văn + danh sách cảnh + thời lượng + hướng dẫn hình ảnh và âm thanh. Không giao chỉ dàn ý/ý tưởng nếu người dùng yêu cầu kịch bản hoàn chỉnh. Khi chỉ định một tác vụ hẹp như đánh giá một chương, viết truyện dài, xuất EPUB..., giữ nguyên hướng định tuyến chuyên dụng bên dưới.

## Các bước bắt buộc
1. Phân loại yêu cầu thành nghiên cứu, nhập truyện, sáng tác, duy trì canon, kiểm định, biên tập, xuất bản hoặc chuyển thể; định tuyến đến kỹ năng phù hợp và dùng nhiều kỹ năng nối tiếp nếu cần.
2. Xem có thư mục dự án, bản đã chốt, hoặc tệp nguồn hay không; ưu tiên nguồn đã tải lên và tài liệu gốc, không bịa nội dung chưa đọc.
3. Tạo một kế hoạch ngắn nêu mục tiêu, đầu ra và điểm phê duyệt tác giả ở những quyết định làm đổi canon; nếu yêu cầu rõ ràng, bắt tay vào thực hiện thay vì hỏi nhiều.
4. Tuân thủ chu trình: Brief → Research/Analysis → Bible → Outline → Chapter Contract → Draft → Review → Revision → Canon Commit → Export.
5. Trong một lượt, hoàn thành một đơn vị công việc có thể nghiệm thu; khi chưa truy cập file, cung cấp nội dung đầy đủ trong chat và nói rõ chưa lưu trên máy.
6. Đưa ra báo cáo ĐẠT/CẦN SỬA/CHƯA KIỂM CHỨNG với bằng chứng; không tự tuyên bố rằng dashboard, API, DB, EPUB đã chạy nếu chưa sử dụng công cụ thực.

## Đầu ra
Bảng lộ trình công việc + đầu ra thực tế + bước tiếp theo.

## Tiêu chí nghiệm thu
Mọi đầu ra truy xuất về yêu cầu; không thay đổi canon hoặc ghi đè bản thảo khi chưa được phép.

## Luật áp dụng chung
- Tôn trọng chỉ đạo hiện tại và dữ kiện tác giả xác nhận; không tự sửa canon, thay đổi cốt truyện hoặc ghi đè bản chính thức ngoài phạm vi.
- Phân biệt **đã thực hiện bằng công cụ**, **đã soạn trong chat**, **đề xuất**, **chưa xác minh**. Không giả vờ có file, DB, dashboard, model, hình hoặc EPUB nếu chưa thật sự tạo/kiểm tra.
- Xem dữ liệu của tác giả là nguồn ưu tiên; bản tóm tắt AI là dẫn xuất có thể sai. Khi thiếu chứng cứ đánh dấu CHƯA XÁC MINH.
- Ưu tiên tiếng Việt rõ ràng và xuất tác phẩm theo ngôn ngữ người dùng yêu cầu; văn xuôi sáng tạo cần nguyên bản.
- Khi cần quyền truy cập máy, API, tải phần mềm hoặc xuất bản ra ngoài: chỉ thực hiện với công cụ đã kết nối và sự cho phép thích hợp.
- Xem thêm `../../references/architecture.md`, `../../references/quality-gates.md`, `../../references/source-map.md`.
