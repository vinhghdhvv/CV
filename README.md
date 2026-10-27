# PORTFOLIO CÁ NHÂN – KIỀU DUY VINH

## 1. Giới thiệu dự án

Đây là dự án website Portfolio cá nhân của **Kiều Duy Vinh**, được xây dựng nhằm giới thiệu bản thân, kỹ năng, các dự án đã thực hiện và thông tin liên hệ.

Website được thiết kế với giao diện hiện đại, dễ sử dụng, hỗ trợ hiển thị trên nhiều kích thước màn hình.

**Thông tin dự án:**

- **Tên dự án:** Personal Portfolio Website
- **Tác giả:** Kiều Duy Vinh
- **Trường:** Đại học Đại Nam
- **Ngành học:** Công nghệ thông tin
- **Mã sinh viên:** 1771020756
- **Tên thư mục:** KT A2.1
- **Ngôn ngữ:** HTML5, CSS3
- **Công cụ phát triển:** Visual Studio Code

## 2. Chức năng chính

Website Portfolio bao gồm các chức năng:

- Giới thiệu thông tin cá nhân.
- Hiển thị kỹ năng và kiến thức chuyên môn.
- Giới thiệu các dự án và sản phẩm đã thực hiện.
- Hiển thị hình ảnh minh họa.
- Cung cấp thông tin liên hệ.
- Hỗ trợ giao diện trên máy tính và điện thoại.

## 3. Công nghệ sử dụng

| Công nghệ | Mục đích |
|---|---|
| HTML5 | Xây dựng cấu trúc website |
| CSS3 | Thiết kế giao diện và bố cục |
| Visual Studio Code | Viết và chỉnh sửa mã nguồn |
| Git & GitHub | Quản lý và lưu trữ mã nguồn |
| Python HTTP Server | Chạy thử website trên máy tính |
| Docker & Nginx | Tùy chọn triển khai website tĩnh |

## 4. Cấu trúc thư mục

```text
KT A2.1/
│
├── index.html
├── README.md
├── BAOCAO-A2.1.docx
│
└── assets/
    ├── css/
    │   └── styles.css
    │
    └── img/
        ├── kdvinh.jpg
        ├── chuviet.jpg
        ├── vietnam.jpg
        ├── lophoc.jpg
        ├── thoitiet.jpg
        └── Nấm.jpg
```

**Giải thích:**

- `index.html`: File giao diện chính của website.
- `styles.css`: File định dạng giao diện.
- `assets/img/`: Thư mục chứa hình ảnh.
- `README.md`: File giới thiệu và hướng dẫn sử dụng dự án.
- `BAOCAO-A2.1.docx`: Báo cáo bài tập.

## 5. Hướng dẫn cài đặt và chạy website

### 5.1. Yêu cầu

- Máy tính Windows, macOS hoặc Linux.
- Trình duyệt Google Chrome, Microsoft Edge hoặc Firefox.
- Visual Studio Code (khuyến nghị).
- Python (nếu muốn chạy máy chủ HTTP).

### 5.2. Chạy website trên Windows

**Cách 1: Mở trực tiếp**

1. Mở thư mục `KT A2.1`.
2. Tìm file `index.html`.
3. Nhấp đúp vào file.
4. Website sẽ hiển thị trên trình duyệt.

**Cách 2: Chạy bằng Python HTTP Server**

Mở Terminal trong VS Code tại thư mục `KT A2.1`.

Nhập lệnh:

```powershell
py -m http.server 8000 --bind 127.0.0.1
```

Nếu không sử dụng được lệnh `py`, thử:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Sau đó mở trình duyệt và truy cập:

[http://127.0.0.1:8000/](http://127.0.0.1:8000/)

Để dừng máy chủ, nhấn `Ctrl + C` trong Terminal.

### 5.3. Chạy website trên macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Truy cập:

[http://localhost:8000](http://localhost:8000)

Nhấn `Control + C` để dừng.

### 5.4. Chạy website trên Linux

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Truy cập:

[http://localhost:8000](http://localhost:8000)

Nhấn `Ctrl + C` để dừng.

## 6. Chạy website bằng Docker

Có thể sử dụng Docker và Nginx để chạy website tĩnh mà không cần cài đặt máy chủ web riêng.

**Yêu cầu:** Docker đã được cài đặt và đang hoạt động.

Mở Terminal tại thư mục `KT A2.1`.

**Windows (PowerShell):**

```powershell
docker run --rm -d -p 8080:80 --name portfolio-site --mount "type=bind,source=$((Get-Location).Path),target=/usr/share/nginx/html,readonly" nginx:alpine
```

**macOS và Linux:**

```bash
docker run --rm -d -p 8080:80 --name portfolio-site --mount "type=bind,source=$(pwd),target=/usr/share/nginx/html,readonly" nginx:alpine
```

Sau khi khởi động, truy cập:

[http://localhost:8080](http://localhost:8080)

Kiểm tra container:

```bash
docker ps
```

Dừng container:

```bash
docker stop portfolio-site
```

## 7. Hướng dẫn chỉnh sửa website

**Thay đổi nội dung:**

Mở file:

```text
index.html
```

Chỉnh sửa các thông tin cá nhân, kỹ năng, dự án và nội dung hiển thị.

**Thay đổi giao diện:**

Mở file:

```text
assets/css/styles.css
```

Chỉnh sửa màu sắc, font chữ, bố cục và hiệu ứng.

**Thay đổi hình ảnh:**

Thêm hình ảnh vào thư mục:

```text
assets/img/
```

Sau đó cập nhật đường dẫn hình ảnh tương ứng trong `index.html`.

## 8. Kiểm tra website

Sau khi chạy website, cần kiểm tra:

- [ ] Trang chủ hiển thị đầy đủ nội dung.
- [ ] Hình ảnh được tải thành công.
- [ ] CSS hoạt động bình thường.
- [ ] Các nút điều hướng hoạt động chính xác.
- [ ] Giao diện hiển thị phù hợp trên điện thoại và máy tính.
- [ ] Các liên kết liên hệ dẫn đến đúng địa chỉ.

## 9. Thông tin tác giả và liên hệ

**Kiều Duy Vinh**

- **Sinh viên:** Trường Đại học Đại Nam
- **Ngành:** Công nghệ thông tin
- **Mã sinh viên:** 1771020756
- **Email:** [vinhquang123423@gmail.com](mailto:vinhquang123423@gmail.com)
- **GitHub:** [github.com/vinhghdhvv](https://github.com/vinhghdhvv)
- **LinkedIn:** [linkedin.com/in/kieuduyvinh](https://www.linkedin.com/in/kieuduyvinh/)

## 10. Bản quyền

© 2026 Kiều Duy Vinh.

Dự án được xây dựng phục vụ mục đích học tập, thực hành thiết kế website và giới thiệu Portfolio cá nhân.

Nội dung và hình ảnh thuộc quyền sở hữu của tác giả hoặc chủ sở hữu tương ứng. Vui lòng liên hệ trước khi sử dụng lại các tài nguyên không được cấp phép.

---

**Personal Portfolio | Kiều Duy Vinh | Đại học Đại Nam | 2026**