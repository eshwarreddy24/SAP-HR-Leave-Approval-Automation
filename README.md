# SAP HR Leave Approval Workflow Automation

**Status: In progress | SAP workflow not yet implemented or tested**

An HR operations portfolio project exploring employee leave requests, manager decisions, HR review and workflow controls using SAP Build Process Automation.

**Tools planned:** SAP Build Process Automation, SAP BTP trial, GitHub documentation.  
**Business concepts:** Employee Self-Service (ESS), Manager Self-Service (MSS), leave administration, internal controls.

> This is a learning prototype with synthetic data, not an AAI deployment, a classic SAP HCM ESS/MSS implementation or an integration with SAP SuccessFactors. Statuses are updated only after real configuration and tests.

**Engineering extension:** [Enterprise engineering roadmap](docs/enterprise-engineering-roadmap.md) covering idempotent retries, concurrency controls, manager delegation, audit integrity, and observability. All features are planned unless individually verified.

## Business problem and objective
Manual leave requests may involve missing information, unclear ownership and inconsistent routing. The goal is to design and, if trial access permits, configure a structured approval process, test the different decisions, and document the outcome.

## Planned workflow
1. Employee completes a leave form with employee ID, leave type and dates.
2. A manager reviews the request and chooses Approve or Reject.
3. An approved request proceeds to HR validation **if this step is supported and implemented**.
4. A rejected request follows a rejection path.
5. Actual execution evidence is captured where monitoring or testing is available.

[View proposed workflow diagram](diagrams/workflow.md)

## Implementation status

| Capability | Status | Evidence |
| --- | --- | --- |
| SAP Build trial / Lobby access | Not confirmed | Pending |
| Employee leave request form | Planned | Pending |
| Manager approval/rejection | Planned | Pending |
| Conditional routing | Planned | Pending |
| HR review step | Optional, not implemented | Pending |
| Successful approval scenario | Not tested | Pending |
| Rejected request scenario | Not tested | Pending |
| SAP project export | Not confirmed available | Pending |
| SAP SuccessFactors HR811 | Unavailable when checked (maintenance) | [Practice log](docs/hr811-practice.md) |

## Planned SAP artifacts

| Artifact | Purpose |
| --- | --- |
| Employee request form | Collect synthetic employee and leave data |
| Human approval task | Capture manager decision |
| Process condition | Route request according to decision |
| HR verification task (optional) | Review approved request |
| Process test evidence | Document actual path and result |

See [design notes and build log](docs/design-notes.md).

## Test plan and evidence
- [Test cases](test-cases.csv) list expected results. All cases are currently **Not run**.
- [Screenshot guidelines](screenshots/README.md) explain what evidence to capture when available.
- [Resume language](docs/resume-entry.md) must be updated only after implementation and testing.
- [Copilot prompts](docs/copilot-prompts.md) can help improve documentation and test design.

## Scope and limitations
- The trial may restrict access, deployment, task configuration, monitoring or export.
- This project does not assume any live employee database, leave-balance integration or payroll automation.
- HR811 SuccessFactors practice is documented separately, not claimed as technically connected to SAP Build.
- Screenshots and any sample employee records must exclude real personal and confidential data.

## How to reproduce
The repository is documentation-first until a real SAP workflow is built. Follow [design notes](docs/design-notes.md), [workflow](diagrams/workflow.md) and [test plan](test-cases.csv). Any actual SAP export or implementation instructions will be added after the SAP trial supports them.

## Official references
- [SAP Build Process Automation](https://help.sap.com/docs/build-process-automation)
- [SAP Build developer tutorials](https://developers.sap.com/topics/process-automation.html)
- [SAP Learning practice systems](https://learning.sap.com/practice-systems)

**Repository owner:** [eshwarreddy24](https://github.com/eshwarreddy24)
