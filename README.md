# 📝 Hướng Dẫn Markdown Toàn Tập

> Tài liệu được biên soạn bởi [Lê Hoàng Quý](https://github.com/HoangQuyCoder) — Software Engineer tại Việt Nam.  
> Portfolio: [hoangquy-dev.vercel.app](https://hoangquy-dev.vercel.app) | LinkedIn: [Lê Hoàng Quý](https://www.linkedin.com/in/le-hoang-quy-762ba3389)

---

## Mục Lục

- [I. Markdown là gì?](#i-markdown-là-gì)
- [II. Công Cụ Soạn Thảo](#ii-công-cụ-soạn-thảo)
- [III. Cú Pháp Cơ Bản](#iii-cú-pháp-cơ-bản)
  - [1. Tiêu đề](#1-tiêu-đề)
  - [2. Đoạn văn](#2-đoạn-văn)
  - [3. Định dạng chữ](#3-định-dạng-chữ)
  - [4. Code](#4-code)
- [IV. Các Khối Nội Dung](#iv-các-khối-nội-dung)
  - [1. Trích dẫn](#1-trích-dẫn)
  - [2. Danh sách](#2-danh-sách)
  - [3. Bảng](#3-bảng)
  - [4. Đường kẻ ngang](#4-đường-kẻ-ngang)
- [V. Liên Kết & Đa Phương Tiện](#v-liên-kết--đa-phương-tiện)
  - [1. Liên kết](#1-liên-kết)
  - [2. Hình ảnh](#2-hình-ảnh)
- [VI. Tính Năng Nâng Cao](#vi-tính-năng-nâng-cao)
  - [1. Checkbox](#1-checkbox)
  - [2. Emoji](#2-emoji)
  - [3. Escape ký tự](#3-escape-ký-tự)
- [VII. Ứng Dụng Thực Tế](#vii-ứng-dụng-thực-tế)
- [VIII. Kết Luận](#viii-kết-luận)

---

## I. Markdown là gì?

**Markdown** là ngôn ngữ đánh dấu văn bản nhẹ, cho phép định dạng nội dung bằng cú pháp đơn giản và trực quan — không cần viết HTML thuần.

### Tại sao dùng Markdown?

| Tiêu chí               | HTML | Markdown |
| :--------------------- | :--- | :------- |
| Độ phức tạp            | Cao  | Thấp     |
| Tốc độ viết            | Chậm | Nhanh    |
| Dễ đọc khi chưa render | Khó  | Dễ       |
| Phù hợp với GitHub     | ✅   | ✅       |

### Markdown được dùng ở đâu?

- **GitHub / GitLab** — README, wiki, issue, pull request
- **Discord** — Định dạng tin nhắn
- **Notion, Obsidian** — Ghi chú
- **Dev.to, Hashnode** — Viết blog kỹ thuật

---

## II. Công Cụ Soạn Thảo

### Desktop

| Tên                                       | Nền tảng          | Ghi chú                            |
| :---------------------------------------- | :---------------- | :--------------------------------- |
| [VS Code](https://code.visualstudio.com/) | Win / Mac / Linux | Khuyên dùng — preview tích hợp sẵn |
| [Typora](https://typora.io/)              | Win / Mac / Linux | WYSIWYG, render ngay khi gõ        |
| Notepad++                                 | Windows           | Nhẹ, không cần preview             |

### Online (không cần cài đặt)

| Tên       | Link                                  |
| :-------- | :------------------------------------ |
| StackEdit | [stackedit.io](https://stackedit.io/) |
| Dillinger | [dillinger.io](https://dillinger.io/) |
| Hashify   | [hashify.me](https://hashify.me/)     |

> 🔧 **Khuyến nghị cá nhân:** Tôi dùng **VS Code** cho tất cả dự án. Cài thêm extension [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) để có preview đẹp hơn mặc định.

---

## III. Cú Pháp Cơ Bản

### 1. Tiêu đề

Dùng dấu `#` để tạo tiêu đề từ cấp 1 đến cấp 6:

```markdown
# Tiêu đề cấp 1 (H1)

## Tiêu đề cấp 2 (H2)

### Tiêu đề cấp 3 (H3)

#### Tiêu đề cấp 4 (H4)

##### Tiêu đề cấp 5 (H5)

###### Tiêu đề cấp 6 (H6)
```

> ⚠️ Lưu ý: Cần có **dấu cách** sau dấu `#` để được nhận diện đúng.

---

### 2. Đoạn văn

Dùng **một dòng trống** để tách các đoạn văn:

```markdown
Đây là đoạn văn thứ nhất.

Đây là đoạn văn thứ hai.
```

Để **xuống dòng trong cùng một đoạn**, thêm hai dấu cách ở cuối dòng trước khi nhấn Enter:

```markdown
Dòng 1  
Dòng 2 (cùng đoạn)
```

---

### 3. Định dạng chữ

| Định dạng     | Cú pháp                  | Kết quả               |
| :------------ | :----------------------- | :-------------------- |
| In nghiêng    | `*chữ*` hoặc `_chữ_`     | _chữ nghiêng_         |
| In đậm        | `**chữ**` hoặc `__chữ__` | **chữ đậm**           |
| Đậm + nghiêng | `***chữ***`              | **_chữ đậm nghiêng_** |
| Gạch giữa     | `~~chữ~~`                | ~~chữ gạch~~          |

---

### 4. Code

#### Inline code — dùng cho tên biến, lệnh ngắn:

```markdown
Chạy lệnh `npm install` để cài dependencies.
```

Kết quả: Chạy lệnh `npm install` để cài dependencies.

#### Block code — dùng cho đoạn mã dài, có syntax highlighting:

````markdown
```java
@RestController
@RequestMapping("/api/hotels")
public class HotelController {
    @GetMapping
    public List<Hotel> getAll() {
        return hotelService.findAll();
    }
}
```
````

Kết quả:

```java
@RestController
@RequestMapping("/api/hotels")
public class HotelController {
    @GetMapping
    public List<Hotel> getAll() {
        return hotelService.findAll();
    }
}
```

**Các ngôn ngữ hỗ trợ syntax highlighting phổ biến:**

```
java, javascript, typescript, python, bash, sql,
json, yaml, dockerfile, kotlin, php, c, cpp, go
```

---

## IV. Các Khối Nội Dung

### 1. Trích dẫn

Dùng `>` để tạo blockquote. Có thể lồng nhiều cấp:

```markdown
> Đây là trích dẫn cấp 1.
>
> > Đây là trích dẫn cấp 2 (lồng nhau).
```

> Đây là trích dẫn cấp 1.
>
> > Đây là trích dẫn cấp 2 (lồng nhau).

---

### 2. Danh sách

#### Danh sách có thứ tự:

```markdown
1. Clone repository
2. Cài dependencies: `npm install`
3. Cấu hình file `.env`
4. Chạy server: `npm run dev`
```

1. Clone repository
2. Cài dependencies: `npm install`
3. Cấu hình file `.env`
4. Chạy server: `npm run dev`

#### Danh sách không thứ tự (có thể lồng nhau):

```markdown
- Backend
  - Java / Spring Boot
  - Node.js / Express.js
- Frontend
  - React.js
  - Tailwind CSS
- DevOps
  - Docker
  - Kubernetes
  - GitHub Actions
```

- Backend
  - Java / Spring Boot
  - Node.js / Express.js
- Frontend
  - React.js
  - Tailwind CSS
- DevOps
  - Docker
  - Kubernetes
  - GitHub Actions

---

### 3. Bảng

```markdown
| Tên dự án            | Tech Stack                     |     Trạng thái     |
| :------------------- | :----------------------------- | :----------------: |
| Hotel Booking System | Spring Boot, React, PostgreSQL |   ✅ Hoàn thành    |
| WebBlog              | Node.js, MongoDB, Ollama       | 🔄 Đang phát triển |
| Library Server       | Node.js, Express, Docker       |   ✅ Hoàn thành    |
```

| Tên dự án            | Tech Stack                     |     Trạng thái     |
| :------------------- | :----------------------------- | :----------------: |
| Hotel Booking System | Spring Boot, React, PostgreSQL |   ✅ Hoàn thành    |
| WebBlog              | Node.js, MongoDB, Ollama       | 🔄 Đang phát triển |
| Library Server       | Node.js, Express, Docker       |   ✅ Hoàn thành    |

**Căn chỉnh cột:**

| Ký hiệu | Ý nghĩa             |
| :------ | :------------------ |
| `:---`  | Căn trái (mặc định) |
| `---:`  | Căn phải            |
| `:---:` | Căn giữa            |

---

### 4. Đường kẻ ngang

Dùng `---`, `***`, hoặc `___` trên một dòng riêng:

```markdown
---
```

---

## V. Liên Kết & Đa Phương Tiện

### 1. Liên kết

```markdown
<!-- Liên kết thông thường -->

[Tên hiển thị](https://url.com)

<!-- Liên kết có tooltip -->

[Tên hiển thị](https://url.com "Tooltip khi hover")

<!-- Liên kết đến section trong file -->

[Xem phần III](#iii-cú-pháp-cơ-bản)

<!-- Liên kết tự động -->

https://hoangquy-dev.vercel.app
```

**Ví dụ thực tế:**

```markdown
Xem thêm tại [portfolio của tôi](https://hoangquy-dev.vercel.app) hoặc liên hệ qua
[LinkedIn](https://www.linkedin.com/in/le-hoang-quy-762ba3389).
```

---

### 2. Hình ảnh

```markdown
<!-- Ảnh cơ bản -->

![Alt text](https://link-anh.com/image.png)

<!-- Ảnh có tooltip -->

![Alt text](https://link-anh.com/image.png "Tooltip")

<!-- Ảnh có thể click (liên kết) -->

[![Alt text](https://link-anh.com/image.png)](https://link-redirect.com)
```

**Ví dụ badge thường dùng trong GitHub README:**

```markdown
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
```

---

## VI. Tính Năng Nâng Cao

### 1. Checkbox

Thường dùng trong **To-do list** hoặc **task tracking** trên GitHub Issues/PR:

```markdown
## Checklist trước khi merge PR

- [x] Viết unit tests
- [x] Cập nhật API documentation
- [ ] Review code với team
- [ ] Deploy lên staging
- [ ] Thông báo cho QA team
```

Kết quả:

- [x] Viết unit tests
- [x] Cập nhật API documentation
- [ ] Review code với team
- [ ] Deploy lên staging
- [ ] Thông báo cho QA team

---

### 2. Emoji

GitHub hỗ trợ emoji bằng cú pháp `:tên_emoji:`:

```markdown
:rocket: :tada: :bug: :fire: :white_check_mark: :warning:
```

🚀 🎉 🐛 🔥 ✅ ⚠️

**Một số emoji hay dùng trong README dự án:**

| Emoji | Code                 | Ý nghĩa         |
| :---: | :------------------- | :-------------- |
|  🚀   | `:rocket:`           | Deploy / Launch |
|  ✅   | `:white_check_mark:` | Hoàn thành      |
|  🐛   | `:bug:`              | Bug fix         |
|  📚   | `:books:`            | Tài liệu        |
|  ⚠️   | `:warning:`          | Cảnh báo        |
|  🔧   | `:wrench:`           | Cấu hình        |

> 🔍 Danh sách đầy đủ: [github.com/ikatyang/emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet)

---

### 3. Escape ký tự

Khi cần hiển thị ký tự Markdown như ký tự thường, thêm dấu `\` trước:

```markdown
\*Dòng này không in nghiêng\*

\`Không phải inline code\`

\# Không phải tiêu đề
```

**Các ký tự cần escape:**

```
\ ` * _ { } [ ] ( ) # + - . !
```

---

## VII. Ứng Dụng Thực Tế

### Mẫu README cho dự án cá nhân

Dưới đây là cấu trúc README mà tôi thường dùng cho các dự án:

````markdown
# Tên Dự Án

> Mô tả ngắn gọn về dự án.

![Badge](...) ![Badge](...)

## ✨ Tính năng

- Tính năng 1
- Tính năng 2

## 🛠️ Tech Stack

- **Backend:** Spring Boot, PostgreSQL
- **Frontend:** React.js, Tailwind CSS
- **DevOps:** Docker, GitHub Actions

## 🚀 Hướng dẫn cài đặt

1. Clone repository
   ```bash
   git clone https://github.com/HoangQuyCoder/ten-du-an.git
   ```
````

2. Cấu hình biến môi trường
   ```bash
   cp .env.example .env
   ```
3. Chạy với Docker
   ```bash
   docker-compose up -d
   ```

## 📄 API Documentation

Xem tại: `http://localhost:8080/swagger-ui.html`

## 🤝 Contributing

Pull request luôn được chào đón. Vui lòng đọc [CONTRIBUTING.md](./CONTRIBUTING.md) trước.

## 📬 Liên hệ

- Email: hoangquyle11@gmail.com
- LinkedIn: [Lê Hoàng Quý](https://www.linkedin.com/in/le-hoang-quy-762ba3389)

````

---

## VIII. Kết Luận

Markdown đơn giản nhưng cực kỳ hiệu quả — đặc biệt trong môi trường làm việc với GitHub và các công cụ developer hiện đại.

**Tóm tắt nhanh những gì đã học:**

| Nhóm | Cú pháp chính |
| :--- | :--- |
| Tiêu đề | `#`, `##`, `###` |
| Định dạng chữ | `**bold**`, `*italic*`, `~~strike~~` |
| Code | `` `inline` ``, ` ```block``` ` |
| Danh sách | `1.`, `-`, `*` |
| Liên kết & ảnh | `[text](url)`, `![alt](url)` |
| Bảng | `\| col \| col \|` |
| Checkbox | `- [ ]`, `- [x]` |
| Blockquote | `>` |

---

> 💬 **Góp ý hoặc đóng góp?** Hãy tạo [Issue](https://github.com/HoangQuyCoder) hoặc liên hệ trực tiếp với tôi.
> Nếu thấy hữu ích, hãy ⭐ star repository này nhé!

*Made with ❤️ by [Lê Hoàng Quý](https://github.com/HoangQuyCoder)*
````
