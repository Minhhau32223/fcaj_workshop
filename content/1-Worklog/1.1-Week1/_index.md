title: "Week 1 Worklog"
date: 2026-06-22
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives:

* Understand the requirements and objectives of the **Automatic Image Optimization System on AWS** project.
* Get familiar with Serverless architecture on AWS.
* Research the AWS services to be used in the system.
* Design the overall architecture of the project.
* Set up the development environment and initialize the repository.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Analyze project requirements <br> - Determine system Input/Output <br> - Analyze Upload → Processing → Output flow | 22/06/2026 | 22/06/2026 | Project requirements document |
| Tuesday | - Learn about Serverless architecture on AWS <br>&emsp; + Amazon S3 <br>&emsp; + AWS Lambda <br>&emsp; + Amazon DynamoDB <br>&emsp; + Amazon CloudWatch <br>&emsp; + Amazon SNS <br>&emsp; + AWS IAM | 23/06/2026 | 23/06/2026 | https://docs.aws.amazon.com/ |
| Wednesday | - Learn about Amazon S3 <br>&emsp; + Bucket <br>&emsp; + Object <br>&emsp; + Bucket Policy <br>&emsp; + Event Notification <br> - Research input and output image storage solutions | 24/06/2026 | 24/06/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html |
| Thursday | - Learn about AWS Lambda <br>&emsp; + Function <br>&emsp; + Runtime <br>&emsp; + Handler <br>&emsp; + Execution Role <br> - Research Amazon S3 → AWS Lambda processing flow | 25/06/2026 | 25/06/2026 | https://docs.aws.amazon.com/lambda/latest/dg/welcome.html |
| Friday | - Design system architecture diagram <br> - Initialize GitHub Repository <br> - Initialize AWS CDK project <br> - Install AWS CLI and development environment | 26/06/2026 | 26/06/2026 | https://docs.aws.amazon.com/cdk/api/v2/ |

### Week 1 Achievements:

* Completed understanding the requirements, scope, and objectives of the **Automatic Image Optimization System on AWS** project, and identified the main components to be built in the system.

* Grasped the **Serverless** architecture and the roles of the AWS services to be used, including:
  * Amazon S3
  * AWS Lambda
  * Amazon DynamoDB
  * Amazon CloudWatch
  * Amazon SNS
  * AWS IAM

* Completed the preliminary system architecture design with the following processing flow:

```text
User
  │
  ▼
Amazon S3 (Input Bucket)
  │
  ▼
AWS Lambda
  │
  ├── Amazon S3 (Output Bucket)
  └── Amazon DynamoDB
```

* Successfully initialized the **GitHub Repository** and **AWS CDK** project, creating a foundation for source code management and infrastructure deployment using **Infrastructure as Code (IaC)**.

* Fully set up the development environment, including:
  * Installing Python Virtual Environment.
  * Installing and configuring AWS CLI.
  * Installing AWS CDK.
  * Connecting the AWS account for deployment and testing purposes.

* Developed the project implementation plan, agreed on the overall architecture, and divided tasks among team members.

* Finalized the architecture diagram and initial design documentation as a basis for deploying **Amazon S3**, **AWS Lambda**, and the **Image Processing Pipeline** in the following week.