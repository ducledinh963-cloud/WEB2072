# WEB2072 - Lập trình Front-End Framework (Vue.js)

## LAB 4: QUẢN LÝ SÁCH THƯ VIỆN

- **Họ và tên**: Lê Đình Đức
- **Mã sinh viên**: PA00493
- **Lớp / Môn học**: WEB2072 - Front-End Framework

---

### Nội dung thực hiện:

#### PHẦN I:
- **Bài 1 (3 điểm)**: Xây dựng chức năng thêm sách nhập từ form
  - Form nhập: Tiêu đề, Tác giả, Thể loại (dropdown danh mục).
  - Sử dụng `ref()` cho các trường dữ liệu.
  - Xử lý thêm sách mới vào danh sách khi bấm nút **"Thêm sách"**.
  - Hiển thị thông tin sách vừa thêm vào danh sách.

- **Bài 2 (2 điểm)**: Thêm sách mới vào danh sách khi ấn phím Enter
  - Bổ sung ô nhập **Số lượng** (`quantity`).
  - Lắng nghe sự kiện `@keyup.enter.prevent="addBook"`: Khi người dùng nhấn phím **Enter** tại ô số lượng thì sách sẽ tự động được thêm vào danh sách.

#### PHẦN II:
- **Bài 3 (2 điểm)**: Xóa thông tin sách
  - Thêm nút **"Xóa"** màu đỏ cho từng sách trong danh sách.
  - Hiển thị hộp thoại xác nhận `confirm()` trước khi thực hiện xóa.

- **Bài 4 (3 điểm)**: Cập nhật thông tin sách
  - Thêm nút **"Sửa"** màu vàng cho mỗi sách trong danh sách.
  - Khi nhấn **"Sửa"**: Form chuyển sang tiêu đề **"Cập nhật sách"**, đổ dữ liệu sách vào form, hiển thị 2 nút **"Cập nhật sách"** và **"Hủy"**.
  - Khi nhấn **"Cập nhật sách"** (hoặc nhấn Enter): Cập nhật thông tin sách trong danh sách.
  - Khi nhấn **"Hủy"**: Xóa form và quay về chế độ thêm mới.

---

### Hướng dẫn cài đặt và chạy:

1. Cài đặt các thư viện phụ thuộc:
   ```bash
   npm install
   ```

2. Chạy môi trường phát triển:
   ```bash
   npm run dev
   # hoặc:
   npm.cmd run dev
   ```

3. Mở trình duyệt truy cập:
   ```
   http://localhost:5173/
   ```
