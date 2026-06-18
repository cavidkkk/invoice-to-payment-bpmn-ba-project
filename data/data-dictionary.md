# Data Dictionary

This data dictionary defines the key fields used in the Invoice-to-Payment process. These fields support invoice capture, validation, approval, posting, payment execution, bank confirmation, reconciliation, and exception handling.

| Field                   | Description                                                                 | Example / Status                                 |
| ----------------------- | --------------------------------------------------------------------------- | ------------------------------------------------ |
| Invoice ID              | Unique identifier assigned to the invoice in the finance system.            | INV-2026-0001                                    |
| Invoice Number          | Invoice number provided by the vendor.                                      | FV/2026/145                                      |
| Vendor ID               | Unique identifier of the vendor in the vendor master data.                  | VND-10045                                        |
| Vendor Name             | Legal or registered name of the supplier.                                   | ABC Logistics Ltd.                               |
| Vendor Status           | Indicates whether the vendor is active, blocked, inactive, or under review. | Active / Blocked                                 |
| PO Number               | Purchase order reference linked to the invoice.                             | PO-2026-7891                                     |
| Goods Receipt Number    | Reference confirming that goods or services were received.                  | GR-2026-334                                      |
| Invoice Amount          | Total amount stated on the invoice.                                         | 12,500.00                                        |
| Currency                | Currency of the invoice amount.                                             | PLN / EUR / USD                                  |
| Tax Amount              | Tax or VAT amount included in the invoice.                                  | 2,875.00                                         |
| Net Amount              | Invoice amount before tax.                                                  | 9,625.00                                         |
| Gross Amount            | Total invoice amount including tax.                                         | 12,500.00                                        |
| Invoice Date            | Date when the invoice was issued by the vendor.                             | 2026-06-16                                       |
| Received Date           | Date when the company received the invoice.                                 | 2026-06-17                                       |
| Due Date                | Date by which payment should be made.                                       | 2026-07-16                                       |
| Payment Terms           | Agreed payment period or condition.                                         | Net 30                                           |
| Invoice Type            | Indicates whether the invoice is PO-based or non-PO-based.                  | PO / Non-PO                                      |
| Match Status            | Result of PO, invoice, and goods receipt matching.                          | Matched / Mismatch                               |
| Exception Reason        | Reason why the invoice was sent to exception handling.                      | Amount mismatch                                  |
| Approval Status         | Status of invoice approval.                                                 | Pending / Approved / Rejected                    |
| Approver ID             | Identifier of the person responsible for approval.                          | APR-102                                          |
| Invoice Status          | Current status of the invoice in the process.                               | Received / Validated / Posted / Paid / Exception |
| Posting Document Number | Accounting document number created after invoice posting.                   | DOC-900456                                       |
| Payment Run ID          | Identifier of the payment run used to process payment.                      | PAYRUN-2026-06-01                                |
| Payment Reference       | Payment transaction reference generated after payment execution.            | PAY-887654                                       |
| Bank Confirmation ID    | Confirmation reference received from the bank or payment provider.          | BANK-CONF-5567                                   |
| Payment Status          | Indicates whether the payment was successful, failed, or pending.           | Successful / Failed / Pending                    |
| Reconciliation Status   | Indicates whether payment and accounting records were matched.              | Matched / Pending / Exception                    |
| Reconciliation Date     | Date when payment reconciliation was completed.                             | 2026-07-18                                       |
| Created By              | User or system that created the invoice record.                             | AP Analyst / OCR System                          |
| Last Updated Date       | Date of the most recent update to the invoice record.                       | 2026-07-18                                       |
| Audit Trail Reference   | Reference used to track actions and decisions in the process.               | AUD-2026-455                                     |

