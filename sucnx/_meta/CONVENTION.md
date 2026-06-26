# sucnx · CONVENTION v3 (engine rules)

Quy ước bắt buộc cho MỌI skill trong engine. `critic-qa` kiểm tra việc tuân thủ.

## 1. Cấu trúc agent
- **1 folder = 1 agent.** Bên trong: `SKILL.md` (entry point, ≤~500 dòng) + `references/` (load on-demand).
- **1 agent = 1 tầng (L1–L5) = 1 workflow pattern.** Cần 2 tầng/pattern → tách thành 2 agent.

## 2. SKILL.md gồm
vai trò · scope · khi nào gọi / không gọi · input · SOP 5–8 bước · 5 nguyên tắc tư duy · Mode Operators · output template · pitfalls · bảng references.

## 3. Luật TÁCH THƯƠNG HIỆU (no brand leakage) — QUAN TRỌNG NHẤT
- Skill **KHÔNG** chứa tên / sản phẩm / claim / ví dụ của bất kỳ brand cụ thể nào.
- Mọi thông tin brand **nạp từ L0 lúc chạy**, không hardcode.
- Tên skill không có tiền tố brand (KHÔNG `pika-...`).
- Ví dụ minh họa trong skill phải generic hoặc ghi rõ `[minh họa]`.

## 4. Nạp brand qua indirection
- Brand đang chạy đọc ở `brands/_active.md`.
- Skill load L0 từ `brands/<active>/0_truth/<file>.md` theo đúng schema trong `_schema/`.
- Skill chỉ tin **cấu trúc** (mục `##`), không tin nội dung.

## 5. Vật chất hóa nguyên liệu
- Mỗi output trung gian là 1 file `.md` có tên/path rõ, để tầng sau dùng lại (không giữ trong đầu).

## 6. Definition of Done (DoD)
Mỗi skill kết thúc bằng checklist: input đủ chưa? · output đúng schema chưa? · đã áp 5 nguyên tắc chưa? · có câu hỏi pre-mortem chưa? · đã chỉ skill kế tiếp chưa?
