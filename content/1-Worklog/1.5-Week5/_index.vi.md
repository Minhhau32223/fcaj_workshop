---
title: "Worklog Tuần 5"
date: 2026-07-20
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Tìm hiểu kiến trúc Event-driven trên AWS.
* Triển khai Amazon EventBridge vào hệ thống.
* Kết nối sự kiện từ Amazon S3 đến AWS Lambda.
* Tích hợp EventBridge với Image Processing Pipeline.
* Hoàn thiện kiến trúc xử lý ảnh theo mô hình Event-driven.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu kiến trúc Event-driven <br> - Tìm hiểu Amazon EventBridge <br> - Nghiên cứu Event Bus, Rule và Target | 20/07/2026 | 20/07/2026 | https://docs.aws.amazon.com/eventbridge/latest/userguide/what-is-amazon-eventbridge.html |
| 3 | - Xây dựng EventBridge Rule <br> - Thiết lập Event Pattern cho sự kiện S3 Object Created <br> - Phân tích cấu trúc Event Payload | 21/07/2026 | 21/07/2026 | https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-patterns.html |
| 4 | - Kết nối Amazon S3 với EventBridge <br> - Kết nối EventBridge với Image Processing Lambda <br> - Kiểm thử Event Payload | 22/07/2026 | 22/07/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventBridge.html |
| 5 | - Điều chỉnh Image Processing Lambda để xử lý EventBridge Event <br> - Kiểm thử với nhiều loại ảnh <br> - Kiểm tra trường hợp xử lý trùng lặp | 23/07/2026 | 23/07/2026 | https://docs.aws.amazon.com/lambda/latest/dg/with-eventbridge.html |
| 6 | - Triển khai EventBridge bằng AWS CDK <br> - Kiểm thử toàn bộ pipeline <br> - Khắc phục lỗi phát sinh trong quá trình xử lý sự kiện | 24/07/2026 | 24/07/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |

### Kết quả đạt được tuần 5:

* Hiểu được nguyên lý hoạt động của **Event-driven Architecture** và cách áp dụng mô hình này vào hệ thống xử lý ảnh trên AWS.

* Nghiên cứu và triển khai thành công **Amazon EventBridge** làm trung gian điều phối sự kiện giữa các dịch vụ AWS, giúp giảm sự phụ thuộc trực tiếp giữa Amazon S3 và AWS Lambda.

* Xây dựng và cấu hình thành công **EventBridge Rule** để lắng nghe sự kiện **Object Created** từ Amazon S3.

* Hoàn thiện kết nối giữa **Amazon S3**, **Amazon EventBridge** và **AWS Lambda**, đảm bảo Lambda được kích hoạt tự động khi có ảnh mới được tải lên Input Bucket.

* Điều chỉnh Image Processing Lambda để tiếp nhận và xử lý dữ liệu theo định dạng EventBridge Event, đồng thời kiểm tra tính chính xác của Event Payload.

* Triển khai hạ tầng EventBridge bằng **AWS CDK**, giúp việc quản lý và triển khai hạ tầng được đồng bộ với các thành phần đã xây dựng trước đó.

* Kiểm thử thành công toàn bộ luồng xử lý ảnh theo mô hình Event-driven:

```text
Người dùng
      │
      ▼
Frontend
      │
      ▼
API Gateway
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
      ├── Resize Image
      ├── Compress Image
      ├── Upload Output Image
      └── Lưu Metadata
      │
      ▼
Amazon S3 (Output Bucket)
      │
      ▼
Amazon DynamoDB
```

* Kiểm tra thành công khả năng xử lý nhiều ảnh liên tiếp, xác nhận EventBridge truyền sự kiện chính xác và Lambda thực hiện xử lý ổn định.

* Cập nhật sơ đồ kiến trúc hệ thống và tài liệu triển khai để phản ánh mô hình Event-driven sau khi bổ sung Amazon EventBridge.

* Hoàn thành giai đoạn mở rộng kiến trúc Serverless, tạo tiền đề cho việc triển khai **CloudWatch Monitoring**, **Amazon SNS Alerting**, **CI/CD Pipeline** và các chức năng giám sát hệ thống trong tuần tiếp theo.