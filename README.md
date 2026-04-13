# penwin.vn

Website portfolio cá nhân — hosted trên GitHub Pages.

## Cấu trúc

```
.
├── index.html   # Trang chính (single-page)
├── CNAME        # Tên miền tuỳ chỉnh
└── README.md
```

## Hướng dẫn deploy lên GitHub Pages

### Bước 1 — Tạo repository
1. Đăng nhập GitHub → **New repository**
2. Đặt tên: `penwin.vn` (hoặc `<username>.github.io` để dùng domain mặc định)
3. Chọn **Public** → **Create repository**

### Bước 2 — Push code lên GitHub
```bash
git init
git add .
git commit -m "init: penwin.vn portfolio"
git branch -M main
git remote add origin https://github.com/<username>/penwin.vn.git
git push -u origin main
```

### Bước 3 — Bật GitHub Pages
1. Vào **Settings** → **Pages**
2. Source: **Deploy from a branch** → branch `main` → folder `/ (root)`
3. Nhấn **Save**

GitHub sẽ tự build và deploy (khoảng 1–2 phút).

### Bước 4 — Trỏ domain penwin.vn về GitHub Pages
Vào trang quản lý DNS của nhà cung cấp domain và thêm các bản ghi sau:

| Type  | Host | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | `<username>.github.io` |

Sau khi DNS propagate (có thể mất 30 phút – 24 giờ), vào **Settings → Pages → Custom domain**, nhập `penwin.vn` và bật **Enforce HTTPS**.

## Tuỳ chỉnh nội dung

Mở `index.html` và chỉnh sửa các phần:
- **Tên / bio** — Hero section và About section
- **Kỹ năng** — Mục `#skills` → các `.skill-card`
- **Dự án** — Mục `#projects` → các `.project-card` (tên, mô tả, link)
- **Liên hệ** — Email và các social link trong `#contact`
- **Thống kê** — Hero stats (số năm kinh nghiệm, số dự án…)
