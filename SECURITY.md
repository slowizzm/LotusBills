# Data and Security Rules

## Repository boundary

This repository stores instructions and empty schemas only. Do not commit personal or business financial source data, even when the repository is private.

Prohibited repository content includes:

- Bills, statements, invoices, receipts, and provider correspondence.
- Excel, CSV, TSV, PDF, image, or OCR files containing real financial data.
- Bank or card exports and transaction histories.
- Names paired with addresses, account numbers, barcodes, QR codes, or other identifiers.
- Credentials, cookies, tokens, API keys, one-time codes, PINs, or security answers.
- Generated reports that reproduce personal financial details.

## Approved source locations

Use only a source the user explicitly selected for the current task:

- Files attached to the ChatGPT conversation or Project.

The GitHub Codex Connector is for reading LotusBills instructions and supporting repository files. Do not use GitHub to store or retrieve real financial source documents.

Authorization to review one file does not authorize reviewing unrelated files already present in the Project.

## Artifact rules

- Preserve originals unchanged.
- Create derived work in a new file.
- Redact sensitive identifiers by default.
- Include only the minimum source detail needed to support a finding.
- Do not embed source documents inside generated workbooks or reports.
- Before sharing or exporting, inspect the output for hidden sheets, comments, metadata, formulas, links, and copied source fields that may expose sensitive data.

## Action boundary

This project never initiates or confirms payments, transfers, purchases, account changes, subscriptions, cancellations, provider communications, or binding submissions.
