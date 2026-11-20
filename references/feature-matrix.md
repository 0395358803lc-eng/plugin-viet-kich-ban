# Kiểm kê nguồn và chuyển đổi năng lực

Tài liệu này dẫn chiếu các gói ZIP **đã được người dùng cung cấp**. Nội dung kỹ năng là hướng dẫn mới, độc lập; không bundling code/GUI/ebook mẫu, không cam kết API hay local service của sáu dự án đã cài hoặc chạy.

| Gói nguồn | Năng lực theo README và code/skills | Kỹ năng Viết-Lách được ánh xạ |
|---|---|---|
| `inkos-master.zip` (InkOS) | 19 professional story skills: tiểu thuyết dài/ngắn; phim/kịch bản/storyboard; fanfic, spinoff, imitation, continuation; import, review, deslop, dịch; scan/analyze thị trường; bìa, interactive film, Play world/illustration; multi-model; FTS5/BM25; forecasts; atomic state; export | khởi tạo, nghiên cứu, phân tích, dài/ngắn, kịch bản, storyboard, tương tác, world, canon, forecast, fanfic, ngoại truyện, dịch, bìa, review, export, model, batch |
| `oh-story-claudecode-main.zip` (Oh Story) | 14 skills: setup, router, market scan/analyze long and short, draft long/short, import, de-AI, review, cover, publish, browser CDP; tracking state, author/reader knowledge, hook, local guard | router, thị trường, phân tích, dài/ngắn, import, review, khử AI, bìa, metadata, canon/hooks, doctor |
| `webnovel-writer-master.zip` (Webnovel Writer v6) | 8 skills init/plan/write/review/query/learn/dashboard/doctor; Story System contract and accepted CHAPTER_COMMIT, projection, RAG fallback BM25, audit, backups, genres | init, outline, chapter, commit/canon, review, query, learn, doctor, versions, batch |
| `AI_NovelGenerator-main.zip` (AI Novel Generator) | quản lý project, world rules, factions, nhân vật/quan hệ, items, location, volume→arc→scene→chapter, graph; configurable LLM workflow DAG with approval; MongoDB transactions | worldbook, cast, architecture, plan, workflow-node, pipeline-model, continuity, query |
| `Pagekin-master.zip` (Pagekin 1.5.0) | desktop book library; reference breakdown; import own draft; style; character states by chapter; due foreshadow; blueprint check; draft-review-rewrite-final; inline edits / batch annotations; reopen chapter, trash/restore, knowledge base and export | import, analysis, style, cast, plot/hook, chapter, review, revise, versions, query, doctor, export |
| `gpt-author-main.zip` (GPT-Author) | tạo và sàng lọc ý tưởng → cải thiện storyline → dàn ý theo số chương → viết tuần tự → prompt bìa/ảnh → tổng hợp EPUB | concept, structure, long writing, cover, ebook |

## Chức năng có trong dự án gốc nhưng KHÔNG được nhận là đã cài trong plugin skills-only
- UI Electron/Web (Studio, Pagekin, Oh Story Workbench, Dashboard của Webnovel Writer, giao diện AI Novel Generator).
- DB SQLite/MongoDB/embedding/vector, worker/daemon, notification, browser CDP, API key/proxy, Ollama/LM Studio, workflow node runner, tạo ảnh động/video, publish thực sự.
- Những phần này có thể thiết kế workflow hoặc hướng dẫn thiết lập khi có công cụ và sự chấp thuận; không có runtime hay MCP riêng trong plugin bản 1.0.0.

## Sở hữu trí tuệ
Giữ tham chiếu nguồn và license; chỉ tổng hợp **ý tưởng phương pháp và quy trình có diễn đạt mới**. Không sao chép source code hoặc bundle tài sản gốc, đặc biệt từ InkOS và AI Novel Generator (AGPL-3.0), Webnovel Writer và Pagekin (GPL-3.0). Oh Story và GPT-Author (MIT). Nếu sau này tích hợp chạy thực tế mã nguồn của các dự án GPL/AGPL, phải xem lại điều kiện của từng giấy phép và thông báo pháp lý thích hợp.
