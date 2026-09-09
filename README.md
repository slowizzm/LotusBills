# LotusBills

A source-backed operating system for reviewing bills and financial spreadsheets in a ChatGPT Project.

The system is intentionally advisory. It can extract, reconcile, audit, compare, explain, and recommend. It cannot pay bills, move money, contact providers, change services, or execute recommendations.

## Recommended architecture

- **GitHub repository:** durable instructions, schemas, and empty templates.
- **ChatGPT Project:** ongoing conversation, uploaded source files, and user-facing review workflow.
- **GitHub Codex Connector:** read access to the repository's canonical instructions and supporting files.
- **Built-in Spreadsheet and PDF capabilities:** Excel/CSV analysis and statement extraction.
- **Sensitive financial files:** upload them to the Project or attach them to the current chat. Never commit them to this repository.

## Start here

1. Private visibility is recommended. Regardless of visibility, keep all real financial data out of GitHub.
2. Enable the GitHub Codex Connector for the ChatGPT Project and allow access to `slowizzm/LotusBills`.
3. Paste the contents of `PROJECT_INSTRUCTIONS.md` into the Project instructions.
4. Attach or authorize only the workbook and bill files needed for the current review.
5. Start with one of the prompts in `docs/STARTER_PROMPTS.md`.

`PROJECT_INSTRUCTIONS.md` tells each new Project chat to retrieve `AGENTS.md` through the connector. After that bootstrap, `AGENTS.md` controls the workflow and routes to any supporting repository files.

## Repository map

- `AGENTS.md` — canonical orchestration and guardrails.
- `PROJECT_INSTRUCTIONS.md` — copy/paste bridge for a ChatGPT Project.
- `docs/WORKFLOWS.md` — task procedures.
- `docs/OUTPUT_CONTRACT.md` — required reporting structure.
- `docs/STARTER_PROMPTS.md` — concise prompts for common reviews.
- `schemas/bill-record.schema.json` — normalized bill data contract.
- `SECURITY.md` — privacy and source-file rules.

## What stays out of GitHub

Bills, statements, spreadsheets containing real financial data, bank/card exports, account details, screenshots, OCR output, generated personal reports, credentials, and provider correspondence.
