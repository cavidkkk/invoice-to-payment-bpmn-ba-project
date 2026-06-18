# Jira-style User Stories

This document contains Jira-style user stories for the Invoice-to-Payment process. The stories describe expected functionality from the perspective of users, systems, and process stakeholders.

## User Story 1 — Capture Invoice Data

**As an AP analyst,**
I want the system to capture invoice details when an invoice is received,
**so that** the invoice can be validated and processed correctly.

### Acceptance Criteria

* Invoice number, vendor ID, amount, currency, invoice date, received date, due date, and PO number can be stored.
* Missing mandatory fields trigger an exception.
* Invoice status changes to Received or Pending Validation after capture.

---

## User Story 2 — Validate Vendor Master Data

**As an AP validation system,**
I want to validate vendor master data,
**so that** invoices from invalid, inactive, or blocked vendors are not posted or paid.

### Acceptance Criteria

* System checks whether vendor exists in vendor master data.
* System checks whether vendor status is active.
* Invalid or blocked vendor creates an exception.
* Exception reason is recorded.

---

## User Story 3 — Check PO Reference

**As an AP validation system,**
I want to check whether a PO-based invoice has a valid purchase order reference,
**so that** invoices can be matched with approved purchasing data.

### Acceptance Criteria

* System identifies whether invoice is PO-based or non-PO-based.
* PO-based invoices require a valid PO number.
* Missing or invalid PO number creates an exception.
* Valid PO reference allows the process to continue to matching.

---

## User Story 4 — Perform PO / Invoice / Goods Receipt Matching

**As an AP validation system,**
I want to match invoice data against purchase order and goods receipt data,
**so that** only accurate invoices continue to approval or posting.

### Acceptance Criteria

* System compares vendor, amount, currency, PO number, and goods receipt data.
* Matching result is stored as Matched, Mismatch, or Pending Review.
* Mismatched invoices are routed to exception handling.
* Matched invoices continue to the next process step.

---

## User Story 5 — Review Invoice Exception

**As an AP analyst,**
I want to review invoice exceptions,
**so that** missing or inconsistent invoice data can be corrected or rejected.

### Acceptance Criteria

* AP analyst can view exception reason.
* AP analyst can add resolution notes.
* AP analyst can send invoice back to validation, route it to approval, or reject it.
* All actions are recorded in the audit trail.

---

## User Story 6 — Approve Invoice

**As a finance approver,**
I want to approve or reject invoices requiring manual approval,
**so that** only authorized invoices move forward to posting and payment.

### Acceptance Criteria

* Finance approver can see invoice details and exception notes.
* Finance approver can approve or reject invoice.
* Rejected invoices require a rejection reason.
* Approval decision, user ID, and timestamp are saved.

---

## User Story 7 — Post Approved Invoice

**As the finance system,**
I want to post approved invoices,
**so that** accounting records are created before payment execution.

### Acceptance Criteria

* Only approved invoices can be posted.
* Posting document number is generated after successful posting.
* Invoice status changes to Posted.
* Posting failure creates an exception.

---

## User Story 8 — Prepare Payment Run

**As a payment and reconciliation user,**
I want approved and due invoices to be included in a payment run,
**so that** payments can be prepared accurately.

### Acceptance Criteria

* Only approved, posted, and due invoices are selected.
* Invoices with Exception, Rejected, or Pending Approval status are excluded.
* Payment run ID is generated.
* Selected invoices are linked to the payment run.

---

## User Story 9 — Send Payment Instruction

**As a payment system,**
I want to send payment instructions to the bank or payment provider,
**so that** approved invoices can be paid.

### Acceptance Criteria

* Payment instruction includes payment amount, currency, vendor bank details, and payment reference.
* Payment reference is generated and stored.
* Payment status changes to Payment Pending.
* Failed instruction transmission creates a payment exception.

---

## User Story 10 — Receive Bank Confirmation

**As a payment system,**
I want to receive payment confirmation or failure response from the bank,
**so that** invoice payment status can be updated.

### Acceptance Criteria

* Bank confirmation ID is stored.
* Successful response updates payment status to Paid.
* Failed response updates payment status to Failed.
* Failed payment creates an exception for review.

---

## User Story 11 — Reconcile Payment

**As a payment and reconciliation user,**
I want to reconcile paid invoices against bank and accounting records,
**so that** payment records are accurate and complete.

### Acceptance Criteria

* System compares payment reference, invoice ID, amount, currency, and bank confirmation.
* Reconciliation status is updated as Matched, Pending, or Exception.
* Matched payments continue to invoice closure.
* Unmatched payments create reconciliation exceptions.

---

## User Story 12 — Close Invoice

**As a finance system,**
I want to close invoices after successful payment and reconciliation,
**so that** the invoice lifecycle is completed.

### Acceptance Criteria

* Invoice can be closed only when payment status is Paid.
* Invoice can be closed only when reconciliation status is Matched.
* Invoice status changes to Closed.
* Closure date is recorded in the audit trail.

## Summary

These Jira-style user stories support the Invoice-to-Payment process by translating process steps and functional requirements into implementation-ready user needs and acceptance criteria.
