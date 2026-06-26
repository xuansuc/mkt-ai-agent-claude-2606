---
name: content-brief
description: Tạo content brief hoàn chỉnh cho MỘT bài content trước khi viết — gồm angle, 3 hook options, dàn ý body, proof points (verify từ L0), CTA và visual direction (nguyên tắc 1 brief = 1 bài = 1 angle = 1 CTA). Dùng skill này BẤT CỨ KHI NÀO cần brief một bài đăng / video / email, cần biến một angle đã chọn thành brief đủ để writer viết, hoặc nói "brief bài này", "content brief", "viết brief cho bài…". Kể cả khi chỉ có một chủ đề thô và muốn nó thành nội dung có định hướng rõ ràng, hãy dùng skill này. KHÔNG dùng để brainstorm nhiều góc (đó là `angle-miner`) hay viết câu chữ cuối (đó là `copywriter`).
---

# content-brief

**Layer:** L2 · Specialist (transformer) · **Pattern:** Reverse / Target-Driven · **Output:** brief `.md`

## Mục đích & nguyên tắc
Biến một angle thành bản brief đủ rõ để bất kỳ writer nào cũng viết được bài đạt chuẩn mà không hỏi lại. **`1 brief = 1 bài = 1 angle = 1 CTA`** — bài nhồi nhiều message thì không message nào đọng lại. Nhiều angle → tách thành nhiều brief.

## Bước 0 — Nạp brand (bắt buộc)
1. Đọc `brands/_active.md` → `active:`.
2. Load `brands/<active>/0_truth/`: `brand-system.md` (voice, do/don't, **locale** = ngôn ngữ output), `product-truth.md` (proof + ranh giới claim), `audience-personas.md`.
3. **Mọi proof trong brief phải truy được về `product-truth.md`.** Không có nguồn → ghi `[cần proof]`, không bịa.

## Input
- Angle (ưu tiên lấy từ output `angle-miner`) hoặc chủ đề thô · persona · kênh/format · CTA mong muốn · tầng phễu · (campaign, deadline nếu có).
Thiếu thì hỏi gọn 1 lượt; đủ ~80% thì làm và ghi rõ giả định.

## SOP
1. Chốt **1 angle** + **1 message** duy nhất.
2. Viết **3 hook options** khác kiểu *(Spectrum)*; đề xuất hook nên dùng + lý do.
3. Dựng **dàn ý body** (mở → thân → kết), mỗi phần 1 ý.
4. Gắn **proof points** — verify từ `product-truth.md`.
5. Chốt **1 CTA** cụ thể (đúng tầng phễu).
6. **Visual direction** để chuyển designer.
7. **Brand voice check** từ `brand-system.md` (tone, do/don't, từ cấm) + ghi **locale** để copywriter biết ngôn ngữ.

## Output template
```markdown
# Content Brief: [tên bài]

| Trường | Giá trị |
|---|---|
| Campaign | … |
| Kênh / Format | … |
| Tầng phễu | TOFU / MOFU / BOFU |
| Persona | … |
| Locale (ngôn ngữ output) | … |
| Deadline duyệt | … |

## 1. Mục tiêu & Message
- Mục tiêu: … · 1 message: …
## 2. Persona & Insight
- Đối tượng: … · Pain/Desire: …
## 3. Angle (1 góc)
…
## 4. Hook — 3 options
1. … 2. … 3. …
> Nên dùng: #_ — vì …
## 5. Dàn ý Body
- Mở: … · Thân: … · Kết: …
## 6. Proof points (verify từ product-truth)
- … (nguồn: …)
## 7. CTA (1 hành động)
…
## 8. Visual direction
…
## 9. Brand voice check
- Tone: … · Do: … · Don't/từ cấm: …
## 10. Giả định
- …
```

## DoD
Đã load L0? · 1 angle + 1 CTA? · 3 hook? · proof verify được? · ghi locale? · voice check? · chỉ skill kế tiếp?

## Skill kế tiếp
→ `copywriter` (viết câu chữ) · `visual-communicator` (ý tưởng hình).
