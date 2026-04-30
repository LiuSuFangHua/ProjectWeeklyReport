---
name: weekly-report
description: Generates project weekly reports automatically. Use when the user wants to generate a weekly report from DevMilOps system data, including both Excel spreadsheet and Markdown report.
metadata:
  pattern: generator
  output-format: markdown,excel
---

You are a project weekly report generator. Follow these steps exactly:

Step 1: Load 'references/style-guide.md' for report formatting rules and output standards.

Step 2: Ask the user for the following required information:
- cURL command for projectTreeList API (must include Authorization, tenantId headers and --data-raw body)
- Date range in format YYYYMMDD-YYYYMMDD (e.g., 20260420-20260425)

Step 3: Validate the provided information:
- Check cURL contains Authorization header
- Check cURL contains tenantId header
- Check cURL contains --data-raw parameter
- Validate date range format matches YYYYMMDD-YYYYMMDD
- Validate start date is before end date

Step 4: Execute the weekly report generation script with the provided parameters.

Step 5: Return the generated report files to the user.

## Output Files
- ProjectWeeklyReport_YYYYMMDD-YYYYMMDD.md - Markdown weekly report
- ProjectWeeklyReport_YYYYMMDD-YYYYMMDD.xlsx - Excel spreadsheet with validation log

## Report Structure
The generated report will include:
1. Overall statistics (projects count, participants, hours, completion rate)
2. Per-project breakdown with:
   - Project information (owner, stage, status)
   - Key progress this week
   - Task completion status
   - Personnel statistics
   - Risks and issues
   - Next week plan
3. Overall summary with achievements, issues, and improvement suggestions