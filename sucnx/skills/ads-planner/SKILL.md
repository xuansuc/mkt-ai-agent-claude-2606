---
name: ads-planner
description: Lập KẾ HOẠCH quảng cáo trả phí — research audience/targeting, tính KPI & ngân sách (CPA/ROAS/break-even), phân bổ media plan theo kênh & giai đoạn phễu, dựng kế hoạch A/B test. Dùng skill này KHI cần lên media plan, "tính KPI/CPA/ROAS mục tiêu", "phân bổ ngân sách ads", "targeting", "kế hoạch chạy quảng cáo". Đọc L0 (personas, kpi-standards, product-truth, competitor). KHÔNG viết ad copy (đó là `ads-copywriter`).
---

# ads-planner

**Layer:** L2 · Specialist (transformer, Ads) · **Pattern:** Reverse / Target-Driven · **Output:** media plan `.md`

## Bước 0 — Nạp brand
Đọc `brands/_active.md` → `audience-personas.md` · `kpi-standards.md` (north-star · CAC · break-even) · `product-truth.md` · `competitor-intel.md`.

## SOP
1. **Targeting** từ personas (audience · interest · awareness stage · loại trừ).
2. **KPI & ngân sách** *(Reverse từ north-star)*: từ mục tiêu lead/booking → CPA mục tiêu → break-even ROAS → ngân sách cần. Lấy đơn vị kinh tế từ `kpi-standards` (nếu `[TODO]` thì nêu giả định).
3. **Phân bổ** theo kênh × giai đoạn phễu (TOFU/MOFU/BOFU) — 80/20 dồn vào kênh hiệu quả.
4. **Kế hoạch A/B test:** 1 biến/lần (audience / creative / offer), tiêu chí winner rõ.
5. **Pre-mortem:** rủi ro (CPA vượt break-even, audience quá hẹp/rộng).

## Output template
```markdown
# Media plan: [brand] — [mục tiêu]
## Targeting (theo persona)
## KPI & ngân sách (Reverse từ north-star)
| Mục tiêu | CPA mục tiêu | Break-even ROAS | Ngân sách |
## Phân bổ kênh × phễu
## Kế hoạch A/B test (1 biến/lần)
## Pre-mortem
```

## DoD
Đã load kpi-standards? · KPI suy ngược từ north-star? · phân bổ theo phễu? · A/B 1 biến/lần? · pre-mortem?

## Skill kế tiếp
→ `ads-copywriter` (viết creative theo plan).
