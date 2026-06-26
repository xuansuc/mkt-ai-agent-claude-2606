---
name: workspace-librarian
description: Bảo trì "thư viện" engine — rà skill trùng/chồng chéo, kiểm tra brand pack đúng schema, dọn/archive artifact cũ, chống drift reference dùng chung. Dùng skill này KHI "dọn workspace", "kiểm tra brand pack", "có skill trùng không", "audit hệ thống", hoặc maintenance định kỳ. KHÔNG sản xuất nội dung.
---

# workspace-librarian

**Layer:** L4 · Meta · **Output:** librarian report `.md`

## Mục đích
Giữ engine sạch khi quy mô lớn dần — chống trùng skill, chống brand drift, chống rác.

## SOP
1. **Rà `skills/`:** phát hiện skill mô tả chồng chéo / trigger trùng → đề xuất gộp hoặc làm rõ ranh giới.
2. **Validate brand pack:** mỗi `brands/*/0_truth/` đủ 5 file đúng `_schema/`? Liệt kê `[TODO]`/`[giả định]` tồn đọng.
3. **Reference dùng chung:** `_meta/CONVENTION.md` · `_meta/THINKING-PRINCIPLES.md` · `_schema/` — cảnh báo chỗ skill tham chiếu lệch/cũ (drift).
4. **Dọn `work/`:** đề xuất archive artifact cũ.
5. **Báo cáo health** + việc cần làm (ưu tiên).

## Output template
```markdown
# Librarian report — [ngày]
## Skill trùng/chồng chéo
## Brand pack thiếu schema / TODO tồn đọng
## Drift reference dùng chung
## Đề xuất archive
## Health & việc cần làm (ưu tiên)
```

## DoD
Đã rà skills + brand packs + references? · liệt kê TODO tồn đọng? · báo cáo có ưu tiên?

## Skill kế tiếp
→ `agent-creator` (nếu cần gộp/tạo) · sửa L0/skill theo báo cáo.
