# Hướng dẫn sử dụng — sucnx

*Marketing Agent Engine cho Claude Code · v1.1*

> Một "đội marketing ảo" 26 skill. Bạn chỉ cấp **L0 (sự thật về thương hiệu)**; engine sản xuất nội dung, quảng cáo, thiết kế — dưới sự điều phối của **lớp chiến lược Leader** — và tự học từ số liệu.

## Mục lục
1. sucnx là gì
2. Cài đặt
3. Bắt đầu nhanh (5 phút)
4. Bốn lệnh chính
5. Cách viết yêu cầu tốt
6. ⭐ Ý tưởng cốt lõi — 3 phòng thực thi × 6 tầng, điều phối bởi lớp Leader
7. ⭐ Chi tiết 3 phòng + lớp Leader (kèm ví dụ)
8. Vòng học (L5)
9. Quản nhiều thương hiệu
10. Xử lý sự cố (FAQ)
- Phụ lục: 26 skill theo tầng

---

## 1. sucnx là gì
- Một engine biến marketing thành **dây chuyền sản xuất** gồm các skill chuyên biệt, thay vì nhồi mọi thứ vào một prompt dài.
- **Triết lý:** mỗi skill làm đúng một việc thật sắc → ghép lại thành deliverable chất lượng, truy vết được.
- **Đa thương hiệu:** đổi brand chỉ là đổi **L0**; toàn bộ skill giữ nguyên.

## 2. Cài đặt

### Cách A — cài như plugin *(khuyên dùng cho cả team)*
1. Giải nén gói → ra thư mục `sucnx-marketplace/`.
2. Trong Claude Code:
   ```
   /plugin marketplace add <đường-dẫn>/sucnx-marketplace
   /plugin install sucnx
   ```
3. Lệnh xuất hiện dạng `/content` (hoặc `/sucnx:content`); skills nạp tự động.

### Cách B — dùng nhanh, không cài *(project-local)*
- Đặt thư mục `sucnx/` vào project của bạn, rồi copy các file trong `sucnx/commands/` sang `.claude/commands/` của project.

### Dữ liệu brand sống ở đâu?
- Plugin sau khi cài là **read-only** → tạo thư mục **`brands/` trong project của bạn** (nơi bạn mở Claude Code). Engine ghi mọi artifact vào `brands/<brand>/work/`.
- `/brand-onboard` sẽ tạo cấu trúc này giúp bạn.

## 3. Bắt đầu nhanh (5 phút)

**Bước 1 — Tạo brand đầu tiên**
```
/brand-onboard https://acme.com
```
Engine đọc website + hỏi bạn **3 câu cốt lõi** (giọng thương hiệu · khách số 1 + 3 nỗi đau · chỉ số quan trọng nhất) và màu/font nếu có → sinh **5 file L0**.

**Bước 2 — Tạo deliverable đầu tiên**
```
/content viết LinkedIn post về "tự động hoá onboarding" cho acme
```
→ Nhận một post hoàn chỉnh đúng giọng brand + verdict QA + đường dẫn file.

**Bước 3 — (khi có số liệu) Khép vòng học**
```
/review tháng này
```
→ Engine đọc số liệu, chỉ ra cái gì hiệu quả, đề xuất cập nhật L0.

> **L0 là gì?** 5 file "sự thật" về brand: `brand-system` (giọng·màu·locale) · `product-truth` (proof + ranh giới claim) · `audience-personas` · `kpi-standards` · `competitor-intel`. Đây là thứ **duy nhất** khác nhau giữa các brand.

## 4. Bốn lệnh chính

| Lệnh | Cú pháp | Làm gì |
|---|---|---|
| `/content` | `/content <yêu cầu>` | Tạo deliverable — tự chọn phòng & chuỗi skill |
| `/use-brand` | `/use-brand <slug>` | Đổi brand đang active |
| `/brand-onboard` | `/brand-onboard <URL>` | Thêm brand mới (sinh L0) |
| `/review` | `/review [kỳ]` | Chạy vòng L5: đo lường → insight → đề xuất cập nhật L0 |

## 5. Cách viết yêu cầu tốt
- **Công thức:** `[deliverable] về [chủ đề] cho [brand]`.
  - *Tốt:* `viết FB post về "5 sai lầm khi chọn vendor" cho acme`
  - *Mơ hồ:* `làm content marketing` (engine sẽ phải hỏi lại).
- **Brand:** nêu tên brand trong câu → engine tự đổi active; không nêu → dùng brand đang active.
- **Chế độ (tùy chọn):** thêm "nhanh/gấp" → chạy gọn; "kỹ/pillar/quan trọng" → chạy đầy đủ.
- **Mẹo:** cứ dùng `/content` làm cổng vào — engine tự route. Nếu cần một skill chưa có, engine sẽ **báo rõ** thay vì làm bừa.

---

