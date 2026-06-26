---
name: performance-analyst
description: Đọc dữ liệu hiệu suất marketing THẬT của brand (từ `brands/<active>/5_data/`), đối chiếu với north-star & target trong `kpi-standards.md`, chẩn đoán cái gì đang hiệu quả / không, truy nguyên nhân gốc và đề xuất hành động 80/20. Dùng skill này KHI cần đọc số liệu, làm report tuần/tháng, hiểu vì sao chỉ số tăng/giảm, "đánh giá hiệu quả campaign". KHÔNG sản xuất nội dung. Cần có dữ liệu trong `5_data/` — nếu trống thì báo user.
---

# performance-analyst

**Layer:** L5 · Tail Loop · **Pattern:** Funnel / Filter-Driven · **Output:** performance report `.md`

## Mục đích
Biến số liệu thô thành chẩn đoán: cái gì đáng nhân lên, cái gì nên dừng — chấm theo **north-star thật của brand**, không theo vanity metric.

## Bước 0 — Nạp chuẩn (bắt buộc)
1. Đọc `brands/_active.md` → load `kpi-standards.md` (north-star · funnel · target · định nghĩa lead).
2. Đọc dữ liệu trong `brands/<active>/5_data/`. Trống → DỪNG, báo user cần dữ liệu.

## SOP
1. **Map dữ liệu** vào phễu & **north-star** (đừng để vanity metric như reach che mất chỉ số thật).
2. **Hiệu quả vs target:** cái gì đạt/không (đặc biệt theo north-star, không chỉ theo reach).
3. **Truy nguyên nhân gốc** *(5-why)* cho gap lớn nhất hoặc winner bất ngờ.
4. **Đề xuất 80/20:** ít hành động, tác động lớn — nhân winner, dừng loser.
5. **Khoảng mù dữ liệu** *(Unknown Unknowns):* số liệu nào còn thiếu để kết luận chắc.

## Output template
```markdown
# Performance report: [brand] — [kỳ]
## North-star kỳ này
## Hiệu quả vs target (bảng)
## Winner / Loser + vì sao
## Root-cause (5-why) cho gap chính
## Hành động đề xuất (80/20)
## Khoảng mù dữ liệu
```

## DoD
Đã load kpi-standards? · chấm theo north-star (không vanity)? · có root-cause? · hành động 80/20 cụ thể? · nêu data gap?

## Skill kế tiếp
→ `content-analyst` (đào sâu nội dung) · `insight-collector` (tổng hợp & vòng về L0).
