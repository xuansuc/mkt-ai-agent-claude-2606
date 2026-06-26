---
description: sucnx — đổi brand đang active.
argument-hint: <brand-slug>
---

Đổi brand đang active của sucnx sang: **$ARGUMENTS**

1. Kiểm tra `sucnx/brands/$ARGUMENTS/` có tồn tại không. Nếu KHÔNG → liệt kê các brand có sẵn trong `sucnx/brands/` và dừng.
2. Nếu có → cập nhật `sucnx/brands/_active.md`, đặt dòng `active: $ARGUMENTS`.
3. Xác nhận ngắn gọn brand active hiện tại + locale của nó (đọc `brand-system.md`).
