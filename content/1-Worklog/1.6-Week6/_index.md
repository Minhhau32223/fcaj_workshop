---
title: "Week 6 Worklog"
date: 2026-07-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Complete the monitoring system for the entire pipeline.
* Set up Amazon CloudWatch Logs, Metrics, and Dashboard.
* Configure CloudWatch Alarm and Amazon SNS to send alerts when errors occur.
* Review access permissions according to the Least Privilege principle.
* Learn and apply data encryption using AWS KMS.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Learn about Amazon CloudWatch Logs <br> - Check AWS Lambda logs <br> - Standardize log content <br> - Identify information to record | 27/07/2026 | 27/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html |
| Tuesday | - Learn about Amazon CloudWatch Metrics <br> - Monitor Lambda Invocations, Errors, Duration <br> - Build CloudWatch Dashboard | 28/07/2026 | 28/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html |
| Wednesday | - Create CloudWatch Alarm <br> - Set alert conditions for Lambda errors <br> - Learn about Amazon SNS | 29/07/2026 | 29/07/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| Thursday | - Connect CloudWatch Alarm with Amazon SNS <br> - Configure Email Notification <br> - Test error scenarios | 30/07/2026 | 30/07/2026 | https://docs.aws.amazon.com/sns/latest/dg/welcome.html |
| Friday | - Review IAM Policy and Bucket Policy <br> - Check service access permissions <br> - Learn about AWS KMS <br> - Check data encryption for Amazon S3 | 31/07/2026 | 31/07/2026 | https://docs.aws.amazon.com/kms/latest/developerguide/overview.html |

### Week 6 Achievements:

* Completed the **Monitoring** system for the Image Optimization Pipeline using **Amazon CloudWatch**, helping to track the real-time operational status of system components.

* Standardized the **CloudWatch Logs** content of AWS Lambda, making it easier to track the image processing and supporting error analysis and troubleshooting during incidents.

* Set up monitoring for critical AWS Lambda metrics via **CloudWatch Metrics**, including:

  * Invocations
  * Errors
  * Duration
  * Throttles
  * Success Rate

* Built a **CloudWatch Dashboard** to visualize the system's operational status, making it easy to monitor performance and image processing health.

* Set up **CloudWatch Alarm** to detect instances where Lambda processing fails or generates errors exceeding the allowed threshold.

* Successfully connected **CloudWatch Alarm** with **Amazon SNS**, enabling the system to automatically send email notifications when errors occur during image processing.

* Successfully tested the alert mechanism by simulating error handling scenarios and confirming that emails were sent to the administrator exactly as configured.

* Reviewed and optimized the **IAM Role**, **IAM Policy**, and **S3 Bucket Policy**, ensuring that services are only granted necessary permissions according to the **Least Privilege** principle.

* Researched and applied **AWS Key Management Service (AWS KMS)** to understand data encryption mechanisms on AWS, and tested encryption capabilities for Amazon S3 to enhance data security.

* Fully tested the system's monitoring and alerting flow:

```text
AWS Lambda
      │
      ▼
Amazon CloudWatch Logs
      │
      ▼
CloudWatch Metrics
      │
      ▼
CloudWatch Alarm
      │
      ▼
Amazon SNS
      │
      ▼
Email Notification