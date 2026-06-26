---
name: visual-communicator
description: Biến một đoạn copy/headline ĐÃ viết xong thành ý tưởng hình ảnh — brainstorm rộng nhiều hướng visual, shortlist top 3, rồi spec đủ để giao designer (kèm cách dùng màu/typography của brand). Dùng skill này KHI đã có copy và cần "ảnh/graphic/carousel nào đi kèm", cần ý tưởng visual trước khi giao designer, hoặc user nói "làm visual cho bài này", "lên ý tưởng hình", "carousel concept". Đây là skill IDEATION — không spec pixel/bố cục chi tiết, không viết copy (đó là `copywriter`), không tìm metaphor cho concept trừu tượng khi chưa có copy (đó là `device-miner`).
---

# visual-communicator

**Layer:** L2 · Specialist (transformer, Design) · **Pattern:** Funnel / Filter-Driven · **Output:** visual ideas `.md`

## Mục đích
Dịch chữ ra hình: từ copy đã chốt → ý tưởng visual đủ rõ để designer làm, vẫn đúng nhận diện brand. Brainstorm rộng rồi lọc — vì ý tưởng visual đầu tiên thường là cliché.

## Bước 0 — Nạp brand (bắt buộc)
1. Đọc `brands/_active.md` → `active:`.
2. Load `brands/<active>/0_truth/brand-system.md`: **màu (HEX) + cách dùng**, **typography**, locale (ngôn ngữ text overlay), do/don't visual nếu có.
3. Mọi spec phải bám đúng palette + font brand — không tự chế màu ngoài hệ.

## Input
- Copy/headline đã viết (ưu tiên từ `copywriter`) · format đích (carousel / single image / video thumbnail / banner).

## SOP
1. **Rút lõi:** message chính + các beat của copy.
2. **Brainstorm 8–12 ý tưởng qua 6 lens** *(Spectrum)*: Literal scene · Metaphor visual · Before/After · Symbol/Icon · Data-viz/Structure · Story scene.
3. **Chấm & lọc** *(80/20)* theo 4 tiêu chí: rõ ràng · đúng message · scroll-stopping · hợp audience → **shortlist top 3**.
4. **Spec top 3:** concept · lens · why-it-works · bố cục thô · **cách dùng màu brand** · text overlay (đúng locale).
5. Nếu format = carousel: **spec slide-by-slide** cho concept đề xuất.
6. **Strategic Alignment:** ý tưởng nào tái dùng cho format khác (single image, thumbnail).
7. **Pre-mortem:** rủi ro visual (khó hiểu, cliché, chữ quá nhiều, sai brand).

## Output template
```markdown
# Visual ideas: [tên bài] — [format]
Brand palette dùng: … (từ brand-system)

## Brainstorm (full)
| # | Ý tưởng | Lens | Điểm mạnh |
|---|---|---|---|

## Shortlist top 3 (spec)
### 1. [concept] — ĐỀ XUẤT
- Lens · why-it-works · bố cục · màu brand · text overlay
### 2 … ### 3 …

## (Nếu carousel) Slide-by-slide concept đề xuất
S1 cover: … · S2: … · …

## Pre-mortem
- …
```

## DoD
Đã load palette/typography brand? · ≥8 ý tưởng → shortlist 3 đã spec? · text overlay đúng locale? · bám màu/font brand? · chỉ skill kế tiếp?

## Skill kế tiếp
→ `carousel-brief` / `designer-producer` (spec sản xuất chi tiết) · `critic-qa` (check brand).
