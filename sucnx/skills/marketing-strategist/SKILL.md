---
name: marketing-strategist
description: Dựng CHIẾN LƯỢC marketing tổng / go-to-market cho brand — định vị, mục tiêu, ưu tiên chiến lược, phân bổ kênh/ngân sách, roadmap theo quý. Dùng skill này KHI cần định hướng tổng thể, "chiến lược marketing", "go-to-market", "kế hoạch quý", "ưu tiên kênh/ngân sách tổng". Đọc TOÀN BỘ L0 + insight mới nhất từ L5 (`5_data/insights-*.md`) — đây là nơi vòng phản hồi quay về. Output là bản chiến lược feed cho `campaign-orchestrator` & `narrative-strategist`. KHÔNG viết copy hay lên lịch chi tiết campaign.
---

# marketing-strategist

**Layer:** L1 · Strategist (Leader) · **Pattern:** Reverse / Target-Driven · **Output:** strategy doc `.md`

## Mục đích
Ra **bản vẽ chiến lược** cho cả brand — và là nơi **insight từ L5 quay về** để cập nhật hướng đi mỗi chu kỳ.

## Bước 0 — Nạp
Đọc `brands/_active.md` → TOÀN BỘ `0_truth/` + file `5_data/insights-*.md` mới nhất (nếu có) = đầu vào vòng lặp.

## SOP
1. **Tổng hợp định vị + north-star** từ L0.
2. **Tích hợp insight L5** (nếu có): điều gì data đã chứng minh → điều chỉnh ưu tiên.
3. **Chọn 3 ưu tiên chiến lược** *(80/20)* cho kỳ tới + lý do.
4. **Phân bổ kênh/ngân sách** theo ưu tiên (tham chiếu `kpi-standards`).
5. **Roadmap** theo quý/giai đoạn, milestone.
6. **Pre-mortem** *(Unknown Unknowns)* + rủi ro.

## Output template
```markdown
# Marketing strategy: [brand] — [kỳ]
## Định vị & north-star
## Insight L5 đã tích hợp (nếu có)
## 3 ưu tiên chiến lược (80/20)
## Phân bổ kênh / ngân sách
## Roadmap theo quý
## Rủi ro & pre-mortem
```

## DoD
Đã load full L0 + insight L5? · 3 ưu tiên rõ? · phân bổ bám north-star? · roadmap có milestone? · pre-mortem?

## Skill kế tiếp
→ `campaign-orchestrator` (biến chiến lược thành campaign) · `narrative-strategist` (thư viện angle).
