# AI Lead Qualification CRM & Notification Automation

An AI-assisted lead qualification and CRM automation workflow built with **n8n, JavaScript, Google Sheets, and Gmail**.

This portfolio project demonstrates how business leads can be automatically validated, analyzed, scored, prioritized, stored in a CRM-style Google Sheet, and routed for follow-up.

## Workflow

```text
Lead Input
    ↓
Lead Validation
    ↓
Lead Analysis
    ↓
Score Calculation
    ↓
Priority Classification
    ↓
Recommended Action
    ↓
Duplicate Check
    ↓
Google Sheets CRM
    ↓
Email Notification
```

## Key Features

* Lead data validation
* Automated lead analysis
* Qualification scoring
* High, Medium, and Low priority classification
* Recommended follow-up action
* Duplicate detection using Lead ID
* Existing lead update
* New lead creation
* Google Sheets CRM integration
* Priority-based Gmail notifications

## Qualification Scoring

| Factor                       |   Score |
| ---------------------------- | ------: |
| Clear requirement            |      20 |
| Defined budget               |      15 |
| Urgent requirement           |      15 |
| High purchase intent         |      20 |
| Suitable service             |      20 |
| Complete contact information |      10 |
| **Maximum**                  | **100** |

### Priority Levels

* **80–100:** High Priority
* **60–79:** Medium Priority
* **40–59:** Low Priority
* **Below 40:** Nurture / Review

## CRM Logic

The workflow uses `lead_id` as the unique identifier.

When a lead is received:

1. Check whether the Lead ID already exists.
2. Update the existing record if found.
3. Append a new record if it does not exist.
4. Route the lead according to its priority.

This prevents repeated executions from unnecessarily creating duplicate CRM records.

## Test Results

| Lead ID | Score | Priority        | CRM Result | Notification          |
| ------- | ----: | --------------- | ---------- | --------------------- |
| L011    |    85 | High Priority   | Updated    | High Priority email   |
| L012    |    45 | Low Priority    | Updated    | No email              |
| L013    |    70 | Medium Priority | Added      | Medium Priority email |

These are controlled demonstration leads used to test the workflow.

## Technologies

* **n8n** — Workflow automation
* **JavaScript** — Qualification and routing logic
* **Google Sheets** — CRM-style storage
* **Gmail** — Email notifications

## What This Demonstrates

* Business process automation
* Workflow design
* Conditional logic
* Data validation and transformation
* CRM automation
* Google Workspace integration
* Email automation
* Duplicate prevention
* Debugging and data mapping

## Project Scope

This is a **portfolio proof-of-concept**, not a production CRM.

The workflow demonstrates practical automation capabilities that can be extended to website forms, AI/LLM qualification, databases, dashboards, and other CRM integrations.

## Author

**Obulisivananthan V R**

AI Automation | GenAI Applications | n8n Workflows | Python
