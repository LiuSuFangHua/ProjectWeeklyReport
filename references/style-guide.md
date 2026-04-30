# Weekly Report Style Guide

## Output Standards

### File Naming
- Markdown: `项目周报_YYYYMMDD-YYYYMMDD.md`
- Excel: `项目周报_YYYYMMDD-YYYYMMDD.xlsx`

### Report Structure
1. **Report Header**
   - Report period
   - Overall statistics

2. **Per-Project Section** (for each project)
   - Project Information
   - Key Progress This Week
   - Task Completion Status
   - Personnel Statistics
   - Risks and Issues
   - Next Week Plan

3. **Overall Summary**
   - Achievements (3 items)
   - Key Issues (2 items)
   - Improvement Suggestions (2 items)

## Content Requirements

### Core Progress
- Must be quantifiable
- Include hours spent and progress percentage
- Avoid vague statements like "in progress"

### Risk Description
- Include scenario + impact + reason
- Response measures must be actionable

### Format Rules
- Use Chinese numerals for project sections (一、二、三...)
- Use Arabic numerals for sub-items
- Tables must have headers
- Empty data should display "本期无数据" instead of empty cells

## Validation Rules

### cURL Validation
- Must contain Authorization header
- Must contain tenantId header
- Must contain --data-raw parameter
- Must contain required body fields: status, currentPage, pageSize

### Date Validation
- Format: YYYYMMDD-YYYYMMDD
- Start date ≤ end date
- Must be valid Gregorian dates
- Cannot exceed 1 year in the future

### Data Consistency
- Project name must match between Excel and Markdown
- Person statistics must be deduplicated
- Completion rate = completed tasks / total tasks × 100%