---
name: narrative-strategist
description: Dựng THƯ VIỆN narrative (5–10 angle có cấu trúc theo schema) cho cả một campaign nhiều kênh — spine kể chuyện trước khi sản xuất. Dùng skill này KHI cần định hướng narrative cho cả chiến dịch / nhiều deliverable / nhiều kênh, cần "kể câu chuyện này xuyên suốt thế nào", hoặc xây nguồn angle dùng chung cho copywriter/script/landing/sales. KHÁC `angle-miner` (đào nhanh angle cho MỘT bài) — đây là tầng chiến lược, ra thư viện angle cho cả campaign. KHÔNG viết câu chữ.
---

# narrative-strategist

**Layer:** L1 · Strategist · **Pattern:** Matrix / Cross-Mapping · **Output:** Narrative Library `.md`

## Mục đích
Tạo **nguồn angle** cho cả campaign — thư viện 5–10 angle có cấu trúc, để mọi producer (copywriter, video, landing, sales) lấy ra dùng thay vì mỗi người tự nghĩ một kiểu (tránh content drift). Đây là spine, không phải brief lẻ.

## Bước 0 — Nạp brand
Đọc `brands/_active.md` → load `audience-personas.md` · `product-truth.md` · `competitor-intel.md` · `brand-system.md` (voice, locale).

## SOP
1. **Chọn 1 anchor** *(Spectrum)*: A = đi từ value/feature · B = audience segment + awareness stage · C = belief cần lật.
2. **Sinh 5–10 angle**, mỗi angle theo **schema cố định 9 trường**:
   tên · story shape (1 trong 8 dạng narrative) · awareness stage (Schwartz) · audience · core message (1 câu) · emotional arc 3-beat · proof anchor (verify `product-truth`) · best-fit downstream (copywriter/video/landing/sales) · kênh.
3. **Polymath:** mượn narrative theory (story shapes), Eugene Schwartz (awareness).
4. **80/20:** đánh dấu top angle nên ưu tiên cho campaign + lý do.
5. **Pre-mortem:** rủi ro lệch (sales quá, trùng đối thủ, claim không verify).

## Output template
```markdown
# Narrative Library: [campaign/brand]
Anchor dùng: A/B/C

## Angle [n]
- Story shape · Awareness stage · Audience
- Core message: …
- Emotional arc: … → … → …
- Proof anchor: … (nguồn product-truth)
- Best-fit: copywriter / video / landing / sales — kênh: …

## Ưu tiên (80/20): angle #… vì …
## Pre-mortem
```

## DoD
Đã load L0? · 5–10 angle đủ schema 9 trường? · proof verify được? · đánh dấu ưu tiên? · pre-mortem?

## Skill kế tiếp
→ `content-brief` / `message-architect` / `copywriter` / `sales-enabler` lấy angle từ thư viện.
