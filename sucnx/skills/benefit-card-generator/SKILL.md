---
name: benefit-card-generator
description: Đóng gói một feature thành BENEFIT CARD marketing theo schema cố định (audience · promise · proof · belief shift · best-fit) — không brainstorm, mà ráp một nguyên liệu chỉn chu sẵn cho copywriter/strategist. Dùng skill này KHI cần thẻ lợi ích cho feature mới hoặc làm lại benefit card cũ. KHÔNG gọi khi chưa biết angle/audience (brainstorm trước bằng `angle-miner`). Đọc `product-truth` + `audience-personas`.
---

# benefit-card-generator

**Layer:** L2 · Specialist (miner) · **Pattern:** Reverse / Target-Driven · **Output:** benefit card `.md`

## Bước 0 — Nạp brand
Đọc `brands/_active.md` → `product-truth.md` (feature + proof) · `audience-personas.md` (desire/pain).

## SOP (Audience-Driven / Reverse)
1. Nhận 1 feature + audience mục tiêu.
2. Reverse: từ **desire/pain của audience** → **promise** (lợi ích thật) → **proof** (verify product-truth) → **belief shift** (niềm tin cần đổi).
3. Ráp theo schema cố định (không brainstorm lan man).
4. Pre-mortem: promise có vượt claim không.

## Output template
```markdown
# Benefit card: [feature]
- **Audience:** …
- **Promise:** … (lợi ích, không phải feature)
- **Proof:** … (nguồn product-truth)
- **Belief shift:** từ "…" → "…"
- **Best-fit:** copywriter / landing / sales …
```

## DoD
Promise là lợi ích (không phải feature)? · proof verify được? · belief shift rõ? · không over-claim?

## Skill kế tiếp
→ `copywriter` / `narrative-strategist` / `sales-enabler`.
