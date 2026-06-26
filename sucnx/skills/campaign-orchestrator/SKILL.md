---
name: campaign-orchestrator
description: Lập kế hoạch & điều phối một CAMPAIGN nhiều kênh — campaign brief, lịch nội dung đa kênh (calendar), phân vai/owner, milestone, dependency. Dùng skill này KHI cần plan cả một chiến dịch, "lên campaign", "lịch đăng đa kênh", "content calendar", "campaign brief + timeline". Đọc strategy (`marketing-strategist`, nếu có) + L0. Output là kế hoạch campaign để `orchestrator`/producers thực thi từng deliverable. KHÁC `orchestrator` (route 1 yêu cầu lẻ) — đây plan cả campaign theo thời gian & nhiều kênh.
---

# campaign-orchestrator

**Layer:** L1 · Strategist (Leader) · **Pattern:** Matrix / Cross-Mapping · **Output:** campaign plan + calendar `.md`

## Bước 0 — Nạp
Đọc `brands/_active.md` → `0_truth/` + strategy doc (nếu có) + Narrative Library (nếu `narrative-strategist` đã chạy).

## SOP
1. **Campaign brief:** objective · audience · message chính · KPI (từ `kpi-standards`) · thời gian.
2. **Map deliverable × kênh × phễu** *(Matrix)*: mỗi ô = 1 deliverable cần sản xuất.
3. **Calendar:** lịch đăng theo tuần, milestone, owner, dependency (cái gì trước cái gì).
4. **Bàn giao sản xuất:** mỗi deliverable → chuỗi `orchestrator` (vd angle-miner→content-brief→copywriter→critic-qa) hoặc skill phù hợp.
5. **Pre-mortem:** rủi ro lịch/nguồn lực; điểm nghẽn.

## Output template
```markdown
# Campaign plan: [tên] — [brand]
## Campaign brief (objective · audience · message · KPI · thời gian)
## Ma trận deliverable (kênh × phễu)
## Content calendar (tuần · deliverable · owner · milestone)
## Bàn giao sản xuất (deliverable → chuỗi skill)
## Pre-mortem
```

## DoD
Đã load L0 (+ strategy)? · brief đủ KPI từ north-star? · ma trận + calendar có owner/milestone? · mỗi deliverable chỉ rõ chuỗi sản xuất? · pre-mortem?

## Skill kế tiếp
→ `narrative-strategist` (thư viện angle) → từng deliverable qua `orchestrator`. Đo lường: `performance-analyst` (L5).
