# brands/ — dữ liệu thương hiệu (bạn cung cấp)

Engine sucnx **không kèm brand nào**. Mỗi brand là một bộ **L0 (nguồn sự thật)**:

```
brands/<slug>/
├── 0_truth/   ← 5 file theo _schema/ (brand-system · product-truth · audience-personas · kpi-standards · competitor-intel)
└── 5_data/    ← dữ liệu hiệu suất thật (đầu vào cho L5)
```

## Tạo brand
- `/brand-onboard <URL>` — tự research website + phỏng vấn → sinh L0.
- Hoặc tạo tay theo `_schema/`, rồi `/use-brand <slug>`.

## Lưu ý runtime
- Dùng như **thư mục project**: `brands/` đặt ngay đây.
- Cài như **plugin (read-only)**: đặt `brands/` trong **project của bạn** (thư mục bạn mở Claude Code) để skill ghi được artifact vào `brands/<slug>/work/`.

> Đừng commit dữ liệu brand thật lên repo công khai — xem `.gitignore`.
