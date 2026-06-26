---
name: designer-producer
description: Tạo SPEC SẢN XUẤT thiết kế & code asset — Canva brief chi tiết, spec từng slide carousel, HTML landing/email, hướng dẫn resize ra đủ kích thước kênh. Dùng skill này KHI cần spec thiết kế sẵn-sàng-dựng hoặc asset có code, "spec design", "carousel brief chi tiết từng slide", "landing/email HTML", "resize asset đủ kích thước". Đọc output `visual-communicator` + L0 (brand-system: màu HEX, font). KHÁC `visual-communicator` (ý tưởng) — đây ra bản spec/code để dựng. Bám đúng màu/font brand; nếu L0 thiếu màu (`[TODO]`) thì nêu rõ.
---

# designer-producer

**Layer:** L3 · Producer (Design) · **Pattern:** Linear / Source-Driven · **Output:** design spec / HTML `.md`

## Bước 0 — Nạp brand
Đọc `brands/_active.md` → `brand-system.md` (**màu HEX · typography · do/don't visual**). Nếu màu/font còn `[TODO]` → nêu rõ và dùng placeholder, KHÔNG tự bịa màu ngoài hệ.

## Input
- Concept từ `visual-communicator` (hoặc copy + format) · loại output cần.

## SOP
1. **Chọn loại output:** Canva brief · spec slide carousel · HTML landing/email · resize guide.
2. **Spec chính xác:** layout/bố cục · **màu (HEX từ L0)** · font · vị trí copy · kích thước theo kênh.
3. **Nếu HTML:** sinh code dùng đúng brand token (màu/font), responsive, inline CSS cho email.
4. **Resize guide:** liệt kê kích thước chuẩn từng kênh (FB post/story · IG · LinkedIn · ads) từ 1 master.
5. **Self-check:** đúng palette/font brand? · text đúng locale? · đủ kích thước kênh cần?

## Output template
```markdown
# Design spec: [asset] — [loại]
Brand tokens: màu (HEX) · font (từ brand-system)
## Spec / Slide-by-slide / HTML code
## Kích thước xuất theo kênh
## Lưu ý brand (do/don't)
```

## DoD
Đã load màu/font brand (hoặc nêu [TODO])? · spec đủ để dựng? · đúng kích thước kênh? · đúng locale?

## Skill kế tiếp
→ `critic-qa` (check brand consistency).
