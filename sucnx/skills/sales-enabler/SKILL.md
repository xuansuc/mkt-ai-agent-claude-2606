---
name: sales-enabler
description: Soạn TÀI LIỆU BÁN HÀNG dùng được ngay — telesale/closing script, battlecard, objection handler, FAQ, pricing one-pager, pre-call checklist. Dùng skill này KHI cần trang bị tài liệu cho đội sale theo 1 segment / 1 đối thủ / 1 objection cụ thể; hoặc user nói "battlecard", "xử lý từ chối", "script telesale", "tài liệu sale", "FAQ bán hàng". Đọc L0 (product-truth, competitor-intel, personas, brand-system). Mọi proof verify từ `product-truth`, mọi so sánh đối thủ bám `competitor-intel`, không vượt ranh giới claim.
---

# sales-enabler

**Layer:** L3 · Producer · **Pattern:** Reverse / Target-Driven · **Output:** sales doc `.md`

## Mục đích
Biến sự thật sản phẩm + insight khách thành tài liệu đội sale mở ra dùng được ngay — bán bằng **outcome**, không phải feature.

## Bước 0 — Nạp brand (bắt buộc)
Đọc `brands/_active.md` → `product-truth.md` (proof + **ranh giới claim**) · `competitor-intel.md` · `audience-personas.md` (objection) · `brand-system.md` (voice, **locale**).

## SOP
1. **Chọn 1 mode:** Audience (segment + stage) · Competitor (1 đối thủ trong competitor-intel) · Objection (1 câu khách nói) · Cross-Asset.
2. **Framework flow 5 bước:** đồng cảm → insight → tiêu chí (đặt tiêu chí mua trước) → outcome → proof.
3. **Cấu trúc theo loại:** battlecard 6 phần (định vị ta/họ · điểm mạnh ta · điểm yếu họ · câu hỏi gài · phản biện · proof) · objection 3-layer (nghe → reframe → proof) · script theo flow 5 bước.
4. **Tuân thủ claim:** mọi proof verify `product-truth`; so sánh đối thủ trung thực theo `competitor-intel`, KHÔNG dìm bịa; ngành nhạy cảm giữ ranh giới §5.
5. Output đúng **locale**.

## Output template
```markdown
# [Loại tài liệu] — mode: [Audience/Competitor/Objection/Cross-Asset]
Đối tượng/đối thủ/objection: …

## Nội dung (theo cấu trúc loại tài liệu)
…

## Proof check
| Câu/claim | Nguồn (product-truth/competitor-intel) |
```

## DoD
Đã load L0? · đúng 1 mode? · bán bằng outcome? · proof verify được? · so sánh đối thủ trung thực? · đúng locale + claim boundary?

## Skill kế tiếp
→ `critic-qa` (gác cổng trước khi giao sale).
