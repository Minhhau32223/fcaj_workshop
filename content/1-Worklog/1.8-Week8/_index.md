---
title: "Week 8 Worklog"
date: 2026-08-10
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Finalize the **Automatic Image Optimization System on AWS** project.
* Review the components deployed in previous weeks.
* Finalize the architecture diagram and technical documentation.
* Summarize results and prepare presentation content.
* Summarize knowledge and experience after the internship process.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Documentation Source |
| --- | --- | --- | --- | --- |
| Monday | - Review source code <br> - Check project structure <br> - Review AWS resources <br> - Check for remaining errors | 10/08/2026 | 10/08/2026 | Project Documentation |
| Tuesday | - Finalize Architecture Diagram <br> - Review Upload → Processing → Output flow <br> - Update Monitoring and Security flow | 11/08/2026 | 11/08/2026 | AWS Documentation |
| Wednesday | - Finalize README <br> - Finalize Setup Guide <br> - Finalize Deployment Guide <br> - Finalize Testing Guide | 12/08/2026 | 12/08/2026 | Project Documentation |
| Thursday | - Finalize Cleanup Guide <br> - Review AWS resources <br> - Check resources to be deleted after demo | 13/08/2026 | 13/08/2026 | AWS Documentation |
| Friday | - Summarize project results <br> - Prepare presentation <br> - Prepare demo content <br> - Summarize the internship process | 14/08/2026 | 15/08/2026 | Project Documentation |

### Week 8 Achievements:

* Finalized the main components of the **Automatic Image Optimization System on AWS** project deployed in previous weeks.

* Reviewed the entire system architecture and how the components connect with each other:

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