# Cài đặt sucnx — đội ngũ marketing AI cho Claude Code

`sucnx` là một **plugin cho Claude Code**: tự viết bài, quảng cáo, thiết kế, chiến lược — tái sử dụng cho nhiều thương hiệu. Mỗi thương hiệu chỉ cần khai "nguồn sự thật" (giọng văn, khách hàng, màu/font) một lần.

---

## Cần có
- **Claude Code** bản tương đối mới (có lệnh `/plugin`).

## Cài đặt — 2 lệnh
Mở Claude Code, gõ lần lượt trong ô chat:
```
/plugin marketplace add xuansuc/mkt-ai-agent-claude-2606
/plugin install sucnx@sucnx-marketplace
```
Đóng/mở lại Claude Code một lần. Gõ `/` thấy **`/content`** là đã cài xong. ✅

## Dùng lần đầu
1. Tạo thương hiệu của bạn:
   ```
   /brand-onboard https://website-cua-ban.com
   ```
   Trả lời vài câu hỏi (giọng văn · khách hàng & nỗi đau · mục tiêu · màu/font) → engine sinh hồ sơ thương hiệu.
2. Bắt đầu tạo nội dung:
   ```
   /content viết LinkedIn post về <chủ đề>
   ```

**Các lệnh khác:**
- `/use-brand <tên>` — đổi thương hiệu đang chạy
- `/review` — đo lường hiệu suất → đề xuất cải thiện
- `/brand-onboard <URL>` — thêm thương hiệu mới

📖 Hướng dẫn đầy đủ: mở file `sucnx/USER_GUIDE.md` trong repo.

---

## Nếu gõ `/plugin` không có
Claude Code của bạn hơi cũ → cập nhật lên bản mới nhất rồi làm lại. (Hoặc xem cách "project-local" trong file `INSTALL.md` ở repo.)

**Repo:** https://github.com/xuansuc/mkt-ai-agent-claude-2606
