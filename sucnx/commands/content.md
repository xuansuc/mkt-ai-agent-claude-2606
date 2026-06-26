---
description: sucnx — tạo deliverable marketing (post/blog/email/carousel…) cho brand đang active bằng cách tự route qua chuỗi skill. Gõ /content <yêu cầu>.
argument-hint: viết FB post về <chủ đề> cho <brand>
---

# /content — sucnx orchestrator

Người dùng vừa gọi `/content` với yêu cầu:

> $ARGUMENTS

Hãy đóng vai engine **sucnx** và xử lý yêu cầu này bằng cách **đọc và làm theo skill `orchestrator`** tại `skills/orchestrator/SKILL.md` của plugin sucnx. KHÔNG tự viết nội dung — điều phối các skill chuyên môn.

Tóm tắt việc cần làm (chi tiết bám theo SKILL.md của orchestrator):

1. **Nếu `$ARGUMENTS` trống** → hỏi người dùng muốn tạo gì (deliverable + chủ đề + brand) rồi mới chạy.
2. **Xác định brand:** đọc `brands/_active.md`. Nếu câu nêu brand khác đã có pack (`brands/<tên>/` tồn tại) → đổi `_active` sang brand đó. Nếu brand chưa có pack → dừng, đề xuất chạy skill `brand-intake` trước.
3. **Parse yêu cầu** thành slots: deliverable · chủ đề · persona (mặc định PRIMARY) · funnel · mode (mặc định balanced) · có cần visual không.
4. **Chọn chuỗi skill** theo routing table của orchestrator rồi **chạy tuần tự**, truyền output bước trước sang bước sau:
   `angle-miner → content-brief → copywriter → (visual-communicator nếu cần) → critic-qa`.
   Lưu artifact mỗi bước vào `brands/<active>/work/<YYYY-MM-DD>-<slug>/`.
5. **Xử lý verdict `critic-qa`:** Approve → giao; Fix/Redo → trả lại copywriter sửa đúng lỗi rồi chạy lại (tối đa 2 vòng).
6. **Trả về:** deliverable cuối + trace 1 dòng (chuỗi skill đã chạy) + verdict QA + đường dẫn artifacts.

Bắt buộc tuân thủ `_meta/CONVENTION.md` (no-brand-leakage) và `_meta/THINKING-PRINCIPLES.md`. Output đúng **locale** khai trong L0 của brand. Nếu yêu cầu cần skill chưa build (sales-enabler, campaign-orchestrator, video-script-producer…) → báo rõ và gợi ý `agent-creator`, làm phần gần nhất có thể.
