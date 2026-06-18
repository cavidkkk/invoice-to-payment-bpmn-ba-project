# Python Analysis and Visualizations

This section supports the analytics extension of the Invoice-to-Payment Business Analysis project.

## Python Analysis Folder

The `python-analysis` folder will contain Python scripts for generating synthetic data, validating invoice records, calculating KPIs, and exporting summary outputs.

Planned files:

| File                             | Purpose                                                                                                           |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `generate_synthetic_data.py`     | Creates synthetic Invoice-to-Payment CSV files for portfolio analysis.                                            |
| `invoice_to_payment_analysis.py` | Loads the synthetic dataset, performs validation checks, calculates KPIs, and prepares outputs for visualization. |

Planned checks:

* Missing mandatory invoice fields
* Duplicate invoices
* Blocked vendors
* PO / invoice amount mismatches
* Late payments
* Payment failures
* Reconciliation exceptions
* KPI summary calculations

## Visualizations Folder

The `visualizations` folder will contain charts created from the synthetic dataset and Python analysis.

Planned files:

| File                                 | Purpose                                             |
| ------------------------------------ | --------------------------------------------------- |
| `invoice-status-summary.png`         | Shows invoice status distribution.                  |
| `exception-reasons-summary.png`      | Shows the main reasons for invoice exceptions.      |
| `payment-status-summary.png`         | Shows payment success, failure, and pending status. |
| `reconciliation-status-summary.png`  | Shows reconciliation outcomes.                      |
| `invoice-processing-kpi-summary.png` | Shows selected Invoice-to-Payment process KPIs.     |

## Privacy Note

The analysis will use only synthetic data created for this portfolio project. No real customer, vendor, company, bank, invoice, or transaction data will be used.
