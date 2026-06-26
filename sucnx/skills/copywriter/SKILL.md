---
name: copywriter
description: Viết câu chữ cuối cùng cho một deliverable cụ thể (LinkedIn post, blog, email, ad, landing copy, microcopy…) từ một content brief — đúng brand voice và đúng locale của brand đang active. Dùng skill này KHI đã có brief/angle và cần biến nó thành bản copy phát ra ngoài; hoặc khi user nói "viết post này", "viết caption/email/copy", "draft bài LinkedIn"… BẮT BUỘC nạp Brand Voice từ L0 trước khi viết câu đầu tiên. KHÔNG brainstorm angle (đó là `angle-miner`), KHÔNG tự bịa proof — mọi bằng chứng phải có trong `product-truth.md`.
---

# copywriter

**Layer:** L3 · Producer · **Pattern:** Linear / Source-Driven · **Output:** copy hoàn chỉnh `.md`

## Mục đích
Viết câu chữ thật, sẵn sàng đăng — đúng giọng thương hiệu, đúng ngôn ngữ thị trường, mọi claim verify được.

## Bước 0 — Brand Voice Loading Protocol (BẮT BUỘC, không skip)
1. Đọc `brands/_active.md` → `active:`.
2. Load `brands/<active>/0_truth/brand-system.md`: tính từ giọng · voice persona · **từ ưu tiên / từ cấm** · do/don't · **locale (ngôn ngữ output)** · 2 ví dụ đúng + 2 ví dụ sai voice.
3. Load `product-truth.md`: proof verify được + **ranh giới claim** (mục "KHÔNG được nói").
4. Viết TOÀN BỘ output bằng đúng **locale** khai trong `brand-system.md` của brand đang active (vd `English (US)`, `Tiếng Việt`).

## Input
- Content brief (từ `content-brief`) · loại deliverable.

## SOP
1. **Verify brief** đủ 4 trường: deliverable · audience · goal · anchor (angle/brief). Thiếu → hỏi.
2. **Chọn SOP theo format.** LinkedIn post: hook 1 dòng cực mạnh → 3–5 đoạn ngắn, ngắt dòng thoáng → 1 CTA mềm → (hashtag tùy chọn, ≤3). Giữ giọng chuyên gia, không hype.
3. **Hook *(Spectrum)*:** viết 2–3 hook, chọn 1, để 2 cái còn lại làm alternates.
4. **Body:** bám dàn ý brief; mỗi proof gắn vào phải verify được trong `product-truth.md`.
5. **Self-check trước khi nộp:** không dùng từ cấm? · không vượt ranh giới claim? · đúng locale 100%? · 1 message + 1 CTA? · nghe như voice persona, không như "sales nói quá"?

## Output template
```markdown
# [Deliverable] — [tên bài]
**Locale:** … · **Persona:** … · **Goal:** …

## Final copy
[bản copy hoàn chỉnh, đúng định dạng kênh]

## Hook alternates
- A: … · B: …

## Proof check
| Câu/claim dùng | Nguồn trong product-truth |
|---|---|
```

## DoD
Đã load Brand Voice? · đúng locale? · không từ cấm / không vượt claim? · proof verify được? · 1 CTA? · sẵn sàng cho `critic-qa`?

## Skill kế tiếp
→ `critic-qa` (gác cổng trước khi đăng) · `visual-communicator` (làm hình).
