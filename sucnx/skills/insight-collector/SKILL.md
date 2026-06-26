---
name: insight-collector
description: Tổng hợp kết quả phân tích (định lượng + định tính) thành insight có cấu trúc, rồi ĐỀ XUẤT cập nhật L0 của brand — khép vòng phản hồi về chiến lược (L1). Dùng skill này SAU khi đã có performance/content analysis, hoặc khi user nói "rút insight", "cập nhật chiến lược từ dữ liệu", "tổng kết học được gì". Ghi log insight vào `5_data/` và đề xuất diff cho L0 — KHÔNG tự ghi đè sự thật brand đã xác nhận, chờ duyệt.
---

# insight-collector

**Layer:** L5 · Tail Loop (khép vòng) · **Pattern:** Funnel / Filter-Driven · **Output:** insights log + đề xuất diff L0

## Mục đích
Đây là **mắt xích đóng vòng**: biến số liệu thành thay đổi trong L0 → để vòng sản xuất kế tiếp thông minh hơn. Không có nó, hệ thống chạy mãi mà không học từ thị trường.

## Bước 0 — Nạp
Đọc output của `performance-analyst` + `content-analyst`, và L0 hiện tại của brand (`brands/<active>/0_truth/`).

## SOP
1. **Tổng hợp 3–5 insight cao tin cậy**, mỗi insight kèm **evidence** (số liệu cụ thể). Phân biệt rõ *insight-từ-data* vs *giả định*.
2. **Map mỗi insight → file L0 nên cập nhật:** persona (pain/desire nào resonate), kpi (north-star/mix/target), brand-system (voice/từ), competitor, product-truth (proof mới).
3. **Ghi log:** `brands/<active>/5_data/insights-<YYYY-MM>.md` (tích lũy theo thời gian — bộ nhớ học của brand).
4. **Đề xuất diff L0** dạng "trước → sau" cho từng file, **chờ người duyệt**. L0 là source of truth — không tự ghi đè dữ liệu brand đã xác nhận.
5. **Chuyển cho L1:** đánh dấu insight nào cần `marketing-strategist`/`campaign-orchestrator` xử lý (nếu chưa build → ghi rõ để leader làm tay).

## Quy tắc đóng vòng
Sau khi user duyệt diff → cập nhật L0 → vòng `/content` kế tiếp tự dùng L0 mới (producer luôn đọc `0_truth/`). Đó là lúc vòng khép kín.

## Output template
```markdown
# Insights: [brand] — [kỳ]
## Insight (mỗi cái: nội dung · evidence · độ tin cậy)
## Đề xuất cập nhật L0 (diff, chờ duyệt)
| File L0 | Trước | Sau | Lý do |
## Chuyển cho L1 (strategy)
```

## DoD
Mỗi insight có evidence? · phân biệt data vs giả định? · đã map vào file L0? · đã ghi insights log? · diff L0 rõ "trước→sau" và chờ duyệt? · đánh dấu việc cho L1?

## Skill kế tiếp
→ L1 `marketing-strategist`/`campaign-orchestrator` (khi build) · hoặc `/content` vòng kế dùng L0 đã cập nhật.
