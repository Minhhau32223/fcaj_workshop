---
title: "Foundations & Agent Setup - Amazon Bedrock AgentCore"
date: 2026-08-01
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch “Foundations & Agent Setup - Amazon Bedrock AgentCore”

### Mục Đích Của Sự Kiện

- Cung cấp kiến thức nền tảng và các bước thiết lập Agent (Foundations & Agent Setup).
- Giới thiệu tổng quan về kiến trúc và các thành phần cốt lõi của Amazon Bedrock AgentCore.
- Hướng dẫn thực hành (Hands-on Lab) triển khai Agent, kết nối công cụ và tích hợp bảo mật.
- Giúp người tham dự làm quen với quy trình xây dựng Web UI tương tác với AI Agent.

### Danh Sách Diễn Giả

- **Nghĩa Trần** - Diễn giả phần Workshop introduction & Amazon Bedrock AgentCore Overview
- **Anh Phạm** - Người hướng dẫn (Instructor) phần Hands-on Lab

### Nội Dung Nổi Bật

#### Tổng quan về Amazon Bedrock AgentCore (09:00 – 10:00)

Được dẫn dắt bởi diễn giả Nghĩa Trần, phần này tập trung vào việc giới thiệu các thành phần kiến trúc cốt lõi của Bedrock AgentCore:
- **Runtime:** Môi trường thực thi và xử lý logic của các AI Agent.
- **Gateway:** Cổng giao tiếp trung gian tiếp nhận và điều phối các API request.
- **Identity:** Cơ chế quản lý định danh, bảo mật và quyền truy cập vào các tài nguyên của hệ thống.

#### Thực hành Hands-on Lab (10:00 – 11:00)

Dưới sự hướng dẫn chi tiết của anh Anh Phạm, người tham gia được trực tiếp thao tác các bước:
- **Deploy a basic agent:** Khởi tạo và triển khai một AI Agent cơ bản trên môi trường AgentCore.
- **Integration:** Kết nối Agent với các công cụ bên ngoài (external tools) và Cơ sở tri thức (Knowledge Bases) để tăng cường khả năng xử lý thông tin.
- **Web UI & Security:** Xây dựng giao diện người dùng (Web UI) và tích hợp dịch vụ Amazon Cognito để xác thực người dùng.
- **Sử dụng Kuro:** Làm quen và ứng dụng công cụ Kuro trong quá trình thiết lập.

### Những Gì Học Được

#### Tư Duy Thiết Kế Hệ Thống AI

- Hiểu rõ vòng đời và cách thức hoạt động của một Agent thông qua các thành phần Runtime, Gateway và Identity.
- Nắm bắt phương pháp kết nối AI với dữ liệu doanh nghiệp (Knowledge Bases) thay vì chỉ sử dụng các mô hình ngôn ngữ chung chung.

#### Kỹ Năng Thực Hành Đám Mây (Cloud Practical Skills)

- Biết cách thao tác trực tiếp trên AWS để deploy một AI Agent hoàn chỉnh.
- Hiểu quy trình tích hợp Amazon Cognito vào Web UI, đảm bảo luồng xác thực (Authentication) an toàn theo tiêu chuẩn.

### Ứng Dụng Vào Công Việc

- **Phát triển Module Backend:** Tích hợp kiến thức về luồng Identity và Amazon Cognito vào quá trình thiết kế, triển khai các module phân quyền và xác thực (như module AUTH) cho các dự án phần mềm thực tế.
- **Xây dựng AI Features:** Áp dụng Amazon Bedrock để nghiên cứu và phát triển các tính năng tự động hóa, chatbot thông minh hoặc công cụ truy xuất dữ liệu từ Knowledge Bases.
- **Thực hành Serverless:** Tận dụng tư duy triển khai nhanh (deploy basic agent, external tools) để thiết kế các kiến trúc Backend tinh gọn và linh hoạt hơn.

### Trải nghiệm trong event

Tham gia sự kiện **“Foundations & Agent Setup”** là một cơ hội tuyệt vời để bước đầu làm quen với hệ sinh thái Generative AI của AWS. Một số trải nghiệm nổi bật:

#### Sự kết hợp hoàn hảo giữa Lý thuyết và Thực hành
- Phần trình bày của anh **Nghĩa Trần** rất súc tích, giúp tôi dễ dàng hình dung bức tranh tổng thể về AgentCore, đặc biệt là cách Runtime và Identity phối hợp với nhau.
- Ngay sau đó, phần Hands-on của anh **Anh Phạm** giúp biến những lý thuyết đó thành trải nghiệm thực tế, tránh được sự bỡ ngỡ khi làm quen với một nền tảng mới.

#### Trải nghiệm kỹ thuật thực tế
- Việc tự tay **deploy một basic agent** và kết nối nó với các **external tools** giúp tôi nhận ra việc tích hợp AI vào hệ thống hiện tại không quá phức tạp nếu nắm vững kiến trúc.
- Đặc biệt, phần tích hợp **Amazon Cognito** vào Web UI rất hữu ích với định hướng Backend của tôi, giúp tôi củng cố thêm kiến thức về thiết kế hệ thống bảo mật người dùng.

#### Bài học rút ra
- Sự kết hợp giữa AI (Bedrock) và các dịch vụ quản lý truyền thống (Cognito) mở ra rất nhiều hướng đi mới để xây dựng các ứng dụng hiện đại, bảo mật cao.
- IDE **Kuro** là một công cụ thú vị, giúp tối ưu hóa đáng kể thời gian xây dựng và tích hợp giao diện.

#### Một số hình ảnh khi tham gia sự kiện
-Ảnh 1 bắt đầu buổi event
![h1](/images/4-Event/event2-1.jpg)
-Ảnh 2 chia sẽ kiến thức
![h1](/images/4-Event/event2-2.jpg)
-Ảnh 3 hands-on
![h1](/images/4-Event/event2-3.jpg)

> Tổng thể, sự kiện mang lại giá trị thực tiễn rất cao. Quá trình chuyển tiếp mượt mà từ lý thuyết tổng quan đến việc tự tay triển khai hạ tầng AI không chỉ bổ sung kiến thức chuyên môn mà còn tiếp thêm rất nhiều động lực để tôi theo đuổi con đường Cloud Engineering.