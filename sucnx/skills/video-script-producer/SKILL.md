---
name: video-script-producer
description: Viết KỊCH BẢN VIDEO chuyên sâu (TikTok/Reels/YouTube Short hoặc video dài) — hook 3 giây đầu, các beat, gợi ý hình/b-roll, lời thoại, CTA, nhịp theo thời lượng. Dùng skill này KHI cần script video thật sự (không phải caption), hoặc user nói "kịch bản video/Reels/TikTok", "script quay", "viết video". Đọc brief (hoặc output `demo-scripter`) + L0 (voice, locale). KHÁC `copywriter` (viết copy chung) — đây là chuyên gia video có timing & shot. Mọi claim verify `product-truth`.
---

# video-script-producer

**Layer:** L3 · Producer · **Pattern:** Linear / Source-Driven · **Output:** video script `.md` (2 cột)

## Mục đích
Biến brief thành kịch bản quay được ngay — nhịp đúng thời lượng, hook giữ người xem trong 3 giây đầu, có cả lời thoại lẫn gợi ý hình.

## Bước 0 — Nạp brand
Đọc `brands/_active.md` → `brand-system.md` (voice, **locale**) · `product-truth.md` (proof + claim).

## Input
- Brief (từ `content-brief`/`message-architect`) hoặc cảnh từ `demo-scripter` · format (short <60s / dài) · chủ đề.

## SOP
1. **Chọn format & thời lượng** → quyết nhịp (short: dồn, mỗi 3–5s một nhịp; dài: có arc).
2. **Hook 0–3s** *(Spectrum: viết 2–3, chọn 1)* — phải chặn lướt.
3. **Cấu trúc:** Hook → Setup → các beat nội dung → Payoff → CTA.
4. **Viết 2 cột:** *Lời thoại / On-screen text* | *Hình · b-roll · shot · timing*.
5. **Self-check:** claim verify `product-truth`? · đúng locale? · không từ cấm? · CTA rõ?

## Output template
```markdown
# Video script: [tên] — [format, ~thời lượng]
Locale: … · Hook đã chọn: …

| Time | Lời thoại / On-screen | Hình · b-roll · shot |
|------|------------------------|----------------------|
| 0–3s | … | … |
| … | | |

## Hook alternates
- … · …
## Caption gợi ý kèm video
…
## Proof check
| Claim | Nguồn product-truth |
```

## DoD
Đã load voice/locale? · hook 3s mạnh? · 2 cột (thoại + hình)? · nhịp theo thời lượng? · claim verify? · CTA rõ?

## Skill kế tiếp
→ `critic-qa` · `visual-communicator` (nếu cần thêm ý tưởng hình).
