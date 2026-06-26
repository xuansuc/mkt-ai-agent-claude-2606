---
name: content-analyst
description: Phân tích hiệu suất NỘI DUNG — bài/angle/hook/format/persona nào hiệu quả, tìm pattern winner/loser, audit nội dung. Dùng skill này KHI review nội dung, "bài nào hiệu quả", report nội dung tháng, "nên làm thêm dạng nào". Đọc `brands/<active>/5_data/` + các artifact trong `work/`. KHÔNG sản xuất nội dung mới.
---

# content-analyst

**Layer:** L5 · Tail Loop · **Pattern:** Funnel / Filter-Driven · **Output:** content audit `.md`

## Mục đích
Tìm ra **công thức đang chạy**: angle/hook/format nào kéo đúng north-star, để producer nhân bản thay vì đoán.

## Bước 0 — Nạp
1. Đọc `brands/_active.md` → `kpi-standards.md` (north-star).
2. Đọc số liệu nội dung trong `5_data/` + các artifact đã sản xuất trong `brands/<active>/work/`.

## SOP
1. **Gắn tag mỗi bài:** angle · hook-type · format · persona · funnel (lấy từ artifact `work/`).
2. **Đối chiếu engagement & north-star:** mỗi bài đóng góp bao nhiêu vào chỉ số thật (vd lead đủ thông tin), không chỉ reach/like.
3. **Rút pattern** *(80/20):* nhóm winner (đặc điểm chung) vs loser.
4. **Đề xuất:** dạng nào **nhân lên**, dạng nào **dừng**, hook/CTA nào nên chuẩn hóa.

## Output template
```markdown
# Content audit: [brand] — [kỳ]
## Bảng bài (tag + đóng góp north-star)
## Pattern WINNER (đặc điểm chung)
## Pattern LOSER
## Double-down / Drop
## Hook & CTA nên chuẩn hóa
```

## DoD
Đã gắn tag theo artifact work/? · chấm theo north-star? · pattern winner/loser rõ? · đề xuất double-down/drop cụ thể?

## Skill kế tiếp
→ `insight-collector` (tổng hợp & đề xuất cập nhật L0).