## 6. ⭐ Ý tưởng cốt lõi — **3 phòng thực thi × 6 tầng**, điều phối bởi lớp **Leader**

### Hai trục + một lớp trên
- **Chiều rộng = 3 phòng thực thi (ai làm):** Content · Ads · Design.
- **Chiều sâu = 6 tầng (công việc chảy qua giai đoạn nào):** từ sự thật brand → chiến lược → nguyên liệu → thành phẩm → bảo trì → đo lường.
- **Lớp chiến lược — Leader (đứng trên, quản 3 phòng):** không tự sản xuất; đặt hướng → giao việc → đọc kết quả → điều chỉnh.

### Sơ đồ
```
        ┌────────── LEADER · lớp chiến lược ──────────┐
        │ marketing-strategist · campaign-orchestrator│
        │        ▲ insight (L5) ── khép vòng          │
        └──┬──────────────┬──────────────┬────────────┘
   giao việc           │              │
        ▼              ▼              ▼
   ┌─────────┐    ┌─────────┐    ┌─────────┐
   │ CONTENT │    │   ADS   │    │ DESIGN  │
   └─────────┘    └─────────┘    └─────────┘
        └──── deliverables → đo lường (L5) ──┘→ insight quay lên Leader
   (dùng chung: L0 nguồn sự thật · L4 meta/orchestrator)
```

### Bảng ma trận (3 phòng thực thi)

| Tầng | Content | Ads | Design |
|---|---|---|---|
| **L1 — Strategists** | narrative-strategist | — | — |
| **L2 — Specialists** | content-brief · message-architect · demo-scripter | ads-planner | visual-communicator |
| ↳ *Miners (dùng chung)* | angle-miner · device-miner · evidence-miner · frame-packager · benefit-card-generator |||
| **L3 — Producers** | copywriter · sales-enabler · video-script-producer | ads-copywriter | designer-producer |
| **L5 — Tail-loop** | content-analyst | performance-analyst | — |
| *dùng chung* | **L0** nguồn sự thật · **L4** orchestrator · brand-intake · critic-qa · agent-creator · workspace-librarian |||
| **⬆ Leader (lớp chiến lược)** | marketing-strategist · campaign-orchestrator · insight-collector (khép vòng) |||

### Dòng chảy
- **Trong mỗi phòng (chảy xuống):** L0 → L1 → L2 → L3 → *deliverable*.
- **Leader điều phối ngang:** chiến lược → campaign đa kênh → giao việc xuống 3 phòng.
- **Vòng ngược (học):** L5 đo lường → insight → Leader cập nhật chiến lược/L0 → vòng sau thông minh hơn.
- **Dùng chung:** L0, Miners (L2), và L4 phục vụ cả 3 phòng.

### Vì sao thiết kế kiểu này
- **Không pha loãng chất lượng** — mỗi skill làm 1 việc thật sắc.
- **Truy vết được** — hỏng ở đâu sửa đúng đó (mỗi bước để lại file).
- **Tái dùng đa brand** — đổi brand chỉ là đổi L0.

---

## 7. ⭐ Chi tiết 3 phòng thực thi + lớp Leader (kèm ví dụ)

> Mỗi phòng theo khung: **Vai trò · Skill · Output · Khi nào gọi · Ví dụ (lệnh → kết quả).**

### 7.1 Phòng **Content**
- **Vai trò:** sản xuất nội dung chữ & kịch bản.
- **Skill:** narrative-strategist → angle-miner → content-brief / message-architect → copywriter / video-script-producer / sales-enabler → content-analyst.
- **Output:** post · blog · email · kịch bản video · tài liệu bán hàng.
- **Khi nào gọi:** cần một bài cụ thể, hoặc thư viện angle cho cả campaign.
- **Ví dụ:**
  ```
  /content viết LinkedIn post về "tự động hoá onboarding" cho acme
  ```
  → angle-miner (10 góc → chọn 1) → content-brief (hook + dàn ý + proof) → copywriter (bài hoàn chỉnh, đúng giọng) → critic-qa (**Approve**).

### 7.2 Phòng **Ads**
- **Vai trò:** kế hoạch & copy quảng cáo trả phí.
- **Skill:** ads-planner → ads-copywriter → (performance-analyst đọc số liệu).
- **Output:** media plan (targeting · CPA · phân bổ kênh · A/B) · ad copy nhiều variant theo phễu.
- **Khi nào gọi:** chạy ads, cần plan ngân sách/KPI hoặc creative.
- **Ví dụ:**
  ```
  /content lên media plan + ad copy cho campaign dùng thử 14 ngày, ngân sách 50tr, cho acme
  ```
  → ads-planner (CPA mục tiêu suy ngược từ north-star + phân bổ TOFU/MOFU/BOFU) → ads-copywriter (3 variant/phễu, sẵn paste Ads Manager) → critic-qa.

