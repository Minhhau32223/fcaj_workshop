---
title: "Worklog Tuần 4"
date: 2026-07-13
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Mở rộng kiến trúc hệ thống với Amazon API Gateway.
* Xây dựng Upload API cho hệ thống.
* Tìm hiểu cơ chế Presigned URL của Amazon S3.
* Triển khai API Gateway bằng AWS CDK.
* Hỗ trợ tích hợp Frontend với Backend thông qua API.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu Amazon API Gateway <br> - Nghiên cứu REST API và HTTP Method <br> - Tìm hiểu mô hình API Gateway → Lambda Integration | 13/07/2026 | 13/07/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html |
| 3 | - Xây dựng Upload Lambda <br> - Thiết kế API `POST /images/upload` <br> - Tìm hiểu cơ chế Presigned URL của Amazon S3 | 14/07/2026 | 14/07/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html |
| 4 | - Triển khai API Gateway bằng AWS CDK <br> - Kết nối API Gateway với Upload Lambda <br> - Kiểm thử API bằng Postman | 15/07/2026 | 15/07/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |
| 5 | - Hỗ trợ tích hợp Frontend với Upload API <br> - Kiểm thử Upload thông qua Presigned URL <br> - Kiểm tra CORS và IAM Permission | 16/07/2026 | 16/07/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-cors.html |
| 6 | - Kiểm thử toàn bộ Upload Flow <br> - Khắc phục lỗi API và cấu hình hạ tầng <br> - Cập nhật tài liệu kiến trúc hệ thống | 17/07/2026 | 17/07/2026 | https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/serverless-multi-tier-architectures-api-gateway-lambda.html |

### Kết quả đạt được tuần 4:

* Hoàn thành nghiên cứu và triển khai **Amazon API Gateway** làm cổng giao tiếp giữa ứng dụng Frontend và các dịch vụ AWS trong kiến trúc Serverless.

* Thiết kế và triển khai thành công Upload API:

```text
POST /images/upload
```

API có nhiệm vụ tiếp nhận yêu cầu từ phía Frontend, gọi Upload Lambda để tạo **Presigned URL**, sau đó trả kết quả về cho người dùng.

* Xây dựng **Upload Lambda** với các chức năng:
  * Tiếp nhận yêu cầu từ API Gateway.
  * Kiểm tra thông tin file tải lên.
  * Sinh Presigned URL để upload trực tiếp lên Amazon S3.
  * Trả về URL cùng các thông tin cần thiết cho phía Frontend.

* Triển khai thành công **Amazon API Gateway** bằng **AWS CDK**, giúp toàn bộ hạ tầng được quản lý theo mô hình **Infrastructure as Code (IaC)** và dễ dàng tái triển khai khi cần.

* Hoàn thiện kết nối giữa các thành phần trong hệ thống:

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
Generate Presigned URL
      │
      ▼
Amazon S3 (Input Bucket)
```

* Kiểm thử API bằng **Postman** và xác nhận:
  * API hoạt động ổn định.
  * Trả về Presigned URL hợp lệ.
  * Có thể tải ảnh trực tiếp lên Amazon S3 thông qua URL được cấp.
  * Upload thành công với nhiều định dạng ảnh phổ biến như JPG, PNG và WEBP.

* Hỗ trợ tích hợp Upload API với Frontend, giúp người dùng có thể tải ảnh lên hệ thống thông qua API Gateway thay vì truy cập trực tiếp Amazon S3.

* Kiểm tra và điều chỉnh **IAM Role**, **Bucket Policy** và **CORS Configuration**, đảm bảo Upload Lambda chỉ được cấp các quyền cần thiết và Frontend có thể truy cập API an toàn.

* Cập nhật tài liệu triển khai và sơ đồ kiến trúc sau khi bổ sung API Gateway, phản ánh đầy đủ luồng xử lý dữ liệu mới của hệ thống.

* Kiểm thử thành công luồng Upload hoàn chỉnh:

```text
Người dùng
      │
      ▼
Frontend
      │
      ▼
Amazon API Gateway
      │
      ▼
Upload Lambda
      │
      ▼
Generate Presigned URL
      │
      ▼
Amazon S3 (Input Bucket)
      │
      ▼
Image Processing Pipeline
```

* Hoàn thành giai đoạn xây dựng **Upload Service**, tạo nền tảng để tuần tiếp theo mở rộng hệ thống theo kiến trúc **Event-driven** với **Amazon EventBridge**, đồng thời tăng khả năng mở rộng và giảm sự phụ thuộc giữa các thành phần trong hệ thống.