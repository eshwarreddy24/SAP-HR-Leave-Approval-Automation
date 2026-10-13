# Prompts for GitHub Copilot

Open this repository in VS Code with Copilot Chat enabled. Copilot can assist with writing and reviewing **documentation, test plans, synthetic data and code**, but cannot independently prove that an SAP process was configured.

## Prompt 1: Improve the test plan
"Read README.md, diagrams/workflow.md and test-cases.csv. Suggest 8 additional realistic HR leave approval test cases, such as invalid date ranges, empty fields, rejected manager requests and duplicate submissions. Preserve all existing statuses as Not run. Do not invent test results."

## Prompt 2: Validate test files
"Write a small Python 3 standard-library script that validates the CSV headers, unique test IDs and allowed statuses (Not run, Pass, Fail, Blocked). Add usage notes and automated tests. Do not change any test result from Not run."

## Prompt 3: Create synthetic data
"Generate 10 fictional employee records and 15 synthetic leave requests with IDs, manager IDs, types and date ranges. Never use real names, personal identifiers, or actual employer records. Explain any validation assumptions."

## Prompt 4: Review workflow documentation
"Compare the README and Mermaid diagram. Find inconsistencies, untested claims and missing approval/rejection edge cases. Return suggestions only, without claiming SAP deployment."

## Prompt 5: Prepare interview explanation after implementation
"Using only verified build-log entries and actual test results in this repository, draft a 60-second interview description covering problem, approach, controls, tests and limitations. Clearly label unverified items."

## Important
Copilot suggestions must be reviewed manually and tested. Do not merge generated claims that are not supported by actual SAP screenshots or execution evidence.
