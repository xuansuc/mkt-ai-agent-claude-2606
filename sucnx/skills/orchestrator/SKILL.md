---
name: orchestrator
description: Điểm vào MẶC ĐỊNH của sucnx. Dùng skill này BẤT CỨ KHI NÀO người dùng đưa một yêu cầu marketing bằng lời thường và muốn ra KẾT QUẢ, chứ không gọi đích danh một skill — vd "viết LinkedIn post về X", "làm carousel về Y cho brand Z", "cần ý tưởng content cho…", "viết email nurture về…". Nó tự xác định brand đang active, parse yêu cầu thành deliverable/chủ đề/persona/funnel/mode, chọn đúng CHUỖI skill, chạy tuần tự (truyền output bước trước sang bước sau), rồi trả deliverable cuối + QA. KHÔNG dùng khi user gọi đích danh 1 skill để chạy thẳng, hoặc khi yêu cầu không phải việc marketing.
---

# orchestrator

**Layer:** L4 · Meta (nhạc trưởng) · **Output:** deliverable cuối + run log `.md`

## Vai trò
Điều phối, KHÔNG tự làm. Nó không viết copy, không brainstorm — nó **chọn và chạy đúng các skill** theo thứ tự, để người dùng không phải nhớ chuỗi 4–5 bước. Đây là thứ biến một đống skill rời thành một dây chuyền dùng được.

## Bước 0 — Xác định brand (bắt buộc)
1. Đọc `brands/_active.md` → `active:`.
2. Nếu yêu cầu **nêu tên brand khác** đã có pack (`brands/<tên>/` tồn tại) → đổi `_active` sang brand đó (hoặc xác nhận 1 câu nếu mơ hồ).
3. Nếu brand chưa có pack → DỪNG, đề xuất chạy `brand-intake` trước. Engine không chạy khi thiếu L0.

## Bước 1 — Parse yêu cầu thành slots
Rút từ câu của user (hỏi gọn 1 lượt nếu thiếu cái cốt lõi):
- **Deliverable:** post (LinkedIn/Facebook) · blog · email · caption · carousel · ý tưởng · brief · QA · ...
- **Chủ đề:** …
- **Persona:** mặc định = persona PRIMARY trong L0; đổi nếu user chỉ định.
- **Funnel:** suy luận (chia sẻ/nhận biết → TOFU · cân nhắc → MOFU · chốt → BOFU).
- **Mode:** mặc định `balanced`; "nhanh/gấp" → `speed`; "kỹ/pillar/quan trọng" → `quality`/`future-proof`.
- **Có cần visual không?** (carousel/ảnh kèm → có).

## Bước 2 — Chọn chuỗi skill (routing table)
| Yêu cầu | Chuỗi |
|---|---|
| Bài content (post/blog/email/caption) | `angle-miner` → `content-brief` → `copywriter` → `critic-qa` |
| Bài content **kèm visual / carousel** | `angle-miner` → `content-brief` → `copywriter` → `visual-communicator` → `critic-qa` |
| Deliverable **dài/phức tạp** (landing · deck · webinar · email sequence) | `angle-miner` → `message-architect` → `copywriter` → `critic-qa` |
| Kịch bản **video** | `video-script-producer` → `critic-qa` |
| **Tài liệu bán hàng** (battlecard/script/FAQ/objection) | `sales-enabler` → `critic-qa` |
| **Quảng cáo trả phí** (media plan) | `ads-planner` → `ads-copywriter` → `critic-qa` |
| **Ad copy** (đã có plan) | `ads-copywriter` → `critic-qa` |
| **Spec/asset thiết kế** (carousel · landing · Canva · resize) | (`visual-communicator` →) `designer-producer` → `critic-qa` |
| **Chiến lược tổng / GTM** | `marketing-strategist` |
| **Kế hoạch campaign đa kênh / calendar** | `campaign-orchestrator` → `narrative-strategist` → (chuỗi từng deliverable) |
| **Đo lường / insight** | `performance-analyst` → `content-analyst` → `insight-collector` |
| Chỉ cần ý tưởng/góc | `angle-miner` |
| Đã có angle, cần brief | `content-brief` |
| Đã có copy, cần visual | `visual-communicator` → `critic-qa` |
| QA một bản có sẵn | `critic-qa` |

Nếu yêu cầu cần một skill CHƯA build (vd `device-miner`, `evidence-miner`, `frame-packager`, `benefit-card-generator`, `demo-scripter`, `agent-creator`, `workspace-librarian`): nói rõ skill còn thiếu, đề xuất `agent-creator` để build, và làm phần gần nhất có thể bằng skill hiện có.

## Bước 3 — Chạy chuỗi
Tạo folder `brands/<active>/work/<YYYY-MM-DD>-<slug>/`. Lần lượt từng skill:
1. Đọc SKILL.md của skill đó, chạy với **mode** đã chọn.
2. Truyền output bước trước làm input bước sau (angle → brief → copy → …).
3. Lưu artifact mỗi bước (`1-…md`, `2-…md`, …) → giữ traceability.

## Bước 4 — Xử lý verdict của critic-qa
- **Approve** → giao.
- **Fix/Redo** → trả lại `copywriter` (hoặc skill liên quan) sửa đúng lỗi đã liệt kê, chạy lại critic-qa. Tối đa 2 vòng; vẫn fail thì giao kèm cảnh báo + lỗi tồn đọng.

## Bước 5 — Giao
Trả về: **deliverable cuối** + trace 1 dòng (chuỗi skill đã chạy) + verdict QA + đường dẫn artifacts. KHÔNG tự ý chỉnh deliverable ngoài những gì critic-qa yêu cầu.

## Quy tắc
- Nhạc trưởng không lấn việc nhạc công: mọi nội dung do skill chuyên môn sinh ra.
- Chỉ hỏi user khi: brand chưa rõ/chưa có pack, hoặc deliverable mơ hồ không suy luận được.
- Tôn trọng `_meta/CONVENTION.md` (no-brand-leakage) và `THINKING-PRINCIPLES.md`.

## DoD
Đã xác định brand? · parse đủ slots? · chọn đúng chuỗi (hoặc báo skill thiếu)? · chạy tuần tự + lưu artifact? · xử lý verdict QA? · giao kèm trace + đường dẫn?

## Skill liên quan
Gọi: `angle-miner` · `content-brief` · `copywriter` · `visual-communicator` · `critic-qa`. Khi thiếu vai trò: `agent-creator`. Onboard brand mới: `brand-intake`.
