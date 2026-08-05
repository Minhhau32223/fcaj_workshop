---
title: "Worklog Tuần 1"
date: 2026-06-22
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Tìm hiểu yêu cầu và mục tiêu của đề tài **Automatic Image Optimization System on AWS**.
* Làm quen với kiến trúc Serverless trên AWS.
* Nghiên cứu các dịch vụ AWS sẽ sử dụng trong hệ thống.
* Thiết kế kiến trúc tổng quan của dự án.
* Thiết lập môi trường phát triển và khởi tạo repository.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Phân tích yêu cầu đề tài <br> - Xác định Input/Output của hệ thống <br> - Phân tích luồng Upload → Processing → Output | 22/06/2026 | 22/06/2026 | Tài liệu yêu cầu dự án |
| 3 | - Tìm hiểu kiến trúc Serverless trên AWS <br>&emsp; + Amazon S3 <br>&emsp; + AWS Lambda <br>&emsp; + Amazon DynamoDB <br>&emsp; + Amazon CloudWatch <br>&emsp; + Amazon SNS <br>&emsp; + AWS IAM | 23/06/2026 | 23/06/2026 | https://docs.aws.amazon.com/ |
| 4 | - Tìm hiểu Amazon S3 <br>&emsp; + Bucket <br>&emsp; + Object <br>&emsp; + Bucket Policy <br>&emsp; + Event Notification <br> - Nghiên cứu phương án lưu trữ ảnh đầu vào và đầu ra | 24/06/2026 | 24/06/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html |
| 5 | - Tìm hiểu AWS Lambda <br>&emsp; + Function <br>&emsp; + Runtime <br>&emsp; + Handler <br>&emsp; + Execution Role <br> - Nghiên cứu luồng xử lý Amazon S3 → AWS Lambda | 25/06/2026 | 25/06/2026 | https://docs.aws.amazon.com/lambda/latest/dg/welcome.html |
| 6 | - Thiết kế sơ đồ kiến trúc hệ thống <br> - Khởi tạo GitHub Repository <br> - Khởi tạo dự án AWS CDK <br> - Cài đặt AWS CLI và môi trường phát triển | 26/06/2026 | 26/06/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |

### Kết quả đạt được tuần 1:

* Hoàn thành việc tìm hiểu yêu cầu, phạm vi và mục tiêu của đề tài **Automatic Image Optimization System on AWS**, đồng thời xác định được các thành phần chính cần xây dựng trong hệ thống.

* Nắm được kiến trúc **Serverless** và vai trò của các dịch vụ AWS sẽ sử dụng, bao gồm:
  * Amazon S3
  * AWS Lambda
  * Amazon DynamoDB
  * Amazon CloudWatch
  * Amazon SNS
  * AWS IAM

* Hoàn thành thiết kế sơ bộ kiến trúc của hệ thống với luồng xử lý như sau:

```text
User
  │
  ▼
Amazon S3 (Input Bucket)
  │
  ▼
AWS Lambda
  │
  ├── Amazon S3 (Output Bucket)
  └── Amazon DynamoDB
```

* Khởi tạo thành công **GitHub Repository** và dự án **AWS CDK**, tạo nền tảng để quản lý mã nguồn và triển khai hạ tầng bằng **Infrastructure as Code (IaC)**.

* Thiết lập hoàn chỉnh môi trường phát triển, bao gồm:
  * Cài đặt Python Virtual Environment.
  * Cài đặt và cấu hình AWS CLI.
  * Cài đặt AWS CDK.
  * Kết nối tài khoản AWS phục vụ quá trình triển khai và kiểm thử.

* Xây dựng kế hoạch triển khai dự án, thống nhất kiến trúc tổng thể và phân chia nhiệm vụ giữa các thành viên trong nhóm.

* Hoàn thiện sơ đồ kiến trúc và tài liệu thiết kế ban đầu, làm cơ sở cho việc triển khai **Amazon S3**, **AWS Lambda** và **Image Processing Pipeline** trong tuần tiếp theo.