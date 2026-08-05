---
title: "Worklog Tuần 3"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Hoàn thiện Image Optimization Pipeline.
* Chuẩn hóa quá trình resize và compression.
* Tích hợp Amazon DynamoDB để lưu metadata.
* Xử lý trạng thái SUCCESS/FAILED.
* Hoàn thiện việc triển khai S3, Lambda và DynamoDB bằng CDK.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tối ưu thuật toán resize <br> - Xác định kích thước output phù hợp cho web <br> - Chuẩn hóa định dạng ảnh | 06/07/2026 | 06/07/2026 | https://pillow.readthedocs.io/en/stable/ |
| 3 | - Chuẩn hóa quy tắc đặt tên file đầu ra <br> - Xây dựng cấu trúc lưu trữ trên Amazon S3 <br> - Xử lý các trường hợp ảnh không hợp lệ | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html |
| 4 | - Tìm hiểu Amazon DynamoDB <br> - Thiết kế bảng lưu metadata <br>&emsp; + imageId <br>&emsp; + fileName <br>&emsp; + inputSize <br>&emsp; + outputSize <br>&emsp; + status <br>&emsp; + createdAt | 08/07/2026 | 08/07/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html |
| 5 | - Kết nối AWS Lambda với Amazon DynamoDB <br> - Lưu trạng thái SUCCESS/FAILED <br> - Lưu thông tin ảnh sau khi xử lý | 09/07/2026 | 09/07/2026 | https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html |
| 6 | - Triển khai Amazon S3, AWS Lambda và Amazon DynamoDB bằng AWS CDK <br> - Kiểm tra tài nguyên sau khi triển khai <br> - Khắc phục lỗi phát sinh trong quá trình deploy | 10/07/2026 | 10/07/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |

### Kết quả đạt được tuần 3:

* Hoàn thiện **Image Processing Pipeline**, cho phép hệ thống tự động xử lý ảnh sau khi được tải lên Amazon S3.

* Chuẩn hóa quá trình xử lý ảnh với các chức năng:
  * Resize ảnh theo kích thước phù hợp cho ứng dụng web.
  * Compress ảnh nhằm giảm dung lượng nhưng vẫn đảm bảo chất lượng hiển thị.
  * Chuẩn hóa định dạng và quy tắc đặt tên ảnh đầu ra.

* Hoàn thiện cấu trúc lưu trữ dữ liệu trên Amazon S3, giúp quản lý ảnh gốc và ảnh sau xử lý rõ ràng, thuận tiện cho việc mở rộng hệ thống.

* Thiết kế và triển khai thành công bảng **ImageMetadata** trên Amazon DynamoDB để lưu trữ thông tin của mỗi ảnh sau khi xử lý.

Bảng metadata bao gồm các thuộc tính:

| Thuộc tính | Mô tả |
|------------|-------|
| imageId | Mã định danh của ảnh |
| fileName | Tên tệp ảnh |
| inputSize | Kích thước ảnh gốc |
| outputSize | Kích thước ảnh sau tối ưu |
| status | Trạng thái xử lý |
| createdAt | Thời điểm hoàn thành xử lý |

* Hoàn thành tích hợp giữa **AWS Lambda** và **Amazon DynamoDB**, cho phép Lambda tự động ghi nhận metadata sau mỗi lần xử lý ảnh.

* Hệ thống có khả năng theo dõi trạng thái xử lý của từng ảnh:

```text
SUCCESS
FAILED
```

Trong đó:

- **SUCCESS:** Ảnh được xử lý thành công, lưu vào Output Bucket và cập nhật metadata vào DynamoDB.
- **FAILED:** Quá trình xử lý xảy ra lỗi, trạng thái được ghi nhận để phục vụ việc theo dõi và khắc phục sau này.

* Triển khai thành công hạ tầng bằng **AWS CDK**, bao gồm:
  * Amazon S3
  * AWS Lambda
  * Amazon DynamoDB
  * IAM Role

Qua đó giúp việc triển khai hạ tầng được tự động hóa, đồng nhất giữa các môi trường và thuận tiện cho việc quản lý phiên bản.

* Kiểm tra và xác nhận các tài nguyên AWS được tạo thành công sau quá trình triển khai bằng AWS CDK.

* Kiểm thử thành công toàn bộ luồng xử lý ảnh và lưu metadata:

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
      │
      ▼
Amazon DynamoDB
      │
      ▼
Lưu metadata và trạng thái xử lý
```

* Cập nhật tài liệu triển khai và sơ đồ kiến trúc hệ thống sau khi bổ sung Amazon DynamoDB, đảm bảo phản ánh đúng luồng xử lý và cấu trúc hạ tầng hiện tại.

* Hoàn thành giai đoạn xây dựng **Core Image Optimization Pipeline**, tạo nền tảng để tuần tiếp theo triển khai **Amazon API Gateway** và xây dựng dịch vụ Upload API cho hệ thống.