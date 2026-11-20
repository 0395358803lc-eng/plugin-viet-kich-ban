# VIET_LACH_WORKSPACE — kiến trúc dự án khuyến nghị

Đây là **schema đề xuất** lấy tinh thần source-of-truth từ InkOS, Webnovel Writer, Oh Story, Pagekin và phân tầng của AI Novel Generator; không phải schema tương thích 1:1 với bất kỳ ứng dụng gốc nào.

```
VIET_LACH_WORKSPACE/
  <ten-du-an>/
    project-brief.md                 # yêu cầu người viết + ràng buộc
    author-intent.md                 # chủ ý và giọng dài hạn
    author-style.md                  # giọng & quy ước đã xác nhận
    story-bible.md                   # bối cảnh, luật, thế giới
    canon.json                       # state thật đã phê duyệt
    events.jsonl                     # sự kiện nguồn gốc theo chương
    worldbook/                      # locations, rules, factions, items
    characters/                     # hồ sơ nhân vật
    outlines/                       # tổng cương/quyển/arc/cảnh/chương
    chapters/                       # draft và bản đã chốt
    tracking/                       # timeline, hooks, knowledge, context
    reviews/                        # issue + review từng chương
    references/                     # tài liệu đối chứng, KHÔNG tự thành canon
    media/                          # kịch bản + storyboard + asset brief
    publishing/                     # tiêu đề, synopsis, metadata
    exports/                        # docx/txt/epub khi thật sự tạo
    backups/                        # bản sao & manifest checksum
    trash/                          # soft-deleted files khi có filesystem
```

## Nguồn chân lý và hợp đồng phiên bản
- `canon.json` giữ `schema_version`, `project_id`, `revision`, `last_committed_chapter`, `characters`, `locations`, `factions`, `items`, `rules`, `hooks`, `author_known`, `reader_known`, `unresolved_questions`. Canon không nhập trực tiếp từ nguồn tham chiếu ngoài.
- `events.jsonl`: mỗi sự kiện có `event_id`, `chapter_id`, `location_ref`, `timestamp_in_story`, `entity_ids`, `fact`, `evidence`, `review_status`, `revision`.
- `tracking/*` và các chỉ mục là sản phẩm đọc được/rebuild, không là căn cứ thay thế nguồn chuẩn.
- **Chapter Contract** trước khi viết: `chapter_id`, `canon_revision`, `goal`, `must_keep`, `must_avoid`, `scene_beats`, `characters`, `due_hooks`, `word_budget`.
- **Chapter Commit** sau khi viết: mã chương, checksum bản chính, review verdict, approved delta, revision mới, backup link; nếu có quyền file phải kiểm tra thao tác ghi thành công.
- Nếu ngoài ChatGPT thuần có kết nối máy, có thể tạo file tương ứng; không tự giả định có runtime chạy nền/DB/BM25/vector.

## Quy tắc phân biệt tri thức
1. Tác giả biết: kế hoạch, twist chưa kể, bí mật thế giới.
2. Độc giả biết tới chương N: văn bản đã xuất hiện / lời nhân vật có thể sai.
3. Nhân vật X biết tới chương N: chỉ những thông tin X nhận bằng quan sát, đối thoại hoặc suy luận hợp lệ.
4. Trạng thái vật lý và quan hệ có thời điểm hiệu lực. Không đưa thông tin từ N+5 quay ngược về N.
