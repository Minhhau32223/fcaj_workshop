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
| 2 | - Tối ưu thuật toán resize <br> - Xác định kích thước output phù hợp cho web <br> - Chuẩn hóa image format | 06/07/2026 | 06/07/2026 | Python / Pillow Documentation |
| 3 | - Chuẩn hóa output file naming <br> - Xây dựng input/output folder structure <br> - Xử lý các trường hợp image không hợp lệ | 07/07/2026 | 07/07/2026 | AWS S3 Documentation |
| 4 | - Tìm hiểu Amazon DynamoDB <br> - Thiết kế metadata schema <br>&emsp; + imageId <br>&emsp; + fileName <br>&emsp; + inputSize <br>&emsp; + outputSize <br>&emsp; + status <br>&emsp; + timestamp | 08/07/2026 | 08/07/2026 | AWS DynamoDB Documentation |
| 5 | - Kết nối Lambda → DynamoDB <br> - Lưu trạng thái SUCCESS/FAILED <br> - Lưu kích thước trước và sau khi tối ưu | 09/07/2026 | 09/07/2026 | AWS DynamoDB Documentation |
| 6 | - Deploy S3 + Lambda + DynamoDB bằng CDK <br> - Kiểm tra resource sau deploy <br> - Fix các lỗi deployment | 10/07/2026 | 10/07/2026 | AWS CDK Documentation |

### Kết quả đạt được tuần 3:

* Hoàn thiện Image Processing Lambda.
* Chuẩn hóa resize và compression.
* Hoàn thiện output image naming.
* Tạo DynamoDB table lưu metadata.
* Lambda có khả năng lưu:
  * File name
  * Input size
  * Output size
  * Processing status
  * Timestamp
* Xử lý được hai trạng thái:

```text
SUCCESS
FAILED