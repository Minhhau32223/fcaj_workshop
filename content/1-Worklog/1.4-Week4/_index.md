---
title: "Week 4 Worklog"
date: 2026-07-13
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Expand the system architecture with Amazon API Gateway.
* Build the Upload API for the system.
* Learn about the Amazon S3 Presigned URL mechanism.
* Deploy API Gateway using AWS CDK.
* Support Frontend and Backend integration via API.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Learn about Amazon API Gateway <br> - Research REST API and HTTP Methods <br> - Learn the API Gateway → Lambda Integration model | 13/07/2026 | 13/07/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html |
| Tuesday | - Build Upload Lambda <br> - Design the `POST /images/upload` API <br> - Learn the Amazon S3 Presigned URL mechanism | 14/07/2026 | 14/07/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html |
| Wednesday | - Deploy API Gateway using AWS CDK <br> - Connect API Gateway with Upload Lambda <br> - Test API using Postman | 15/07/2026 | 15/07/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |
| Thursday | - Support integrating Frontend with Upload API <br> - Test Upload via Presigned URL <br> - Check CORS and IAM Permissions | 16/07/2026 | 16/07/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-cors.html |
| Friday | - Test the entire Upload Flow <br> - Troubleshoot API errors and infrastructure configuration <br> - Update system architecture documentation | 17/07/2026 | 17/07/2026 | https://docs.aws.amazon.com/whitepapers/latest/serverless-multi-tier-architectures-api-gateway-lambda/serverless-multi-tier-architectures-api-gateway-lambda.html |

### Week 4 Achievements:

* Completed researching and deploying **Amazon API Gateway** as the communication gateway between the Frontend application and AWS services in the Serverless architecture.

* Successfully designed and deployed the Upload API:

```text
POST /images/upload
```

The API is responsible for receiving requests from the Frontend, calling the Upload Lambda to generate a **Presigned URL**, and then returning the result to the user.

* Built the **Upload Lambda** with the following functions:
  * Receive requests from API Gateway.
  * Validate uploaded file information.
  * Generate a Presigned URL for direct upload to Amazon S3.
  * Return the URL along with necessary information to the Frontend.

* Successfully deployed **Amazon API Gateway** using **AWS CDK**, helping the entire infrastructure to be managed under the **Infrastructure as Code (IaC)** model and easily redeployed when needed.

* Completed the connection between system components:

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

* Tested the API using **Postman** and confirmed:
  * The API works stably.
  * Returns a valid Presigned URL.
  * Images can be uploaded directly to Amazon S3 via the provided URL.
  * Successful uploads with various popular image formats such as JPG, PNG, and WEBP.

* Supported integrating the Upload API with the Frontend, allowing users to upload images to the system via the API Gateway instead of directly accessing Amazon S3.

* Checked and adjusted the **IAM Role**, **Bucket Policy**, and **CORS Configuration**, ensuring the Upload Lambda is only granted necessary permissions and the Frontend can securely access the API.

* Updated the deployment documentation and system architecture diagram after adding API Gateway, fully reflecting the system's new data processing flow.

* Successfully tested the complete Upload flow:

```text
User
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

* Completed the **Upload Service** building phase, creating a foundation for next week to expand the system with an **Event-driven** architecture using **Amazon EventBridge**, while increasing scalability and reducing dependencies between system components.