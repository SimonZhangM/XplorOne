English | [简体中文](./local-api-and-mcp_zh-CN.md)

# Local API and MCP

This document explains XplorOne's local integration path for external agents and tools.

It is intended for users who want to understand how Local API and MCP differ from the in-app assistants.

## What MCP Means Here

MCP stands for Model Context Protocol.

In XplorOne, MCP is used as an optional local integration path so external agent tools can query structured finance information through XplorOne's controlled local interface.

The current public boundary is:

- local
- token-protected
- read-only
- scoped around the current active book
- routed through XplorOne's Local API and query layers
- not direct database access

## How It Differs From In-App AI

XplorOne has in-app assistants and local integration paths.

They are related, but not the same thing.

| Area | In-app Local Assistant | In-app AI Assistant | Local API / MCP |
|---|---|---|---|
| Main use | local query and entry workflows | analysis and broader finance conversation | external agent read-only query |
| Model required | no for supported local flows | yes for AI workflows | external client may use its own model |
| Write access | drafts require confirmation | writes require confirmation | current MCP path is read-only |
| Scope | current app workflow | current app workflow | current active book query path |
| Database access | through app services | through app services and selected context | through controlled Local API/query layers |

## What External Agents Can Do

External tools such as Codex, WorkBuddy, or similar agent clients may use the read-only MCP/query path to ask questions like:

- show this month's highest expense categories
- summarize recent income and expense patterns
- list budget categories that are over plan
- inspect recent cash-flow movement
- compare selected periods using structured results

The external agent receives structured results from XplorOne and is responsible for its own interpretation or response.

## What It Should Not Be Used For

The current Local API / MCP path should not be treated as:

- an automatic bookkeeping writer
- a delete or edit tool
- a direct SQLite reader
- a public web API
- a hosted service for other users
- an accounting, tax, audit, or legal decision engine
- a way to bypass XplorOne's write-confirmation boundaries

## Tokens and Local Access

Local API and MCP access are protected by local tokens.

Token-related boundaries:

- Local API tokens protect local HTTP access.
- MCP client tokens authorize external agent clients.
- Tokens should be treated as secrets.
- Tokens should not be pasted into public issues, logs, screenshots, or shared prompts.
- Tokens should be removable, resettable, or regenerable from application settings where supported.

MCP client tokens are treated as protected local credentials and are intended to be stored through Electron `safeStorage` or an equivalent system-protected local mechanism where available.

## Active Book Scope

The current MCP/query path is designed around the active book context.

Users should not assume that MCP can query every archived book, every backup, or every account outside the active application scope.

If a question depends on a specific book, open or activate the relevant book in XplorOne first.

## Privacy and Safety Notes

Read-only does not mean non-sensitive.

Query results may still contain private financial information. Do not paste MCP output into public issues or third-party systems unless it is redacted.

For broader privacy details, see:

- [Privacy](../PRIVACY.md)
- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md)
- [Security](../SECURITY.md)