### 7.3 Phòng **Design**
- **Vai trò:** ý tưởng hình & spec sản xuất, đúng nhận diện brand.
- **Skill:** visual-communicator (ý tưởng) → designer-producer (spec/HTML/resize).
- **Output:** concept carousel · spec từng slide theo màu/font brand · HTML landing/email · guide resize.
- **Khi nào gọi:** cần visual đi kèm nội dung, hoặc asset để designer dựng.
- **Ví dụ:**
  ```
  /content làm carousel 5 slide "5 sai lầm khi chọn vendor" cho acme
  ```
  → visual-communicator (10 ý tưởng → 3 concept) → designer-producer (spec từng slide: layout · HEX màu brand · font · text overlay) → critic-qa (check brand).

### 7.4 Lớp chiến lược — **Leader** *(quản 3 phòng, không phải phòng ban)*
- **Vai trò:** đứng trên 3 phòng — đặt chiến lược tổng, lên campaign đa kênh, **giao việc xuống Content/Ads/Design**, và **khép vòng học**.
- **Skill:** marketing-strategist → campaign-orchestrator → (bàn giao 3 phòng) ← insight-collector.
- **Output:** bản chiến lược/GTM · campaign plan + content calendar · insight đề xuất cập nhật L0.
- **Khi nào gọi:** định hướng quý, lên cả chiến dịch, hoặc tổng kết số liệu.
- **Ví dụ:** giao agent `mkt-leader`:
  ```
  lập chiến lược Q3 + campaign ra mắt tính năng mới đa kênh cho acme
  ```
  → marketing-strategist (3 ưu tiên + phân bổ kênh) → campaign-orchestrator (ma trận deliverable × kênh + calendar) → giao Content/Ads/Design.
  Cuối kỳ: `/review tháng 6` → performance-analyst → content-analyst → insight-collector → **đề xuất sửa L0** (chờ duyệt).

---

## 8. Vòng học (L5)
1. Bỏ số liệu thật vào `brands/<brand>/5_data/` (export GA/Facebook/LinkedIn, kết quả campaign…).
2. Chạy `/review`.
3. Engine chấm theo **north-star thật** (không vanity metric), chỉ ra winner/loser, và **đề xuất diff L0** (vd: dồn nội dung dạng A, giảm dạng B).
4. Bạn **duyệt** → L0 cập nhật → các lần `/content` sau tự ưu tiên đúng hướng. Hệ thống *học* thay vì chạy mãi một chỗ.

## 9. Quản nhiều thương hiệu
- Mỗi brand = một **L0 pack** trong `brands/<slug>/0_truth/`. Engine **không** chứa thông tin brand nào (no-brand-leakage) — tất cả nạp từ L0 lúc chạy.
- Đổi brand: `/use-brand <slug>` (hoặc sửa `brands/_active.md`).
- Thêm brand: `/brand-onboard <URL>` — chỉ tốn một buổi là có brand mới chạy được.
- Mỗi brand có **locale** riêng (ngôn ngữ output) khai trong `brand-system.md` → cùng một skill, brand tiếng Anh ra tiếng Anh, brand tiếng Việt ra tiếng Việt.

## 10. Xử lý sự cố (FAQ)
- **`/content` không hiện?** Đóng & mở lại Claude Code; kiểm tra đã `/plugin install sucnx`; hoặc dùng cách B (copy command vào `.claude/commands/`).
- **"Brand chưa có pack"?** Chạy `/brand-onboard <URL>` trước.
- **Muốn output ngôn ngữ khác?** Sửa field `Locale` trong `brand-system.md` của brand.
- **Engine gọi nhầm skill?** Dùng `/content` (orchestrator) làm cổng vào; hoặc nói rõ loại deliverable.
- **Ngành nhạy cảm (y tế/tài chính/pháp lý)?** `brand-intake` tự đặt ranh giới claim chặt; `critic-qa` chặn over-claim.
- **File output ở đâu?** `brands/<brand>/work/<ngày>-<slug>/`.
- **Designer ra sai màu?** Điền mục Visual (HEX + font) trong `brand-system.md`.

---

## Phụ lục — 26 skill theo tầng
- **L1 Strategists (3):** narrative-strategist · marketing-strategist · campaign-orchestrator
- **L2 Miners (5):** angle-miner · device-miner · evidence-miner · frame-packager · benefit-card-generator
- **L2 Transformers (5):** content-brief · message-architect · demo-scripter · visual-communicator · ads-planner
- **L3 Producers (5):** copywriter · sales-enabler · video-script-producer · ads-copywriter · designer-producer
- **L4 Meta (5):** orchestrator · brand-intake · critic-qa · agent-creator · workspace-librarian
- **L5 Tail-loop (3):** performance-analyst · content-analyst · insight-collector

> *Lưu ý mô hình:* **Content · Ads · Design** là 3 phòng thực thi; **Leader** (marketing-strategist · campaign-orchestrator · insight-collector) là **lớp chiến lược** điều phối 3 phòng, không phải phòng ban thứ 4.
