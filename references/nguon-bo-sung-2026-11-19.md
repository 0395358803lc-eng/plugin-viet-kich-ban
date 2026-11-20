# Nguồn bổ sung và ánh xạ chức năng phiên bản 1.1.0

Bốn kho lưu trữ được người dùng đưa trực tiếp. **Đã đọc mô tả và SKILL.md liên quan trong ZIP để rút phương pháp, không sao chép mã nguồn, không tích hợp các tiến trình/CLI/API trả phí của dự án gốc.** Nguồn 1.0.0 (6 dự án) trong `feature-matrix.md` và `source-map.md` vẫn nguyên vẹn.

| Nguồn ZIP | Giấy phép trong ZIP | Các thành phần liên quan | Phần tích hợp trong Viết-Lách |
|---|---|---|---|
| `shuohao-skills-main.zip` | Apache-2.0 | `novel-outline`, `novel-characters`, `novel-art`, `novel-script`, `novel-staging`, `novel-storyboard`, `character-refs` | Chia nhịp thành cảnh, lời thoại theo cảm xúc/người nói, ngân sách cảnh; liên tục nhân vật/đạo cụ, staging và chỉ dẫn shot. Không tự sinh ảnh. |
| `drama-skills-main.zip` | MIT | `short-drama-develop`, `short-drama-write`, `short-drama-assets`, `short-drama-storyboard`, `short-drama-video-prompts`, `short-drama-review` | Viết kịch bản phim/hoạt hình có hành động nhìn được, production cues, hướng dẫn hình/âm, review. Không tích hợp API media/FFmpeg/dashboard. |
| `humanizer-main.zip` | MIT | `SKILL.md` | Phát hiện và giảm nhịp câu công thức, sáo rỗng, giải thích thừa, văn phong thiếu cá tính; không đổi nghĩa/canon. |
| `ai-copywriter-claude-humanizer-copywriting-skill-u5x4vd.zip` | MIT | `SKILL.md`, `references/` | Xác định cảm xúc khán giả, hook/mở đầu, tiêu đề, nhịp và kết thúc thực chất; ngôn ngữ rõ, tự nhiên. Tránh đặt copy bán hàng vào thoại truyện khi không phù hợp. |

## Ranh giới quyền và chức năng
- Dùng tên dự án để nhận diện phương pháp; không nhận là chủ sở hữu các dự án, không chạy script/validator gốc trong plugin skills-only.
- Các kết quả theo README (JSON / dashboard HTML / image generation / video API / bản render) chỉ là năng lực ứng dụng gốc. Viết-Lách 1.1.0 giao tài liệu kịch bản và **hướng dẫn** sản xuất, không chuyển giao runtime.
- Không đưa code hoặc vật liệu nguồn dưới giấy phép của bên thứ ba vào plugin mới. Nếu tích hợp code thực trong tương lai, đánh giá Apache NOTICE/MIT và các giấy phép của 6 dự án v1.0.0 trước.
- Vùng nguồn gốc cấp 1: `../skills/tang-1-xay-dung-cau-chuyen` từ InkOS+Oh Story; cấp 2: `../skills/tang-2-viet-kich-ban-canh` và `../skills/thiet-ke-hinh-anh-am-thanh` từ Shuohao+Drama; cấp 3: `../skills/tang-3-bien-tap-loi-thoai` từ Humanizer+AI Copywriter.
