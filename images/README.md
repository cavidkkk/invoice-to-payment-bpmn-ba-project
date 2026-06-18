# Images

This folder contains visual exports of the Invoice-to-Payment BPMN 2.0 process model.

The full overview image shows the complete process, while the zoomed images split the model into readable sections for GitHub, LinkedIn, and portfolio presentation use.

## Files Included

| File | Description |
|---|---|
| `bpmn-overview.png` | Full BPMN 2.0 model overview showing the complete Invoice-to-Payment process across Vendor, Procurement, Finance / Accounts Payable, and Bank / Payment Provider pools. |
| `bpmn-zoom-01-invoice-submission-receipt.png` | Invoice submission and receipt: vendor sends invoice, invoice is received, readability is checked, and missing/corrected information can be requested. |
| `bpmn-zoom-02-data-validation-vendor-check.png` | Data validation and vendor check: mandatory fields are validated, vendor master data is checked, and missing information or vendor exceptions are handled. |
| `bpmn-zoom-03-po-matching-exception-review.png` | PO matching and exception review: PO availability is checked, PO / goods receipt / invoice matching is performed, and vendor or PO exceptions are reviewed. |
| `bpmn-zoom-04-approval-posting-rejection.png` | Approval, posting and rejection handling: resolved invoices move to posting or approval, while rejected invoices are updated and notifications are sent. |
| `bpmn-zoom-05-payment-execution-bank-response.png` | Payment execution and bank response: invoices are scheduled for payment, payment runs are executed, payment instructions are sent, and bank authorization response is received. |
| `bpmn-zoom-06-reconciliation-closure.png` | Reconciliation and closure: payment status is updated, payments are reconciled, invoices are closed, or reconciliation exceptions are created. |

## Usage

Use `bpmn-overview.png` as the main visual overview in the repository README or portfolio deck.

Use the zoomed images to explain the process step by step:

1. Invoice submission and receipt
2. Data validation and vendor check
3. PO matching and exception review
4. Approval, posting and rejection handling
5. Payment execution and bank response
6. Reconciliation and invoice closure

## Source

These images are generated from the BPMN 2.0 model export for the Invoice-to-Payment Business Analysis portfolio project.
