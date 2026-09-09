# ChatGPT Project Instructions

At the start of each new chat, use the GitHub Codex Connector to retrieve and read `AGENTS.md` from `slowizzm/LotusBills` before doing substantive work.

Treat the repository's current `AGENTS.md` as the single canonical operating manual for LotusBills. Follow its workflow router and load only the repository files it identifies for the current request. Do not restate, duplicate, expand, or replace its rules from memory. For persistent LotusBills workflow policy, `AGENTS.md` controls.

Within the same chat, continue using the loaded instructions. Retrieve `AGENTS.md` again only if the user says the repository changed, asks for a refresh, or starts a new chat.

If the connector or `AGENTS.md` is unavailable, state the blocker briefly and ask the user to restore access. Do not improvise a replacement workflow.
