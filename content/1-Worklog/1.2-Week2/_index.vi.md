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
| 2 | - Tạo S3 Input Bucket <br> - Tạo S3 Output Bucket <br> - Tìm hiểu Object Key và Folder Structure | 29/06/2026 | 29/06/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html |
| 3 | - Tìm hiểu AWS Lambda Python Runtime <br> - Xây dựng Image Processing Lambda <br> - Tạo Lambda Handler cơ bản | 30/06/2026 | 30/06/2026 | https://docs.aws.amazon.com/lambda/latest/dg/welcome.html |
| 4 | - Cài đặt thư viện Pillow <br> - Thực hành Resize Image <br> - Thực hành Compress Image <br> - Kiểm thử xử lý ảnh trên môi trường Local | 01/07/2026 | 01/07/2026 | https://pillow.readthedocs.io/en/stable/ |
| 5 | - Kết nối Lambda với Amazon S3 <br> - Đọc ảnh từ Input Bucket <br> - Lưu ảnh sau xử lý vào Output Bucket | 02/07/2026 | 02/07/2026 | https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html |
| 6 | - Tạo IAM Execution Role cho Lambda <br> - Cấu hình quyền truy cập Amazon S3 <br> - Kiểm tra CloudWatch Logs <br> - Kiểm thử pipeline xử lý ảnh | 03/07/2026 | 03/07/2026 | https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html |

### Kết quả đạt được tuần 2:

* Hoàn thành triển khai **Storage Layer** của hệ thống bằng Amazon S3, bao gồm:
  * Tạo **Input Bucket** để lưu trữ ảnh gốc.
  * Tạo **Output Bucket** để lưu trữ ảnh sau khi xử lý.
  * Chuẩn hóa cấu trúc lưu trữ và quy tắc đặt tên đối tượng (Object Key).

* Xây dựng phiên bản đầu tiên của **Image Processing Lambda** bằng Python với khả năng:
  * Tiếp nhận sự kiện từ Amazon S3.
  * Đọc ảnh từ Input Bucket.
  * Thực hiện các thao tác Resize và Compress.
  * Lưu ảnh đã xử lý vào Output Bucket.

* Tích hợp thành công thư viện **Pillow (PIL)** vào Lambda để phục vụ quá trình xử lý ảnh.

* Hoàn thiện cấu hình **IAM Execution Role** cho Lambda, đảm bảo:
  * Có quyền đọc dữ liệu từ Input Bucket.
  * Có quyền ghi dữ liệu vào Output Bucket.
  * Có quyền ghi log lên Amazon CloudWatch.
  * Tuân thủ nguyên tắc **Least Privilege** trong việc phân quyền.

* Triển khai các tài nguyên AWS bằng **AWS CDK**, bao gồm:
  * Amazon S3.
  * AWS Lambda.
  * IAM Role.

Qua đó giúp quá trình triển khai hạ tầng được tự động hóa và có thể tái sử dụng trong các lần triển khai tiếp theo.

* Kiểm tra và xác nhận các tài nguyên được tạo thành công trên tài khoản AWS sau khi triển khai bằng AWS CDK.

* Kiểm thử thành công luồng xử lý ảnh đầu tiên của hệ thống:

```text
Upload Image
      │
      ▼
Amazon S3 (Input Bucket)
      │
      ▼
AWS Lambda
      │
      ├── Resize Image
      ├── Compress Image
      │
      ▼
Amazon S3 (Output Bucket)
```

* Theo dõi quá trình thực thi của Lambda thông qua **Amazon CloudWatch Logs**, xác nhận hàm được kích hoạt đúng khi có ảnh mới được tải lên Amazon S3 và hoàn thành quá trình xử lý mà không phát sinh lỗi.

* Cập nhật tài liệu triển khai ban đầu và sơ đồ kiến trúc hệ thống, làm cơ sở cho việc tích hợp **Amazon DynamoDB** để quản lý metadata trong tuần tiếp theo.

* Hoàn thành giai đoạn xây dựng nền tảng của hệ thống, bao gồm **Storage Layer**, **Image Processing Lambda** và quy trình xử lý ảnh cơ bản, tạo tiền đề để mở rộng các chức năng ở các tuần tiếp theo.