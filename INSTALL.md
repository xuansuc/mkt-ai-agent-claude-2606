# Cài đặt sucnx — đọc file này trước

`sucnx` là một **plugin cho Claude Code**: bộ "đội ngũ marketing" tự động (viết bài, ads, thiết kế, chiến lược) tái sử dụng cho nhiều thương hiệu.

Gói này là một **marketplace** (thư mục có `.claude-plugin/marketplace.json` + plugin `sucnx/`). Cài bằng cách thêm thư mục này vào Claude Code rồi install.

---

## Cần có
- **Claude Code** bản tương đối mới (có lệnh `/plugin`). Nếu gõ `/plugin` mà không có → xem mục **"Nếu không có /plugin"** ở cuối.

## 3 bước cài

**1. Giải nén** gói này ra một thư mục **đường dẫn đơn giản, không dấu cách**, ví dụ:
- Windows: `D:\sucnx\`  → sau khi giải nén có `D:\sucnx\sucnx-marketplace\`
- Mac: `~/sucnx/`       → có `~/sucnx/sucnx-marketplace/`

> Ghi nhớ đường dẫn tới thư mục **`sucnx-marketplace`** (thư mục chứa `.claude-plugin`).

**2. Thêm marketplace** — mở Claude Code, gõ trong ô chat:
```
/plugin marketplace add D:\sucnx\sucnx-marketplace
```
(thay bằng đường dẫn của bạn). Nếu hỏi tin tưởng nguồn → đồng ý.

**3. Cài plugin:**
```
/plugin install sucnx@sucnx-marketplace
```
Hoặc gõ `/plugin` → menu hiện ra → chọn cài **sucnx**.

Đóng/mở lại Claude Code một lần. Gõ `/` thấy **`/content`** là xong. ✅

---

## Dùng lần đầu
Gói này chưa kèm thương hiệu nào (trống). Tạo thương hiệu của bạn:
```
/brand-onboard https://website-cua-ban.com
```
Trả lời vài câu (giọng văn · khách hàng · mục tiêu · màu/font) → engine sinh "nguồn sự thật" (L0). Sau đó:
```
/content viết LinkedIn post về <chủ đề>
```
Các lệnh khác: `/use-brand <tên>` (đổi thương hiệu), `/review` (đo lường → cải thiện).

**Hướng dẫn đầy đủ:** mở `sucnx/USER_GUIDE.md` trong gói này.

---

## Nếu không có `/plugin` (bản Claude Code cũ)
Vẫn dùng được theo kiểu **project-local**:
1. Chép thư mục `sucnx/` (trong gói) vào thư mục dự án bạn sẽ làm việc.
2. Tạo thư mục `.claude/commands/` trong dự án đó, chép các file lệnh vào (xem `sucnx/USER_GUIDE.md` mục cài đặt — lưu ý các đường dẫn trong lệnh phải trỏ tới `sucnx/...`).
3. Mở Claude Code **ngay tại thư mục dự án đó** → gõ `/content`.

Cần hỗ trợ, hỏi người gửi gói cho bạn.
