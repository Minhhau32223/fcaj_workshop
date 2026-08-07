---
title: "Week 7 Worklog"
date: 2026-08-03
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Complete the CI/CD pipeline for the project.
* Automate AWS infrastructure deployment using AWS CDK.
* Test the entire system following the End-to-End process.
* Test successful and failed processing scenarios.
* Fix remaining errors before finalizing the project.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Learn about GitHub Actions <br> - Design CI/CD pipeline <br> - Build AWS CDK deployment Workflow | 03/08/2026 | 03/08/2026 | https://docs.github.com/en/actions |
| Tuesday | - Integrate GitHub Actions with AWS CDK <br> - Test CDK Deploy from GitHub Repository <br> - Check deployment status | 04/08/2026 | 04/08/2026 | https://docs.aws.amazon.com/cdk/v2/guide/home.html |
| Wednesday | - Test JPG, PNG, WEBP images <br> - Test with various image sizes <br> - Evaluate Resize and Compression results | 05/08/2026 | 05/08/2026 | https://pillow.readthedocs.io/en/stable/ |
| Thursday | - Test invalid images <br> - Test Lambda Failure <br> - Check FAILED status on DynamoDB <br> - Test CloudWatch Alarm and Amazon SNS | 06/08/2026 | 06/08/2026 | https://docs.aws.amazon.com/ |
| Friday | - Test the entire End-to-End Pipeline <br> - Troubleshoot arising errors <br> - Review IAM Permissions <br> - Final check of the CI/CD Pipeline | 07/08/2026 | 07/08/2026 | https://docs.github.com/en/actions |

### Week 7 Achievements:

* Completed the **CI/CD** pipeline for the project using **GitHub Actions**, helping to automate the AWS infrastructure deployment process after every source code update.

* Successfully built the **GitHub Actions Workflow** with the following steps:
  * Check out source code from the GitHub Repository.
  * Set up the execution environment.
  * Install necessary libraries.
  * Execute **AWS CDK Deploy**.
  * Automatically update AWS infrastructure.

* Successfully tested the automated deployment process:

```text
Git Push
      │
      ▼
GitHub Actions
      │
      ▼
Build & Validate
      │
      ▼
AWS CDK Deploy
      │
      ▼
AWS Infrastructure