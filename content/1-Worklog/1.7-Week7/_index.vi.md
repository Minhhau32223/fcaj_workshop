---
title: "Worklog Tuần 7"
date: 2026-08-03
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Hoàn thiện quy trình CI/CD cho dự án.
* Tự động hóa việc triển khai hạ tầng AWS bằng AWS CDK.
* Kiểm thử toàn bộ hệ thống theo quy trình End-to-End.
* Kiểm tra các trường hợp xử lý thành công và thất bại.
* Khắc phục các lỗi còn tồn tại trước khi hoàn thiện dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu GitHub Actions <br> - Thiết kế quy trình CI/CD <br> - Xây dựng Workflow triển khai AWS CDK | 03/08/2026 | 03/08/2026 | https://docs.github.com/en/actions |
| 3 | - Tích hợp GitHub Actions với AWS CDK <br> - Kiểm thử CDK Deploy từ GitHub Repository <br> - Kiểm tra trạng thái triển khai | 04/08/2026 | 04/08/2026 | https://docs.aws.amazon.com/cdk/v2/guide/home.html |
| 4 | - Kiểm thử ảnh JPG, PNG, WEBP <br> - Kiểm thử với nhiều kích thước ảnh khác nhau <br> - Đánh giá kết quả Resize và Compression | 05/08/2026 | 05/08/2026 | https://pillow.readthedocs.io/en/stable/ |
| 5 | - Kiểm thử ảnh không hợp lệ <br> - Kiểm thử Lambda Failure <br> - Kiểm tra trạng thái FAILED trên DynamoDB <br> - Kiểm thử CloudWatch Alarm và Amazon SNS | 06/08/2026 | 06/08/2026 | https://docs.aws.amazon.com/ |
| 6 | - Kiểm thử toàn bộ End-to-End Pipeline <br> - Khắc phục lỗi phát sinh <br> - Rà soát IAM Permission <br> - Kiểm tra CI/CD Pipeline lần cuối | 07/08/2026 | 07/08/2026 | https://docs.github.com/en/actions |

### Kết quả đạt được tuần 7:

* Hoàn thiện quy trình **CI/CD** cho dự án bằng **GitHub Actions**, giúp tự động hóa quá trình triển khai hạ tầng AWS sau mỗi lần cập nhật mã nguồn.

* Xây dựng thành công **GitHub Actions Workflow** với các bước:
  * Kiểm tra mã nguồn từ GitHub Repository.
  * Thiết lập môi trường thực thi.
  * Cài đặt các thư viện cần thiết.
  * Thực hiện **AWS CDK Deploy**.
  * Cập nhật hạ tầng AWS tự động.

* Kiểm thử thành công quy trình triển khai tự động:

```text
Git Push
      │
      ▼
GitHub Actions
      │
      ▼
Build & Validate
      │
      ▼
AWS CDK Deploy
      │
      ▼
AWS Infrastructure
```

* Hoàn thiện kiểm thử chức năng xử lý ảnh với nhiều định dạng và kích thước khác nhau, bao gồm:
  * JPG
  * PNG
  * WEBP

* Xác nhận hệ thống xử lý chính xác các chức năng:
  * Upload ảnh.
  * Resize ảnh.
  * Compress ảnh.
  * Lưu ảnh vào Amazon S3 Output Bucket.
  * Cập nhật metadata vào Amazon DynamoDB.

* Kiểm thử các trường hợp ngoại lệ của hệ thống:
  * Ảnh không đúng định dạng.
  * Lỗi trong quá trình xử lý của AWS Lambda.
  * Trạng thái **FAILED** được lưu chính xác trong Amazon DynamoDB.
  * CloudWatch Alarm được kích hoạt khi phát sinh lỗi.
  * Amazon SNS gửi email cảnh báo thành công đến người quản trị.

* Thực hiện kiểm thử **End-to-End Pipeline**, xác nhận toàn bộ hệ thống hoạt động đúng theo thiết kế:

```text
Frontend
      │
      ▼
Amazon API Gateway
      │
      ▼
Upload Lambda
      │
      ▼
Amazon S3 (Input Bucket)
      │
      ▼
Amazon EventBridge
      │
      ▼
Image Processing Lambda
      │
      ▼
Amazon S3 (Output Bucket)
      │
      ▼
Amazon DynamoDB
      │
      ▼
CloudWatch Monitoring
      │
      ▼
Amazon SNS Alert
```

* Rà soát lại **IAM Role**, **Bucket Policy** và các cấu hình bảo mật nhằm đảm bảo hệ thống tuân thủ nguyên tắc **Least Privilege** và sẵn sàng cho quá trình triển khai thực tế.

* Cập nhật tài liệu triển khai, quy trình CI/CD và sơ đồ kiến trúc hệ thống để phản ánh đầy đủ các thành phần đã hoàn thiện.

* Hoàn thành quá trình kiểm thử tổng thể, khắc phục các lỗi còn tồn tại và xác nhận hệ thống vận hành ổn định, sẵn sàng bước sang giai đoạn hoàn thiện báo cáo và chuẩn bị demo trong tuần cuối.