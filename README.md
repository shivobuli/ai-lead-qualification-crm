# AI Lead Qualification CRM & Notification Automation

An AI-assisted lead qualification and CRM automation workflow built with **n8n, JavaScript, Google Sheets, and Gmail**.

This project demonstrates how incoming business leads can be automatically validated, analyzed, scored, prioritized, recorded in a CRM-style Google Sheet, and routed for follow-up.

## Project Overview

The workflow automates the initial lead qualification process so that sales teams can quickly identify leads that may require immediate attention.

### Workflow

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
Priority-based Email Notification
```

## Key Features

* Lead data validation
* Rule-based AI-assisted lead analysis
* Automated qualification scoring
* High, Medium, and Low priority classification
* Recommended follow-up action
* Duplicate lead detection using Lead ID
* Existing lead record update
* New lead record creation
* Google Sheets CRM integration
* High Priority email notification
* Medium Priority email notification
* Low Priority leads retained without unnecessary email alerts
* JavaScript-based workflow logic

## Qualification Scoring

The workflow evaluates six qualification factors:

| Qualification factor         |   Score |
| ---------------------------- | ------: |
| Clear requirement            |      20 |
| Defined budget               |      15 |
| Urgent requirement           |      15 |
| High purchase intent         |      20 |
| Suitable service             |      20 |
| Complete contact information |      10 |
| **Maximum score**            | **100** |

Priority levels:

* **80–100:** High Priority
* **60–79:** Medium Priority
* **40–59:** Low Priority
* **Below 40:** Nurture / Review

## CRM Logic

The workflow uses `lead_id` as the unique identifier.

When a lead is received:

1. The workflow checks whether the Lead ID already exists.
2. If the lead exists, the existing Google Sheets record is updated.
3. If the lead is new, a new CRM record is created.
4. The result is then routed according to lead priority.

This prevents repeated workflow executions from unnecessarily creating duplicate CRM records.

## Example Test Results

| Lead ID | Score | Priority        | CRM Result | Notification          |
| ------- | ----: | --------------- | ---------- | --------------------- |
| L011    |    85 | High Priority   | Updated    | High Priority email   |
| L012    |    45 | Low Priority    | Updated    | No email              |
| L013    |    70 | Medium Priority | Added      | Medium Priority email |

These are controlled demonstration leads used to test the workflow.

## Technologies

* **n8n** — Workflow automation
* **JavaScript** — Qualification and routing logic
* **Google Sheets** — CRM-style lead storage
* **Gmail** — Automated notifications

## What This Project Demonstrates

This project demonstrates practical experience with:

* Workflow automation
* Business process automation
* Conditional logic
* Data validation
* Data transformation
* CRM automation
* Google Workspace integrations
* Email automation
* Duplicate prevention
* Debugging and data mapping
* Building practical AI-assisted business workflows

## Project Scope

This is a **portf**
