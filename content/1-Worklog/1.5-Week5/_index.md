---
title: "Week 5 Worklog"
date: 2026-07-20
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Learn about Event-driven architecture on AWS.
* Deploy Amazon EventBridge into the system.
* Connect events from Amazon S3 to AWS Lambda.
* Integrate EventBridge with the Image Processing Pipeline.
* Complete the image processing architecture based on the Event-driven model.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Learn about Event-driven architecture <br> - Learn about Amazon EventBridge <br> - Research Event Bus, Rule, and Target | 20/07/2026 | 20/07/2026 | https://docs.aws.amazon.com/eventbridge/latest/userguide/what-is-amazon-eventbridge.html |
| Tuesday | - Build EventBridge Rule <br> - Set up Event Pattern for S3 Object Created event <br> - Analyze Event Payload structure | 21/07/2026 | 21/07/2026 | https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-patterns.html |
| Wednesday | - Connect Amazon S3 with EventBridge <br> - Connect EventBridge with Image Processing Lambda <br> - Test Event Payload | 22/07/2026 | 22/07/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventBridge.html |
| Thursday | - Adjust Image Processing Lambda to handle EventBridge Event <br> - Test with multiple image types <br> - Check for duplicate processing cases | 23/07/2026 | 23/07/2026 | https://docs.aws.amazon.com/lambda/latest/dg/with-eventbridge.html |
| Friday | - Deploy EventBridge using AWS CDK <br> - Test the entire pipeline <br> - Troubleshoot errors arising during event processing | 24/07/2026 | 24/07/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |

### Week 5 Achievements:

* Understood the operating principles of **Event-driven Architecture** and how to apply this model to the image processing system on AWS.

* Successfully researched and deployed **Amazon EventBridge** as an event orchestration intermediary between AWS services, helping to reduce direct dependency between Amazon S3 and AWS Lambda.

* Successfully built and configured the **EventBridge Rule** to listen for the **Object Created** event from Amazon S3.

* Completed the connection between **Amazon S3**, **Amazon EventBridge**, and **AWS Lambda**, ensuring Lambda is triggered automatically when a new image is uploaded to the Input Bucket.

* Adjusted the Image Processing Lambda to receive and process data in the EventBridge Event format, while verifying the accuracy of the Event Payload.

* Deployed the EventBridge infrastructure using **AWS CDK**, helping infrastructure management and deployment stay synchronized with previously built components.

* Successfully tested the entire image processing flow following the Event-driven model:

```text
User
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
      └── Save Metadata
      │
      ▼
Amazon S3 (Output Bucket)
      │
      ▼
Amazon DynamoDB