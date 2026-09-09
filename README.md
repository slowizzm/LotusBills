# LotusBills

A source-backed operating system for reviewing bills and financial spreadsheets with ChatGPT or Codex.

The system is intentionally advisory. It can extract, reconcile, audit, compare, explain, and recommend. It cannot pay bills, move money, contact providers, change services, or execute recommendations.

## Recommended architecture

- **GitHub repository:** durable instructions, schemas, and empty templates.
- **ChatGPT Project:** ongoing conversation, context, and user-facing review workflow.
- **Built-in Spreadsheet and PDF capabilities:** Excel/CSV analysis and statement extraction.
- **Optional storage connector:** use only the connector that already holds the source files.
- **Sensitive financial files:** attach to the Project/chat or retrieve from an explicitly authorized storage source. Never commit them to this repository.

## Start here

1. Private visibility is recommended. Regardless of visibility, keep all real financial data out of GitHub.
2. Connect it to the ChatGPT Project through GitHub.
3. Paste the contents of `PROJECT_INSTRUCTIONS.md` into the Project instructions.
4. Attach or authorize only the workbook and bill files needed for the current review.
5. Start with one of the prompts in `docs/STARTER_PROMPTS.md`.

Codex reads the root `AGENTS.md` automatically when working in the repository. A standard ChatGPT Project chat should be told to retrieve it explicitly, which is handled by `PROJECT_INSTRUCTIONS.md`.

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
