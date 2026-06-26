---
name: evidence-miner
description: Tìm BẰNG CHỨNG cho một thông điệp/claim — reasoning ngược để chọn 2–4 trụ evidence phù hợp từ 7 trụ, rồi shortlist ~10 ý cụ thể. Dùng skill này KHI thông điệp yếu/thiếu lực, cần "đắp bằng chứng", "tìm proof/số liệu/lý lẽ", "làm claim cứng hơn". Mọi evidence phải verify được trong `product-truth` (không bịa).
---

# evidence-miner

**Layer:** L2 · Specialist (miner) · **Pattern:** Funnel / Filter-Driven · **Output:** evidence shortlist `.md`

## Bước 0 — Nạp brand
Đọc `brands/_active.md` → `product-truth.md` (nguồn proof + ranh giới claim) · `audience-personas.md`.

## 7 trụ evidence
số liệu sản phẩm · nghiên cứu khoa học · lời chuyên gia · dữ liệu thị trường · anecdote người dùng · quan sát hành vi · tin tức/case.

## SOP
1. Nhận 1 claim/message cần chống lưng.
2. **Reasoning ngược:** với audience này, trụ evidence nào thuyết phục nhất → chọn 2–4 trụ.
3. **Shortlist ~10 evidence cụ thể**, mỗi cái ghi **nguồn verify** trong `product-truth`. Thiếu nguồn → `[cần proof]`, KHÔNG bịa.
4. 80/20: đánh dấu 3 evidence mạnh nhất.
5. Pre-mortem: claim nào còn hổng, cần thu thập thêm gì.

## Output template
```markdown
# Evidence: [claim]
Trụ đã chọn: …
| # | Evidence cụ thể | Trụ | Nguồn (product-truth) |
## Top 3 mạnh nhất
## Còn hổng / cần thu thập
```

## DoD
Chọn 2–4 trụ hợp audience? · mỗi evidence có nguồn (hoặc [cần proof])? · top 3? · nêu chỗ hổng?

## Skill kế tiếp
→ `content-brief` / `message-architect` / `copywriter` (đắp proof vào).
