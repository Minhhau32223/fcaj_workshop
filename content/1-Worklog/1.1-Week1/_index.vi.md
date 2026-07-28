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
* Tìm hiểu các dịch vụ AWS dự kiến sử dụng trong hệ thống.
* Thiết kế kiến trúc tổng quan của hệ thống.
* Thiết lập môi trường phát triển và repository cho project.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Phân tích yêu cầu đề tài <br> - Xác định input/output của hệ thống <br> - Xác định flow upload → processing → output | 22/06/2026 | 22/06/2026 | AWS Documentation |
| 3 | - Tìm hiểu AWS Serverless Architecture <br>&emsp; + S3 <br>&emsp; + Lambda <br>&emsp; + DynamoDB <br>&emsp; + CloudWatch <br>&emsp; + SNS <br>&emsp; + IAM | 23/06/2026 | 23/06/2026 | AWS Documentation |
| 4 | - Tìm hiểu Amazon S3 <br>&emsp; + Bucket <br>&emsp; + Object <br>&emsp; + Bucket Policy <br>&emsp; + Event notification <br> - Tìm hiểu cách lưu trữ ảnh input/output | 24/06/2026 | 24/06/2026 | AWS Documentation |
| 5 | - Tìm hiểu AWS Lambda <br>&emsp; + Function <br>&emsp; + Runtime <br>&emsp; + Handler <br>&emsp; + Execution Role <br> - Tìm hiểu flow S3 → Lambda | 25/06/2026 | 25/06/2026 | AWS Documentation |
| 6 | - Thiết kế architecture diagram <br> - Tạo GitHub repository <br> - Khởi tạo AWS CDK project <br> - Setup môi trường development | 26/06/2026 | 26/06/2026 | AWS CDK Documentation |

### Kết quả đạt được tuần 1:

* Hiểu được mục tiêu và phạm vi của đề tài **Automatic Image Optimization System on AWS**.
* Nắm được kiến trúc Serverless cơ bản và vai trò của các AWS services trong hệ thống.
* Hiểu được vai trò của:
  * Amazon S3
  * AWS Lambda
  * Amazon DynamoDB
  * Amazon CloudWatch
  * Amazon SNS
  * AWS IAM
* Hiểu được flow xử lý ảnh cơ bản:

```text
S3 Input
   ↓
Lambda
   ↓
S3 Output
   ↓
DynamoDB