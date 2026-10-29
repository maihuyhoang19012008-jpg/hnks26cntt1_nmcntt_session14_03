


## Phần 1: Luồng Dữ liệu Từ Lưu => Đồng bộ 

###  Nếu không loại trừ `node_modules`

plaintext

```
Nhấn Ctrl+S => Phát hiện thay đổi => Quét toàn bộ thư mục
=> Đếm hàng vạn tệp trong node_modules => Tải lên tất cả
=> Máy chậm, Cloud đầy, tích xanh rất chậm 

```

###  Đã loại trừ đúng

plaintext

```
Nhấn Ctrl+S => Lưu ngay => Bộ lọc bỏ qua node_modules
=> Chỉ quét mã của bạn => Tải lên vài tệp nhỏ
=> Tích xanh hiện ngay 

```

>  `node_modules` chỉ là thư viện người khác viết  chỉ cần có `package.json` thì chạy `npm install` là có lại ngay => **Không cần lưu lên Cloud**

----------

## Phần 2: Cách Bỏ `node_modules` Khỏi Đồng bộ

Tạo tệp tên **`.gitignore`** trong thư mục gốc dự án, viết 1 dòng:

plaintext

```
node_modules/

```

Ngoài ra trong cài đặt Cloud (Google Drive / OneDrive / Dropbox):

-   Thêm `node_modules/` vào danh sách **loại trừ / bỏ qua**
-   Bật **Files On-Demand** → tệp không chiếm dung lượng ổ cứng cho đến khi mở dùng

----------

## Phần 3: Cấu trúc Thư mục Cloud Chuẩn

plaintext

```
 Cloud/
  Code/        Mã nguồn, dự án của bạn  đồng bộ
  src/
     package.json
     node_modules/   Bỏ qua, không tải lên
     Docs/      Tài liệu, hướng dẫn đồng bộ

   Assets/       Hình ảnh, slide, font đồng bộ
   Archive/      Dự án cũ  lưu trữ

```

### Nguyên tắc dễ nhớ



Thư mục

Tải lên Cloud?

Lý do

Mã nguồn của bạn

 Có

Viết tay, không khôi phục lại nếu mất

`package.json`

Có

Chứa danh sách thư viện  `npm install` tự cài lại

`node_modules`


Tự tạo lại được, nặng hàng GB, không cần lưu

Tài liệu, ảnh, slide

CÓ 

Công việc của nhóm
