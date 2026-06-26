# sucnx — Marketing Agent Engine

Engine marketing đa thương hiệu cho Claude Code. **Build 1 lần, dùng cho nhiều brand** — mỗi brand chỉ cấp bộ **L0 (nguồn sự thật)** của riêng nó; toàn bộ skill giữ nguyên.

> Bản này **non-branded**: không kèm dữ liệu brand nào. Tạo brand đầu tiên bằng `/brand-onboard`.

📖 **Hướng dẫn đầy đủ (cài đặt · ma trận · từng phòng ban · ví dụ · FAQ):** xem [`USER_GUIDE.md`](USER_GUIDE.md).

## Kiến trúc 6 tầng
```
L0 nguồn sự thật → L1 strategists → L2 specialists → L3 producers → deliverable
   ↑                                                                    │
   └──────────────── L5 tail-loop ←── đo lường ←───────────────────────┘
   (L4 meta: orchestrator · brand-intake · critic-qa · agent-creator · workspace-librarian)
```

## Bắt đầu nhanh
1. `/brand-onboard <URL>` — tạo brand đầu tiên (research + phỏng vấn → sinh L0).
2. `/content <yêu cầu>` — tạo deliverable. Vd: `/content viết FB post về <chủ đề> cho <brand>`
3. `/use-brand <slug>` — đổi brand đang active.
4. `/review [kỳ]` — chạy vòng L5 (đo lường → insight → đề xuất cập nhật L0).

## Cấu trúc
```
sucnx/
├── .claude-plugin/plugin.json
├── _schema/   ← hợp đồng L0 (5 file)
├── _meta/     ← CONVENTION · THINKING-PRINCIPLES
├── skills/    ← 26 skill (6 tầng)
├── agents/    ← 3 phòng (content-lead · media-buyer · designer) + lớp Leader (mkt-leader)
├── commands/  ← /content · /use-brand · /brand-onboard · /review
└── brands/    ← rỗng — bạn tự thêm (xem brands/README.md)
```

## Nguyên tắc cốt lõi (xem `_meta/`)
- **No-brand-leakage:** skill không hardcode thông tin brand; tất cả nạp từ L0 lúc chạy.
- **5 nguyên tắc tư duy** (Spectrum · 80/20 · Strategic Alignment · Polymath · Unknown Unknowns) + **Mode Operators**.
- **1 agent = 1 tầng = 1 pattern.** Convention v3: `SKILL.md` + `references/`.

## Cài đặt
**Dùng nhanh (project-local):** đặt thư mục `sucnx/` trong project, copy các file trong `commands/` sang `.claude/commands/` của project.

**Cài như plugin (cả team):**
1. Đặt `sucnx/` trong một repo có `.claude-plugin/marketplace.json` (đăng ký plugin này).
2. `/plugin marketplace add <repo>` → `/plugin install sucnx`.
3. Sau khi cài, lệnh xuất hiện dạng `/sucnx:content`; skills nạp tự động; `brands/` đặt trong project của bạn.

## License
MIT — xem `LICENSE`.
