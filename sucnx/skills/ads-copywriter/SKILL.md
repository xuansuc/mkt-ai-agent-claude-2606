---
name: ads-copywriter
description: Viết AD COPY cho quảng cáo trả phí theo từng giai đoạn phễu (TOFU/MOFU/BOFU) + nhiều variant để A/B test, sẵn paste vào Ads Manager (primary text · headline · description · CTA). Dùng skill này KHI cần copy quảng cáo, "viết ads", "copy quảng cáo Facebook/Google", "variant A/B". Đọc media-plan/brief + L0 (voice, product-truth, locale). KHÁC `copywriter` (content thường) — đây là chuyên gia ad có variant theo phễu + A/B. Mọi claim verify `product-truth`, không vượt ranh giới claim.
---

# ads-copywriter

**Layer:** L3 · Producer (Ads) · **Pattern:** Linear / Source-Driven · **Output:** ad copy `.md`

## Bước 0 — Nạp brand
Đọc `brands/_active.md` → `brand-system.md` (voice, từ cấm, **locale**) · `product-truth.md` (proof + ranh giới claim).

## SOP
1. **Verify input:** media-plan/brief (audience · giai đoạn phễu · offer · KPI).
2. **Viết theo giai đoạn:** TOFU (hook nhận biết, ít chốt) · MOFU (giá trị/so sánh) · BOFU (offer + CTA mạnh).
3. **2–3 variant/asset** *(Spectrum)* khác hook/angle để A/B (mỗi variant đổi đúng 1 biến).
4. **Cấu trúc ad:** primary text · headline · description · CTA button.
5. **Self-check:** không từ cấm? · không vượt claim? · đúng locale? · proof verify được?

## Output template
```markdown
# Ad copy: [brand] — [giai đoạn phễu]
| Variant | Primary text | Headline | Description | CTA | Biến test |
|---|---|---|---|---|---|
## Proof check
| Claim | Nguồn product-truth |
```

## DoD
Đã load voice/proof/locale? · copy theo giai đoạn phễu? · ≥2 variant đổi 1 biến? · đủ trường ad? · claim-safe?

## Skill kế tiếp
→ `critic-qa` (gác cổng trước khi đẩy ads).
