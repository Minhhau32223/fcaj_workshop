---
title: "Worklog Tuần 6"
date: 2026-07-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Hoàn thiện hệ thống giám sát (Monitoring) cho toàn bộ pipeline.
* Thiết lập Amazon CloudWatch Logs, Metrics và Dashboard.
* Cấu hình CloudWatch Alarm và Amazon SNS để gửi cảnh báo khi xảy ra lỗi.
* Rà soát quyền truy cập theo nguyên tắc Least Privilege.
* Tìm hiểu và áp dụng mã hóa dữ liệu bằng AWS KMS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu Amazon CloudWatch Logs <br> - Kiểm tra log của AWS Lambda <br> - Chuẩn hóa nội dung log <br> - Xác định các thông tin cần ghi nhận | 27/07/2026 | 27/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html |
| 3 | - Tìm hiểu Amazon CloudWatch Metrics <br> - Theo dõi Lambda Invocations, Errors, Duration <br> - Xây dựng CloudWatch Dashboard | 28/07/2026 | 28/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html |
| 4 | - Tạo CloudWatch Alarm <br> - Thiết lập điều kiện cảnh báo khi Lambda xảy ra lỗi <br> - Tìm hiểu Amazon SNS | 29/07/2026 | 29/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| 5 | - Kết nối CloudWatch Alarm với Amazon SNS <br> - Cấu hình Email Notification <br> - Kiểm thử các tình huống phát sinh lỗi | 30/07/2026 | 30/07/2026 | https://docs.aws.amazon.com/sns/latest/dg/welcome.html |
| 6 | - Rà soát IAM Policy và Bucket Policy <br> - Kiểm tra quyền truy cập của các dịch vụ <br> - Tìm hiểu AWS KMS <br> - Kiểm tra mã hóa dữ liệu cho Amazon S3 | 31/07/2026 | 31/07/2026 | https://docs.aws.amazon.com/kms/latest/developerguide/overview.html |

### Kết quả đạt được tuần 6:

* Hoàn thiện hệ thống **Monitoring** cho Image Optimization Pipeline bằng **Amazon CloudWatch**, giúp theo dõi trạng thái hoạt động của các thành phần trong hệ thống theo thời gian thực.

* Chuẩn hóa nội dung **CloudWatch Logs** của AWS Lambda, giúp dễ dàng theo dõi quá trình xử lý ảnh và hỗ trợ việc phân tích, khắc phục lỗi khi có sự cố.

* Thiết lập theo dõi các chỉ số quan trọng của AWS Lambda thông qua **CloudWatch Metrics**, bao gồm:

  * Invocations
  * Errors
  * Duration
  * Throttles
  * Success Rate

* Xây dựng **CloudWatch Dashboard** để trực quan hóa trạng thái hoạt động của hệ thống, giúp dễ dàng theo dõi hiệu suất và tình trạng xử lý ảnh.

* Thiết lập **CloudWatch Alarm** nhằm phát hiện các trường hợp Lambda xử lý thất bại hoặc phát sinh lỗi vượt quá ngưỡng cho phép.

* Kết nối thành công **CloudWatch Alarm** với **Amazon SNS**, cho phép hệ thống tự động gửi email thông báo khi xảy ra lỗi trong quá trình xử lý ảnh.

* Kiểm thử thành công cơ chế cảnh báo bằng cách mô phỏng các tình huống xử lý lỗi và xác nhận email được gửi đến người quản trị đúng theo cấu hình.

* Rà soát và tối ưu **IAM Role**, **IAM Policy** và **S3 Bucket Policy**, đảm bảo các dịch vụ chỉ được cấp các quyền cần thiết theo nguyên tắc **Least Privilege**.

* Nghiên cứu và áp dụng **AWS Key Management Service (AWS KMS)** để tìm hiểu cơ chế mã hóa dữ liệu trên AWS, đồng thời kiểm tra khả năng mã hóa đối với Amazon S3 nhằm tăng cường bảo mật dữ liệu.

* Kiểm thử hoàn chỉnh luồng giám sát và cảnh báo của hệ thống:

```text
AWS Lambda
      │
      ▼
Amazon CloudWatch Logs
      │
      ▼
CloudWatch Metrics
      │
      ▼
CloudWatch Alarm
      │
      ▼
Amazon SNS
      │
      ▼
Email Notification
```

* Cập nhật tài liệu triển khai và sơ đồ kiến trúc hệ thống sau khi bổ sung **CloudWatch**, **Amazon SNS** và các thành phần bảo mật, giúp phản ánh đầy đủ kiến trúc của hệ thống trước giai đoạn hoàn thiện và triển khai cuối cùng.

* Hoàn thành hệ thống **Monitoring**, **Alerting** và **Security**, tạo nền tảng để thực hiện kiểm thử tổng thể, xây dựng quy trình CI/CD và chuẩn bị cho buổi demo ở các tuần tiếp theo.