---
title: "Week 2 Worklog"
date: 2026-06-29
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Deploy the Storage Layer using Amazon S3.
* Build a basic Image Processing Lambda.
* Learn and practice image processing using Python.
* Set up an IAM Role for Lambda.
* Build the first image processing pipeline.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Create S3 Input Bucket <br> - Create S3 Output Bucket <br> - Learn Object Key and Folder Structure | 29/06/2026 | 29/06/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html |
| Tuesday | - Learn AWS Lambda Python Runtime <br> - Build Image Processing Lambda <br> - Create a basic Lambda Handler | 30/06/2026 | 30/06/2026 | https://docs.aws.amazon.com/lambda/latest/dg/welcome.html |
| Wednesday | - Install Pillow library <br> - Practice Resize Image <br> - Practice Compress Image <br> - Test image processing in Local environment | 01/07/2026 | 01/07/2026 | https://pillow.readthedocs.io/en/stable/ |
| Thursday | - Connect Lambda with Amazon S3 <br> - Read image from Input Bucket <br> - Save processed image to Output Bucket | 02/07/2026 | 02/07/2026 | https://docs.aws.amazon.com/lambda/latest/dg/with-s3.html |
| Friday | - Create IAM Execution Role for Lambda <br> - Configure Amazon S3 access permissions <br> - Check CloudWatch Logs <br> - Test image processing pipeline | 03/07/2026 | 03/07/2026 | https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html |

### Week 2 Achievements:

* Completed the deployment of the system's **Storage Layer** using Amazon S3, including:
  * Creating an **Input Bucket** to store original images.
  * Creating an **Output Bucket** to store processed images.
  * Standardizing the storage structure and object naming conventions (Object Key).

* Built the first version of the **Image Processing Lambda** using Python with the ability to:
  * Receive events from Amazon S3.
  * Read images from the Input Bucket.
  * Perform Resize and Compress operations.
  * Save processed images to the Output Bucket.

* Successfully integrated the **Pillow (PIL)** library into Lambda to serve the image processing process.

* Finalized the **IAM Execution Role** configuration for Lambda, ensuring:
  * Permission to read data from the Input Bucket.
  * Permission to write data to the Output Bucket.
  * Permission to write logs to Amazon CloudWatch.
  * Compliance with the **Least Privilege** principle in permission delegation.

* Deployed AWS resources using **AWS CDK**, including:
  * Amazon S3.
  * AWS Lambda.
  * IAM Role.

Thereby helping the infrastructure deployment process become automated and reusable in subsequent deployments.

* Checked and confirmed that resources were successfully created on the AWS account after deployment using AWS CDK.

* Successfully tested the system's first image processing flow:

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
```

* Monitored Lambda's execution process through **Amazon CloudWatch Logs**, confirmed the function was triggered correctly when a new image was uploaded to Amazon S3, and completed the processing without errors.

* Updated the initial deployment documentation and system architecture diagram, serving as a basis for integrating **Amazon DynamoDB** to manage metadata in the following week.

* Completed the foundational building phase of the system, including the **Storage Layer**, **Image Processing Lambda**, and the basic image processing pipeline, laying the groundwork for expanding functionalities in the upcoming weeks.