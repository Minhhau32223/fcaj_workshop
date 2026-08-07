---
title: "Week 3 Worklog"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Complete the Image Optimization Pipeline.
* Standardize the resize and compression process.
* Integrate Amazon DynamoDB to store metadata.
* Handle SUCCESS/FAILED statuses.
* Complete the deployment of S3, Lambda, and DynamoDB using CDK.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Optimize resize algorithm <br> - Determine suitable output size for web <br> - Standardize image format | 06/07/2026 | 06/07/2026 | https://pillow.readthedocs.io/en/stable/ |
| Tuesday | - Standardize output file naming conventions <br> - Build storage structure on Amazon S3 <br> - Handle invalid image cases | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html |
| Wednesday | - Learn about Amazon DynamoDB <br> - Design metadata table <br>&emsp; + imageId <br>&emsp; + fileName <br>&emsp; + inputSize <br>&emsp; + outputSize <br>&emsp; + status <br>&emsp; + createdAt | 08/07/2026 | 08/07/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html |
| Thursday | - Connect AWS Lambda with Amazon DynamoDB <br> - Save SUCCESS/FAILED status <br> - Save image information after processing | 09/07/2026 | 09/07/2026 | https://docs.aws.amazon.com/lambda/latest/dg/with-ddb.html |
| Friday | - Deploy Amazon S3, AWS Lambda, and Amazon DynamoDB using AWS CDK <br> - Check resources after deployment <br> - Troubleshoot errors arising during deployment | 10/07/2026 | 10/07/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |

### Week 3 Achievements:

* Completed the **Image Processing Pipeline**, allowing the system to automatically process images after they are uploaded to Amazon S3.

* Standardized the image processing with the following functions:
  * Resize images to a suitable size for web applications.
  * Compress images to reduce file size while maintaining display quality.
  * Standardize the format and naming conventions of output images.

* Perfected the data storage structure on Amazon S3, helping to manage original and processed images clearly, facilitating system expansion.

* Successfully designed and deployed the **ImageMetadata** table on Amazon DynamoDB to store information for each image after processing.

The metadata table includes the following attributes:

| Attribute | Description |
|-----------|-------------|
| imageId | Image identifier |
| fileName | Image file name |
| inputSize | Original image size |
| outputSize | Optimized image size |
| status | Processing status |
| createdAt | Processing completion time |

* Completed the integration between **AWS Lambda** and **Amazon DynamoDB**, allowing Lambda to automatically record metadata after each image processing.

* The system has the capability to track the processing status of each image:

```text
SUCCESS
FAILED
```

Where:

- **SUCCESS:** The image was processed successfully, saved to the Output Bucket, and its metadata was updated in DynamoDB.
- **FAILED:** An error occurred during processing; the status is recorded for monitoring and future troubleshooting.

* Successfully deployed the infrastructure using **AWS CDK**, including:
  * Amazon S3
  * AWS Lambda
  * Amazon DynamoDB
  * IAM Role

Thereby helping the infrastructure deployment process become automated, consistent across environments, and convenient for version management.

* Checked and confirmed that AWS resources were successfully created after deployment using AWS CDK.

* Successfully tested the entire image processing flow and metadata storage:

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
Save metadata and processing status
```

* Updated the deployment documentation and system architecture diagram after adding Amazon DynamoDB, ensuring it accurately reflects the current processing flow and infrastructure structure.

* Completed the **Core Image Optimization Pipeline** building phase, laying the foundation for deploying **Amazon API Gateway** and building the Upload API service for the system next week.