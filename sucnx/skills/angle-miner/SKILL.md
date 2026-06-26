---
name: angle-miner
description: Brainstorm a wide catalogue of distinct story angles for a topic, feature, or message — then score them and shortlist the strongest ~20% for a given audience and funnel stage. Use this skill WHENEVER someone needs angles / ways to frame a story / "how should we position this" / directional hooks BEFORE writing a content piece, or wants options instead of committing to the first idea. Trigger even if they only give a raw topic and want it turned into sharp, audience-fit angles. Do NOT use to write final copy (that is `copywriter`) or to sequence one piece beat-by-beat (that is `content-brief`).
---

# angle-miner

**Layer:** L2 · Specialist (miner) · **Pattern:** Funnel / Filter-Driven · **Output:** angle catalogue `.md`

## Mục đích
Đào RỘNG nhiều góc kể chuyện cho một chủ đề rồi LỌC xuống số ít sắc nhất. Đây là nguồn brief, không phải brief. Brainstorm rộng trước, chấm điểm sau — vì góc đầu tiên nghĩ ra thường chỉ là góc phổ biến nhất, hiếm khi sắc nhất.

## Bước 0 — Nạp brand (bắt buộc, qua indirection)
1. Đọc `brands/_active.md` → lấy `active:`.
2. Load từ `brands/<active>/0_truth/`: `audience-personas.md` (pain/desire/awareness/objection), `product-truth.md` (sự thật + proof + differentiators), `competitor-intel.md` (điểm khác biệt), `brand-system.md` (voice + locale).
3. Mọi angle phải bám persona thật và sự thật sản phẩm trong L0 — KHÔNG bịa.

## Input
- Chủ đề thô · persona mục tiêu (mặc định: persona PRIMARY trong L0) · tầng phễu (TOFU/MOFU/BOFU) · kênh.

## SOP
1. **Xác định khung.** Chốt persona + tầng phễu + awareness stage (Schwartz, lấy từ persona).
2. **Brainstorm 8–12 angle theo nhiều trục** *(Spectrum of Choices)*: pain-led · desire-led · contrarian · proof-led · trend-led · story-led · objection-led · comparison-led. Mỗi angle 1 câu, khác nhau thật về góc nhìn.
3. **Polymath:** dùng ít nhất 1 khung ngoài marketing để bẻ góc mới (vd Eugene Schwartz awareness stages, Jobs-to-be-Done, loss aversion).
4. **Chấm điểm & lọc** *(80/20)*: mỗi angle chấm theo 4 tiêu chí — chạm pain persona · tận dụng differentiator · có proof thật chống lưng · đúng tầng phễu → gắn HIGH / MEDIUM / NORMAL.
5. **Shortlist top ~3** kèm lý do, và 1 angle **đề xuất dùng**.
6. **Strategic Alignment:** ghi rõ angle nào tái dùng được cho ≥2 kênh, angle nào single-purpose.
7. **Pre-mortem** *(Unknown Unknowns)*: 1–2 rủi ro khiến các angle này flop (vd nghe sales quá, trùng đối thủ, claim không verify được).

## Output template
```markdown
# Angles: [chủ đề] — [persona] — [tầng phễu]

## Catalogue (full)
| # | Angle (1 câu) | Trục | Impact | Proof chống lưng (từ product-truth) |
|---|---|---|---|---|

## Shortlist (top 3)
1. **[angle]** — vì … · tái dùng cho: …
2. …
3. …

## Đề xuất dùng: #_
Lý do ngắn.

## Pre-mortem
- …
```

## DoD
Input đủ? · đã load L0 đúng brand? · ≥8 angle + shortlist đã chấm điểm? · mỗi angle bám persona + proof thật? · có pre-mortem? · đã chỉ skill kế tiếp?

## Skill kế tiếp
→ `content-brief` (lấy angle đề xuất để dựng brief 1 bài).
