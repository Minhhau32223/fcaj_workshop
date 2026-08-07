---
title: "Worklog Tuần 8"
date: 2026-08-10
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Hoàn thiện project **Automatic Image Optimization System on AWS**.
* Rà soát lại các thành phần đã triển khai trong những tuần trước.
* Hoàn thiện architecture diagram và tài liệu kỹ thuật.
* Tổng hợp kết quả và chuẩn bị nội dung presentation.
* Tổng kết kiến thức và kinh nghiệm sau quá trình thực tập.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Review source code <br> - Kiểm tra cấu trúc project <br> - Rà soát các AWS resources <br> - Kiểm tra các lỗi còn tồn tại | 10/08/2026 | 10/08/2026 | Project Documentation |
| 3 | - Hoàn thiện Architecture Diagram <br> - Rà soát flow Upload → Processing → Output <br> - Cập nhật Monitoring và Security flow | 11/08/2026 | 11/08/2026 | AWS Documentation |
| 4 | - Hoàn thiện README <br> - Hoàn thiện Setup Guide <br> - Hoàn thiện Deployment Guide <br> - Hoàn thiện Testing Guide | 12/08/2026 | 12/08/2026 | Project Documentation |
| 5 | - Hoàn thiện Cleanup Guide <br> - Rà soát AWS resources <br> - Kiểm tra các tài nguyên cần xóa sau khi demo | 13/08/2026 | 13/08/2026 | AWS Documentation |
| 6 | - Tổng hợp kết quả project <br> - Chuẩn bị presentation <br> - Chuẩn bị nội dung demo <br> - Tổng kết quá trình thực tập | 14/08/2026 | 15/08/2026 | Project Documentation |

### Kết quả đạt được tuần 8:

* Hoàn thiện các thành phần chính của project **Automatic Image Optimization System on AWS** đã được triển khai trong các tuần trước.

* Rà soát lại toàn bộ kiến trúc hệ thống và cách các thành phần kết nối với nhau:

```text
Frontend
    ↓
API Gateway
    ↓
Upload Lambda
    ↓
Presigned URL
    ↓
S3 Input
    ↓
EventBridge
    ↓
Image Processing Lambda
    ├── Resize
    ├── Compress
    └── Convert
    ↓
S3 Output
    ↓
DynamoDB
```