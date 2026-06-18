# Invoice-to-Payment Process — BPMN 2.0 Business Analysis Portfolio Project

## Project Summary

This project presents an anonymized Business Analyst portfolio case study focused on an Invoice-to-Payment process.

The process models how a vendor invoice moves from invoice submission to invoice receipt, invoice data capture, vendor validation, purchase order matching, exception handling, approval, invoice posting, payment execution, bank confirmation, reconciliation, and final invoice closure.

The project demonstrates how BPMN 2.0 process modeling can be connected with business requirements, functional requirements, business rules, data properties, KPIs, risks, controls, and Jira-style user stories.

## Business Context

Invoice-to-Payment is a critical finance process because it controls how supplier invoices are received, checked, approved, paid, and reconciled.

If this process is not clearly structured, a company may face duplicate payments, delayed payments, incorrect vendor records, approval bottlenecks, invoice mismatches, missing audit trails, and reconciliation issues.

This project shows how a Business Analyst can map the process, define requirements, identify decision points, and document controls to support better process visibility and operational efficiency.

## Project Objective

The objective of this project is to design a clear and structured Invoice-to-Payment process model using BPMN 2.0 and support it with Business Analysis documentation.

The project aims to:

* Clarify responsibilities between Vendor, Procurement, Finance / Accounts Payable, and Bank / Payment Provider
* Show the end-to-end invoice lifecycle
* Identify key validation and approval points
* Define business and functional requirements
* Document business rules and data fields
* Highlight risks, controls, and KPIs
* Demonstrate practical Business Analyst documentation skills

## Project Scope

### In Scope

* Vendor invoice submission
* Invoice receipt and data capture
* Vendor master data validation
* Purchase order reference check
* PO / invoice / goods receipt matching
* Invoice exception handling
* Finance approval workflow
* Invoice posting
* Payment run preparation
* Payment execution
* Bank confirmation
* Payment reconciliation
* Invoice closure

### Out of Scope

* Vendor onboarding
* Contract negotiation
* Tax reporting
* Full ERP implementation
* Dispute litigation
* Advanced cash forecasting
* Supplier performance management

## Stakeholders

| Stakeholder                   | Responsibility                                                                    |
| ----------------------------- | --------------------------------------------------------------------------------- |
| Vendor                        | Sends invoice and receives payment confirmation.                                  |
| Procurement Department        | Supports PO validation and exception clarification.                               |
| Invoice Processing Team       | Receives invoice, captures invoice data, and handles initial checks.              |
| AP Validation System / SAP    | Performs vendor validation, PO matching, posting, and payment status updates.     |
| Finance Approver              | Reviews and approves invoice exceptions or approval-required invoices.            |
| Payment & Reconciliation Team | Runs payment, receives bank confirmation, reconciles payment, and closes invoice. |
| Bank / Payment Provider       | Processes payment instruction and sends payment confirmation or failure response. |

## BPMN Model Overview

The BPMN 2.0 model includes multiple pools, internal lanes, typed BPMN tasks, gateways, message flows, exception paths, and end states.

### Pools

* Vendor
* Procurement Department
* Finance / Accounts Payable
* Bank / Payment Provider

### Lanes inside Finance / Accounts Payable

* Invoice Processing Team
* AP Validation System / SAP
* Finance Approver
* Payment & Reconciliation Team

## BPMN Task Types Used

| BPMN Task Type     | Example in Process                                                 |
| ------------------ | ------------------------------------------------------------------ |
| Send Task          | Vendor sends invoice; payment instruction sent to bank.            |
| Receive Task       | Finance receives invoice; system receives bank confirmation.       |
| Service Task       | System validates vendor, checks PO, posts invoice, updates status. |
| User Task          | Finance approver reviews invoice exception.                        |
| Business Rule Task | System applies matching and approval rules.                        |
| Manual Task        | Reconciliation team investigates unmatched payment.                |

## Main Decision Gateways

| Gateway                               | Purpose                                                             |
| ------------------------------------- | ------------------------------------------------------------------- |
| Vendor valid?                         | Checks whether vendor exists and is active in vendor master data.   |
| PO available?                         | Checks whether invoice has a purchase order reference.              |
| PO / invoice / goods receipt matched? | Checks whether invoice details match purchasing and receiving data. |
| Approval required?                    | Determines whether invoice needs manual approval.                   |
| Invoice approved?                     | Confirms whether approver accepts or rejects the invoice.           |
| Payment successful?                   | Checks whether bank/payment provider completed the payment.         |
| Reconciliation matched?               | Checks whether payment and accounting records match.                |

## Key Deliverables

This project includes:

* BPMN 2.0 process model
* Business Requirements Document
* Functional Requirements Document
* Business requirements
* Functional requirements
* Business rules
* Data dictionary
* Risks, controls, and KPIs
* Jira-style user stories
* Portfolio presentation structure

## Business Analysis Skills Demonstrated

* BPMN 2.0 process modeling
* Business process analysis
* Requirements documentation
* BRD and FRD preparation
* Stakeholder responsibility mapping
* Functional requirement writing
* Business rule definition
* Data dictionary preparation
* Risk and control identification
* KPI definition
* Jira-style user story writing
* Finance process understanding

## Disclaimer

This is an anonymized portfolio project created for demonstration purposes. It does not include confidential company data or internal documentation from any employer.
