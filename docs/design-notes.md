# Design notes and implementation log

## Scenario
A fictional employee submits a leave request. A manager approves or rejects it. Optionally, HR validates an approved request. This demonstrates administrative controls and ESS/MSS-style workflows.

## Proposed request fields

| Field | Suggested control | Notes |
| --- | --- | --- |
| Employee ID | Required text | Synthetic ID only |
| Employee name | Text | Invented name only |
| Leave type | Dropdown | Annual, casual or sick |
| Start date | Date | Requested first day |
| End date | Date | Requested last day |
| Reason | Optional text | No private medical information |
| Manager decision | Choice | Approve or Reject |
| Manager comments | Text | Reason for decision |

## Build and test log

| Date | Step | Actual outcome | Evidence |
| --- | --- | --- | --- |
| TBD | Access SAP Build trial and Lobby | Not attempted | None |
| TBD | Create process project | Not attempted | None |
| TBD | Create employee form | Not attempted | None |
| TBD | Add manager approval task | Not attempted | None |
| TBD | Configure decision routing | Not attempted | None |
| TBD | Test approve scenario | Not attempted | None |
| TBD | Test reject scenario | Not attempted | None |
| TBD | Configure HR review (optional) | Not attempted | None |

## Environment details (fill in)
- Tenant/service tier:
- SAP Build Process Automation capabilities available:
- Project name and process name:
- Trial restrictions:
- Export / monitoring available:
- Date of tested deployment, if any:

## Security and functional boundary
Use only synthetic employee data and scrub tenant IDs, tokens, email addresses and internal information from public artifacts. Do not claim real SuccessFactors integration, productive SAP HCM access, payroll processing, or deployment into an AAI environment.
