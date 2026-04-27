English | [简体中文](./privacy-and-ai-boundaries_zh-CN.md)

# Privacy & AI Boundaries

XplorOne is designed as a local-first desktop finance workspace.

This document explains how XplorOne handles local data, AI participation, model API keys, Local API tokens, MCP tokens, and write boundaries.

It is a product-boundary explanation, not a legal privacy policy.

## 1. Local-First by Default

XplorOne’s official release line is the desktop application.

The core desktop workflow is designed around local application data:

- your books
- accounts
- categories
- transactions
- reports
- budgets
- settings and local configuration metadata

Core financial records are stored in the user’s local application data environment.

XplorOne is not designed around the idea that your financial workflow must begin by uploading your books into a cloud-first system.

## 2. What Works Without an API Key

You do not need a model API key to use XplorOne as a local-first finance workspace.

Without an API key, you can still use core local features such as:

- local bookkeeping
- Quick Entry
- books, accounts, categories, and transactions
- reports and financial views
- basic local queries
- backup, restore, export, import, and archive workflows where available

A model API key is only required for AI-assisted features.

## 3. What Requires an API Key

A user-configured model API key is required only when you want AI-assisted capabilities.

Depending on the enabled workflow, AI-assisted features may include:

- natural-language query interpretation
- entry draft preparation
- financial analysis and explanation
- broader finance-related chat workflows

The API key connects XplorOne to the model service chosen by the user.

XplorOne does not require an API key for ordinary local bookkeeping, reports, financial views, or basic local queries.

## 4. Model API Key Storage

Model API keys are treated as sensitive local credential data.

XplorOne stores model credentials through Electron `safeStorage` or an equivalent system-protected local credential mechanism.

Model API keys are not intended to be stored as plain text in the ledger database.

Non-sensitive model configuration metadata may be stored locally, such as:

- provider name
- base URL
- model name
- enabled status
- configuration state

These metadata fields help XplorOne remember which model configuration should be used, without treating the model key as ordinary ledger data.

Users can remove, replace, or reconfigure their model API key from the application settings.

## 5. Local API and MCP Token Boundaries

XplorOne may use local tokens for local integration paths.

These tokens are different from model API keys.

- **Model API keys** connect XplorOne to the user’s chosen model provider.
- **Local API tokens** protect access to XplorOne’s local HTTP API.
- **MCP client tokens** authorize external agents such as Codex or WorkBuddy to access XplorOne’s local read-only MCP/query path.

Local API and MCP access are intended for local loopback integration.

They are not meant to be treated as public web API credentials.

MCP client tokens are treated as sensitive local credential data and are stored through Electron `safeStorage` or an equivalent system-protected storage mechanism.

Users should not:

- share these tokens
- paste them into public issues
- commit them to GitHub
- send them to third parties
- include them in screenshots or public support messages

If needed, local integration tokens should be removable, resettable, or regenerable from the application settings.

## 6. What Data May Be Sent to Model Providers

Core local features do not require sending data to a model provider.

When AI-assisted features are used, XplorOne may send relevant information to the user-configured model service in order to complete that AI task.

Depending on the workflow, this may include:

- the user’s current question or instruction
- structured financial context needed for the request
- selected report or query context
- entry draft context
- recent conversation context
- AI personalization summary, only if the user has enabled AI personalization

XplorOne aims to send task-relevant context, not the entire local database by default.

Users should choose a model provider they trust and review that provider’s own data and privacy terms.

## 7. Query, Entry, Analysis, and Free Chat Boundaries

XplorOne does not treat every AI interaction as the same type of operation.

### Query

Query workflows are local-first.

Many queries can be resolved directly from local ledger data.
Some queries may use a model to interpret the user’s natural-language request into a structured query.

### Entry

Entry workflows prepare drafts.

AI may help turn a natural-language description into an entry draft, but the draft must be reviewed and confirmed by the user before anything is written.

### Analysis

Analysis workflows may use structured financial context to generate explanations, trends, and suggestions.

This is intended to help users understand their financial data, not to replace user judgment.

### Free Chat

Free chat is for broader finance-related conversations.

It is not the same as direct ledger query.
In the current release line, free chat is not positioned as the default path for direct ledger access.

## 8. AI Write Boundary

AI does not automatically write to the ledger.

Write actions require user confirmation.

This applies especially to:

- transaction creation
- entry draft submission
- any workflow that would change ledger data

XplorOne is designed so that AI can assist with query, interpretation, analysis, and draft preparation, while the user remains responsible for confirming writes.

## 9. Local API and MCP Read-Only Boundary

XplorOne includes local integration capabilities for AI-native workflows.

The current MCP/query path is designed as a token-protected local read-only access path.

Current boundaries:

- MCP access is read-only
- MCP does not expose write actions
- MCP queries go through XplorOne’s controlled local API and query layers
- MCP does not directly read the database
- MCP is designed around the current active book scope
- external agents receive structured query results and are responsible for their own response interpretation

This allows external agents to query relevant financial data while keeping XplorOne’s application boundary intact.

## 10. Backup, Export, and Archive Boundaries

XplorOne includes backup, restore, export, import, and archive workflows depending on the release state.

General boundaries:

- Ledger exports and archive packages are intended to preserve financial data, not expose plain-text credentials.
- Model API keys and MCP tokens should not appear as plain text in exported ledger files.
- Full-app backup workflows may include protected credential metadata for same-machine recovery.
- Protected credential backups are not the same as portable plain-text credential exports.
- Users should still store backups carefully because financial data itself is sensitive.

If you move data between machines, you may need to reconfigure model API keys or local integration tokens depending on the backup type and operating-system credential environment.

## 11. User Responsibilities

XplorOne is local-first, but local-first does not remove all user responsibility.

Users should:

- keep their computer account secure
- protect backups and exported files
- avoid sharing model API keys or local integration tokens
- use trusted model providers
- review provider-specific data policies
- avoid pasting sensitive financial data into public issues
- reset local tokens if they may have been exposed

If you report a bug, please remove private financial data, API keys, tokens, and personal information before posting.

## 12. What XplorOne Is Not

XplorOne is not:

- a cloud-first accounting suite
- a hosted AI finance service where all data is uploaded by default
- an enterprise finance system for every team or region
- a system where AI can automatically mutate your ledger without confirmation
- a public web API service

XplorOne is best understood as a local-first desktop finance workspace with optional AI-assisted features and controlled local integration paths.

## Where to Go Next

- [Getting Started](./getting-started.md) — complete your first workflow
- [Feature Overview](./feature-overview.md) — understand the main product areas
- [BYOK Setup](./byok-setup.md) — configure your own model API key
- [Known Limitations](./known-limitations.md) — understand current release scope
- [Support](../SUPPORT.md) — learn where to ask questions or report problems
