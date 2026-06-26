---
name: brand-intake
description: Onboard một THƯƠNG HIỆU MỚI vào sucnx — nghiên cứu + phỏng vấn rồi sinh ra trọn bộ L0 brand pack (5 file nguồn sự thật) đúng theo hợp đồng schema trong `_schema/`. Dùng skill này BẤT CỨ KHI NÀO cần thêm một brand/khách mới, "tạo brand pack", "onboard brand mới", "thêm thương hiệu", hoặc khi `orchestrator` dừng vì một brand chưa có L0. Nó tự pre-fill dữ kiện công khai từ website của brand, chỉ hỏi những gì nội bộ (giọng, persona, KPI, ranh giới claim), rồi ghi `brands/<slug>/0_truth/`. KHÔNG dùng để sửa L0 của brand đã có (chỉ cần sửa file trực tiếp) hay để sản xuất nội dung (đó là `orchestrator` + producers).
---

# brand-intake

**Layer:** L4 · Meta · **Pattern:** Reverse / Target-Driven (đích = đủ 5 file L0 đúng schema) · **Output:** brand pack `brands/<slug>/0_truth/`

## Skill này tạo ra gì
Một brand pack hoàn chỉnh để engine chạy được cho brand mới — chỉ tốn một buổi phỏng vấn. Đây là thứ làm cho mục tiêu "mỗi brand chỉ cấp L0" trở nên rẻ và lặp lại được.

## Bước 0 — Đọc hợp đồng
Đọc `_schema/` (5 file `*.schema.md`) để biết **đích cần điền**: brand-system · product-truth · audience-personas · kpi-standards · competitor-intel. Schema là khung; intake chỉ đi điền cho đủ.

## SOP
1. **Nhận input:** tên brand + website (nếu có) + tài liệu sẵn có (brand guideline, case study…).
2. **Nghiên cứu công khai** *(giảm gánh cho user)*: nếu có URL → WebFetch trang chủ + trang dịch vụ/about; WebSearch tên brand để lấy review/đối thủ. Rút: dịch vụ, định vị, proof công khai, ngành, đối thủ, giá.
3. **Pre-fill nháp** các phần lấy được từ web; **khoanh vùng phần chỉ nội bộ biết**: giọng/tone, persona chi tiết, KPI, naming, ranh giới claim.
4. **Phỏng vấn** theo bộ câu hỏi nhóm theo 5 file L0 → xem `references/intake-questions.md`. Đánh dấu **3 câu cốt lõi** (giọng · persona PRIMARY + pain · north-star KPI); cho phép "fast pass" — trả lời tối thiểu là dựng được v1.
5. **Kiểm tra ngành nhạy cảm** (sức khỏe/y tế · tài chính · pháp lý · trẻ em) → đặt **ranh giới claim chặt** vào product-truth §5 + giọng thận trọng + disclaimer bắt buộc. Xem `references/intake-questions.md` (mục Sensitive domains).
6. **Sinh 5 file L0** đúng schema: đủ mọi mục `##`; chỗ tự suy luận ghi `[giả định]`, chỗ thiếu ghi `[TODO]`; điền **locale** (ngôn ngữ output).
7. **Tạo cấu trúc:** `brands/<slug>/0_truth/<5 file>.md` + `brands/<slug>/5_data/README.md`.
8. **Hỏi** có set brand này thành active không → cập nhật `brands/_active.md`.
9. **Xuất intake summary:** liệt kê phần đã xác nhận vs `[giả định]`/`[TODO]` để user soi nhanh.

## Quy tắc
- Slug brand: chữ thường, gạch nối, không dấu (vd `acme-corp`, `my-brand`).
- KHÔNG bịa proof/số liệu — không có nguồn thì `[cần proof]`.
- Mỗi file L0 phải **pass schema** (đủ các mục `##` của file schema tương ứng).
- Với ngành nhạy cảm: thà thận trọng còn hơn over-claim — đây là điều `critic-qa` sẽ soi sau.

## references
- `references/intake-questions.md` — bộ câu hỏi đầy đủ theo 5 file L0 + xử lý ngành nhạy cảm. Đọc khi tới Bước 4–5.

## DoD
Đã đọc schema? · đã research web (nếu có URL)? · đã hỏi đủ (ít nhất 3 câu cốt lõi)? · 5 file L0 pass schema + đánh dấu giả định? · có locale? · ngành nhạy cảm đã đặt ranh giới claim? · đã tạo folder + 5_data? · có intake summary?

## Skill kế tiếp
→ `orchestrator` (bắt đầu sản xuất nội dung cho brand mới) · sửa L0 trực tiếp nếu cần.
