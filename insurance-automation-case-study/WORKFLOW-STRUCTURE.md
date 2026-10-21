# Workflow structure — safe technical walkthrough

The following is a **descriptive map** of selected nodes in the uploaded n8n JSON exports, **not** a full executable workflow export. Production node parameters, IDs, endpoints, OAuth references, and embedded PDF assets are intentionally excluded.

## 1. Main workflow — NEW INSURANCE WORKFLOW
- When chat message received / Receive External Workflow Request
- Prepare Webhook Data
- Find Saved Conversation
- Combine New Message and History
- Classify Customer Request
- Intent Router
- White Card Subworkflow
- Ask and Validate Next Quote Question
- Save Customer Answers
- All Quote Details Collected?
- Create Underwriting Summary
- Call TOKEN TRACKING SUB
- Prepare Agent Review Package
- Send to Human Quote Review
- Prepare Customer Status Response

## 2. White Card Sub Workflow
- Execute Workflow Trigger
- Prepare White Card Request
- Ready to Generate?
- Get Policy Record
- Combine Policy Record
- Policy Verified?
- Build White Card PDF
- Send White Card Email
- Customer response / Slack notification

## 3. Insurance Quote Async Review
- Review Request Trigger
- Check Existing Quote
- Quote Already Posted?
- Ignore Duplicate Request / Post Quote to Slack
- Save Thread Reference
- Wait for Agent Review
- Parse Review Decision
- Review Decision Router
- Approval Valid?
- Approved, needs-information and rejected outcome branches

The approval path requires a positive agent-entered rate, agent name and valid email. It does **not** establish binding coverage.

## 4. TOKEN TRACKING SUB
- When Executed by Another Workflow
- Wait
- Receive Token Usage
- Read Token Count
- Format Token Usage
- Insert Row In Data Table
- Code in JavaScript
- Send Slack dashboard

## What a reviewer can evaluate
Control-flow decomposition, stateful dialog, human approval, duplicate handling, data validation and observability.

## What remains private
Embedded code node source, live integration settings, customer records, insurer-specific PDF template images, webhook endpoints, and any sensitive production configuration. A sanitized *importable* sample may be published later, following security review and tests.
