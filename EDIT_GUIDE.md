# 📝 Hướng dẫn chỉnh sửa thông tin trang web

> File này giúp bạn biết chính xác **cần sửa gì** trong `index.html` để cập nhật thông tin cá nhân.
> Mỗi phần đều ghi rõ **dòng tìm** và **cách thay thế**.

---

## 🔧 CÁC PHẦN CÓ THỂ CHỈNH SỬA

### 1. Tên thương hiệu (hiển thị ở Header & Footer)

**Tìm dòng này trong Header (navigation):**
```html
NEON_SNDCT
```
**Thay bằng tên của bạn**, ví dụ: `MINH_CREATOR`

**Cũng sửa trong Footer:**
```html
NEON_SNDCT
```

---

### 2. Ảnh đại diện (Avatar)

**Tìm dòng:**
```html
src="https://lh3.googleusercontent.com/..."
```
**Thay bằng link ảnh của bạn** (Google Drive, imgur, hoặc bất kỳ host nào).

**Cũng sửa alt text:**
```html
alt="Minh Creator - Cyberpunk android portrait..."
```
Thay mô tả ảnh cho đúng với ảnh thật.

**Cũng sửa trong `<meta property="og:image">` và `<meta name="twitter:image">`** (để ảnh hiển thị khi share lên mạng xã hội).

---

### 3. Tên hiển thị

**Tìm dòng:**
```html
<h1 ...>Minh Creator</h1>
```
**Thay bằng tên của bạn.**

---

### 4. Trạng thái (Badge)

**Tìm dòng:**
```html
<div ...>SYSTEM_ONLINE</div>
```
**Thay bằng dòng trạng thái mong muốn**, ví dụ: `OPEN_FOR_WORK`, `ACTIVE`, `AVAILABLE`...

---

### 5. Tagline (Dòng dưới badge)

**Tìm dòng:**
```html
<h2 ...>NEURAL_CONTENT_ARCHITECT</h2>
```
**Thay bằng tagline của bạn**, ví dụ: `CONTENT_CREATOR`, `DIGITAL_ARTIST`, `GAMER`...

---

### 6. Quote / Câu nói

**Tìm dòng:**
```html
<p ...>"Interfacing with the digital void to bring you stories from the frontier of code and creativity."</p>
```
**Thay bằng câu nói của bạn.**

---

### 7. Giới thiệu bản thân (About Me)

**Tìm dòng:**
```html
<p ...>Xin chào! Mình là <span class="text-primary font-semibold">Minh</span> — một mắt xích-link giữa trang cá nhân và các nền tảng mạng xã hội thương mại trên không gian mạng thực tế ảo. Tự tạo nội dung theo phong cách cyberpunk — nói tiếng giữa công nghệ và sáng tạo.</p>
```
**Thay toàn bộ nội dung paragraph** bằng giới thiệu của bạn. Lưu ý: giữ nguyên tag `<span class="text-primary font-semibold">Tên</span>` nếu muốn tên được highlight màu hồng.

---

### 8. Thống kê (Stats)

**Tìm dòng có 3 ô thống kê:**
```html
<div ...>11+</div>          ← Thay số lượng nền tảng
<div ...>NỀN TẢNG</div>    ← Thay nhãn

<div ...>24/7</div>         ← Thay trạng thái online
<div ...>ONLINE</div>       ← Thay nhãn

<div ...>01</div>           ← Thay số lượng
<div ...>MẠNG XÃ HỘI</div> ← Thay nhãn
```

---

### 9. Link mạng xã hội (Quan trọng nhất!)

**Tìm đoạn JavaScript `platformLinks`:**

```javascript
const platformLinks = {
    youtube: [
        { label: "Kênh YouTube chính", url: "https://youtube.com/@minhcreator" }
    ],
    tiktok: [
        { label: "TikTok", url: "https://tiktok.com/@minhcreator" }
    ],
    // ... các platform khác
};
```

**Cách chỉnh sửa:**

#### Nếu chỉ có 1 link:
```javascript
youtube: [
    { label: "Kênh YouTube chính", url: "https://youtube.com/@ten-cua-ban" }
],
```

#### Nếu có nhiều link (hiển thị modal khi bấm):
```javascript
youtube: [
    { label: "Kênh YouTube chính", url: "https://youtube.com/@kênh1" },
    { label: "Kênh YouTube phụ", url: "https://youtube.com/@kênh2" },
    { label: "YouTube Shorts", url: "https://youtube.com/@shorts" }
],
```

**Cũng sửa username hiển thị trên card:**
Tìm dòng có `@minhcreator` trong mỗi card và thay bằng username thật.

---

### 10. Email liên hệ

**Tìm dòng:**
```html
<a href="mailto:your@email.com"
```
**Thay `your@email.com`** bằng email thật của bạn.

---

### 11. JSON-LD (SEO Structured Data)

**Tìm đoạn:**
```json
{
    "@context": "https://schema.org",
    "@type": "Person",
    "name": "Minh Creator",
    "alternateName": "NEON_SNDCT",
    "description": "Cyberpunk content creator...",
    "url": "https://tienlh1998-jpg.github.io/minh-creator-profile/",
    "jobTitle": "Content Creator",
    "sameAs": [
        "https://www.youtube.com/@minhcreator",
        "https://www.tiktok.com/@minhcreator",
        ...
    ]
}
```
**Sửa:**
- `name`: Tên hiển thị
- `alternateName`: Tên phụ / thương hiệu
- `description`: Mô tả ngắn
- `url`: Link trang web hiện tại
- `jobTitle`: Chức danh
- `sameAs`: Link các mạng xã hội thật

---

### 12. Meta Tags (SEO)

**Tìm các dòng sau và sửa:**
```html
<title>Minh Creator - Cyberpunk Content Creator</title>
<meta name="description" content="..." />
<meta property="og:title" content="..." />
<meta property="og:description" content="..." />
<meta property="og:url" content="..." />
```

---

## ⚡ MẸO NHANH

1. **Dùng Ctrl+F** (hoặc Cmd+F trên Mac) trong editor để tìm nhanh nội dung cần sửa
2. **Khi sửa link**: Luôn bắt đầu bằng `https://`
3. **Khi thêm nhiều link**: Mỗi link trên 1 dòng, bắt đầu bằng `{ label: "...", url: "..." },`
4. **Sau khi sửa xong**: Lưu file → mở lại trên trình duyệt để xem kết quả
5. **Để push lên GitHub**: Chạy lệnh `git add . && git commit -m "Update info" && git push`

---

## 🎨 MÀU SẮC (Nâng cao)

Nếu muốn thay đổi màu sắc, tìm trong `<script>` phần `tailwind.config`:

| Màu | Ý nghĩa | HEX hiện tại |
|------|---------|-------------|
| `primary` | Màu hồng (tên, badge, CTA) | `#ffb1c4` |
| `secondary` | Màu cyan (viền, avatar glow) | `#00dce6` |
| `tertiary` | Màu xanh lá (stats, dot) | `#00e639` |
| `background` | Màu nền | `#131313` |

**Thay HEX code** để đổi màu: https://colorpicker.me

---

*Lưu ý: File này chỉ để tham khảo, không cần upload lên website.*
