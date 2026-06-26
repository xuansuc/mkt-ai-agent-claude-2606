---
description: sucnx — chạy vòng L5 (đo lường → insight → đề xuất cập nhật L0) cho brand active.
argument-hint: [kỳ, vd "tháng 6/2026"]
---

Chạy vòng tail-loop L5 cho brand đang active (đọc `sucnx/brands/_active.md`). Kỳ: **$ARGUMENTS** (nếu trống thì lấy kỳ gần nhất có dữ liệu).

1. Đọc dữ liệu trong `sucnx/brands/<active>/5_data/`. Nếu trống → báo cần thêm dữ liệu hiệu suất.
2. Chạy tuần tự theo SKILL.md: `performance-analyst` → `content-analyst` → `insight-collector`.
3. Trả về: insight (kèm evidence) + **đề xuất diff L0 chờ duyệt** + ghi log `5_data/insights-<kỳ>.md`.
4. Nhắc: vòng khép kín khi user duyệt diff → cập nhật L0 → `/content` kế tiếp dùng L0 mới.
