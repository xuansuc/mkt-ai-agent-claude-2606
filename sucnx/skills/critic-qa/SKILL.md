---
name: critic-qa
description: Gác cổng chất lượng cuối trước khi xuất bản. Audit một deliverable theo brand voice, ranh giới claim, locale, độ bám persona/funnel, và việc tuân thủ 5 nguyên tắc tư duy + luật no-brand-leakage — rồi ra verdict Approve / Fix / Redo kèm danh sách lỗi cụ thể. Dùng skill này KHI có một bản copy/asset chuẩn bị đăng và cần kiểm tra độc lập; hoặc user nói "QA bài này", "check trước khi đăng", "review chất lượng". Đây là gác cổng thứ hai — không tự viết lại, chỉ chấm và chỉ lỗi để producer sửa.
---

# critic-qa

**Layer:** L4 · Meta · **Output:** QA report `.md` (Approve / Fix / Redo)

## Mục đích
Bắt lỗi có hệ thống trước khi deliverable ra ngoài. Đứng độc lập với người viết — vì người viết khó tự thấy lỗi của mình.

## Bước 0 — Nạp chuẩn
1. Đọc `brands/_active.md` → load `brand-system.md` (voice, từ cấm, locale), `product-truth.md` (ranh giới claim + proof), `audience-personas.md`.
2. Load `_meta/THINKING-PRINCIPLES.md` để biết tiêu chuẩn tư duy.

## Checklist audit (chấm từng mục Pass/Fail + bằng chứng)
1. **Brand voice** — đúng tính từ giọng? nghe như voice persona, không "sales nói quá"?
2. **Từ cấm** — có dùng từ nào trong danh sách cấm không?
3. **Ranh giới claim** — có vượt mục "KHÔNG được nói" trong product-truth không? mọi proof có verify được không?
4. **Locale** — đúng 100% ngôn ngữ quy định? (không lẫn ngôn ngữ khác)
5. **Persona & funnel fit** — chạm pain persona? CTA đúng tầng phễu?
6. **Thinking principles** — có dấu hiệu áp Spectrum/80-20? message tập trung (không nhồi)?
7. **No-brand-leakage (engine)** — nếu đang review một SKILL: skill có hardcode tên/claim brand không? (với deliverable thì bỏ qua mục này.)
8. **CTA** — rõ 1 hành động duy nhất?

## Verdict
- **Approve** — không có lỗi nghiêm trọng.
- **Fix** — đăng được sau khi sửa các lỗi đã liệt kê.
- **Redo** — sai nền tảng (sai angle/claim/locale), làm lại.

## Output template
```markdown
# QA report: [deliverable]
**Verdict:** Approve / Fix / Redo

| # | Mục | Pass/Fail | Bằng chứng / lỗi | Mức |
|---|---|---|---|---|

## Phải sửa (nếu Fix/Redo)
1. …

## Ghi chú tốt (giữ lại)
- …
```

## DoD
Đã chấm đủ 8 mục? · mỗi Fail có bằng chứng cụ thể? · verdict rõ ràng? · lỗi actionable (chỉ rõ sửa gì)?

## Skill kế tiếp
→ trả về `copywriter` để sửa (nếu Fix/Redo) · hoặc xuất bản (nếu Approve).
