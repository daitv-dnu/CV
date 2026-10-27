# Portfolio CV cá nhân – Frontend Developer

Website hồ sơ cá nhân (CV/portfolio) dạng tĩnh, giới thiệu thông tin, kỹ năng,
dự án và cách liên hệ. Giao diện được xây dựng theo hướng responsive, ưu tiên
hiển thị tốt trên điện thoại, máy tính bảng và máy tính để bàn.

## Chức năng

- Giới thiệu cá nhân và định hướng nghề nghiệp.
- Trình bày kỹ năng bằng các thẻ nội dung.
- Hiển thị các dự án mẫu: Landing Page, Todo List, Weather Dashboard và Blog.
- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp thông tin liên hệ và liên kết mạng xã hội mẫu.
- Bố cục responsive, cuộn trang mượt và hỗ trợ điều hướng bằng bàn phím.

## Công nghệ

- HTML5: cấu trúc nội dung và các vùng ngữ nghĩa.
- CSS3: giao diện, Flexbox, CSS Grid, biến CSS và media queries.
- Không sử dụng framework, thư viện JavaScript, cơ sở dữ liệu hoặc bước biên dịch.
- Nginx (tùy chọn): phục vụ trang khi chạy bằng Docker.

## Yêu cầu môi trường

### Chạy trực tiếp

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Không cần cài Node.js hay công cụ build.
- Tùy chọn: Python 3 nếu muốn chạy website qua máy chủ HTTP cục bộ.

### Chạy bằng Docker

- Docker Engine; trên Windows và macOS có thể dùng Docker Desktop.
- Kết nối Internet trong lần chạy đầu để tải image `nginx:alpine`.

## Cài đặt

Tải mã nguồn về máy bằng Git:

```bash
git clone https://github.com/daitv-dnu/CV.git
cd CV
```

Hoặc tải mã nguồn dưới dạng ZIP, giải nén rồi mở thư mục dự án. Không cần cài
thêm thư viện hay chạy lệnh build.

## Cấu hình và tùy chỉnh

Website hiện không yêu cầu file cấu hình, biến môi trường hay khóa API. Để cá
nhân hóa nội dung:

1. Chỉnh sửa tên, phần giới thiệu, kỹ năng, dự án và thông tin liên hệ trong
   `index.html`.
2. Thay ảnh đại diện tại `assets/img/avatar.jpg` (giữ nguyên tên file hoặc cập
   nhật đường dẫn ảnh trong `index.html`).
3. Tùy chỉnh màu sắc, khoảng cách và bố cục trong `assets/css/styles.css`.
4. Cập nhật các địa chỉ liên hệ mẫu trước khi đưa website lên môi trường thật.

Tên và liên hệ trong trang hiện là dữ liệu mẫu, có thể chưa đồng nhất giữa các
vị trí. Hãy rà soát và thay bằng thông tin chính xác của bạn.

## Chạy thử

### Windows

**Cách nhanh:** mở thư mục dự án trong File Explorer rồi nhấp đúp `index.html`.

**Chạy qua máy chủ HTTP (Python 3 tùy chọn):**

```powershell
py -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Dừng máy chủ
bằng `Ctrl+C`.

### macOS

**Cách nhanh:** mở `index.html` bằng trình duyệt.

**Chạy qua máy chủ HTTP (Python 3 tùy chọn):**

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

### Linux

**Cách nhanh:** mở `index.html` bằng trình duyệt.

**Chạy qua máy chủ HTTP (Python 3 tùy chọn):**

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Dừng máy chủ bằng `Ctrl+C`.

### Docker (Windows, macOS và Linux)

Mở PowerShell hoặc Terminal tại thư mục gốc của dự án, sau đó chạy lệnh tương
ứng.

**Windows PowerShell:**

```powershell
docker run --rm --name portfolio-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS / Linux:**

```bash
docker run --rm --name portfolio-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Khi Nginx khởi động, mở [http://localhost:8080](http://localhost:8080). Dừng
container bằng `Ctrl+C`; tùy chọn `--rm` sẽ tự xóa container sau khi dừng.
Trên Windows, nếu Docker không truy cập được thư mục dự án, hãy kiểm tra quyền
chia sẻ ổ đĩa/thư mục trong Docker Desktop.

## Thông tin liên hệ

Thông tin đang hiển thị trong trang chỉ là dữ liệu mẫu:

- Email: `an.nguyen@example.com`
- GitHub: `github.com/nguyenvanan` (liên kết hiện chưa được cấu hình)
- LinkedIn: `linkedin.com/in/nguyenvanan` (liên kết hiện chưa được cấu hình)

Vui lòng thay bằng thông tin thật trong `index.html` trước khi phát hành. Không
có thông tin liên hệ của người bảo trì dự án được khai báo riêng trong mã nguồn.