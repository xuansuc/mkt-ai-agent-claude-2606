---
name: agent-creator
description: Tạo AGENT/SKILL MỚI cho engine khi xuất hiện vai trò chưa có. Dùng skill này KHI "tạo agent", "thêm skill", "thiết kế nhân sự ảo", "tách job", hoặc khi `orchestrator` báo thiếu skill. Quét workspace tránh trùng, chạy 7 bộ lọc chất lượng, đóng gói theo convention v3 + 5 nguyên tắc tư duy. KHÔNG dùng cho việc ad-hoc làm 1 lần.
---

# agent-creator

**Layer:** L4 · Meta · **Output:** `skills/<name>/SKILL.md` mới + cập nhật ROADMAP/orchestrator

## Mục đích
"Tuyển nhân sự ảo" — sinh skill mới đúng chuẩn engine, không trùng cái đã có.

## Bước 0 — Nạp chuẩn
Đọc `_meta/CONVENTION.md` · `_meta/THINKING-PRINCIPLES.md` · `_meta/ROADMAP.md` (xem skill đã có) · `_schema/` (nếu skill động tới L0).

## SOP (5 bước)
1. **Xác định I/O:** skill nhận gì, ra gì.
2. **Chọn anchor pattern:** Source / Target / Trigger-Driven (1 agent = 1 pattern).
3. **Thiết kế chuỗi chuyển hóa** + xác định **tầng** (1 agent = 1 tầng).
4. **Áp 5 nguyên tắc tư duy** vào SOP.
5. **Chạy 7 bộ lọc:** Role Clarity · Scope Boundaries · Competency · Executable SOP · Collaboration Contract · Definition of Done · Thinking Quality.
→ **Quét `skills/`** trước khi đề xuất để tránh trùng trigger/scope.

## Sau khi tạo
- Ghi `skills/<name>/SKILL.md` (frontmatter description "pushy" + body theo convention).
- Cập nhật `_meta/ROADMAP.md` (tick) và routing table của `orchestrator` nếu cần.

## DoD
Không trùng skill có sẵn? · đúng 1 tầng + 1 pattern? · qua 7 bộ lọc? · description rõ "gọi/không gọi"? · đã cập nhật ROADMAP + orchestrator?

## Skill kế tiếp
→ `critic-qa` (review skill mới) · `workspace-librarian` (đăng ký/đối chiếu).
