---
title: "Worklog Tuần 2"
date: 2026-06-29
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Triển khai Storage Layer bằng Amazon S3.
* Xây dựng Image Processing Lambda cơ bản.
* Tìm hiểu và thực hành xử lý ảnh bằng Python.
* Thiết lập IAM Role cho Lambda.
* Xây dựng pipeline xử lý ảnh đầu tiên.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tạo S3 Input Bucket <br> - Tạo S3 Output Bucket <br> - Tìm hiểu object key và folder structure | 29/06/2026 | 29/06/2026 | AWS S3 Documentation |
| 3 | - Tìm hiểu AWS Lambda Python Runtime <br> - Tạo Image Processing Lambda <br> - Xây dựng handler cơ bản | 30/06/2026 | 30/06/2026 | AWS Lambda Documentation |
| 4 | - Cài đặt thư viện xử lý ảnh <br> - Thực hành resize image <br> - Thực hành compress image <br> - Test xử lý ảnh local | 01/07/2026 | 01/07/2026 | Python / Pillow Documentation |
| 5 | - Kết nối Lambda với S3 <br> - Đọc ảnh từ Input Bucket <br> - Ghi ảnh đã xử lý vào Output Bucket | 02/07/2026 | 02/07/2026 | AWS S3 / Lambda Documentation |
| 6 | - Tạo IAM Execution Role cho Lambda <br> - Cấu hình quyền S3 Read/Write <br> - Kiểm tra Lambda execution <br> - Test pipeline end-to-end | 03/07/2026 | 03/07/2026 | AWS IAM Documentation |

### Kết quả đạt được tuần 2:

* Tạo thành công S3 Input Bucket và Output Bucket.
* Xây dựng được Lambda xử lý ảnh bằng Python.
* Thực hiện được:
  * Resize image
  * Compress image
  * Đọc ảnh từ S3
  * Ghi ảnh output vào S3
* Thiết lập IAM Execution Role cho Lambda.
* Hoàn thành pipeline đầu tiên:

```text
S3 Input
    ↓
Lambda
    ↓
S3 Output