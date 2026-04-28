English | [简体中文](./known-limitations_zh-CN.md)

# Known Limitations and Current Scope

This page explains the current release scope of XplorOne.

It is not a roadmap and does not describe future promises.
It is here to help users understand what XplorOne can do today, what is optional, and which boundaries are intentional.

## 1. Current Official Release Line

XplorOne’s current official release line is the desktop application.

At this stage:

- Windows is the current official release line
- the Electron desktop app is the intended end-user release form
- Web preview is for development and internal preview only
- Web preview is not the official end-user release form

If you are evaluating XplorOne as a user, please use the official desktop release rather than the development preview path.

## 2. Core Local Workflow Does Not Require an API Key

XplorOne remains usable without a model API key.

You can use core local features such as:

- local bookkeeping
- Quick Entry
- books, accounts, categories, and transactions
- reports and financial views
- basic local queries
- backup, restore, export, import, and archive workflows where available

A model API key is only required for AI-assisted features.

## 3. AI Features Are Optional

AI is an enhancement layer, not the foundation of the product.

Without an API key, XplorOne can still function as a local-first finance workspace.

If you configure your own API key, AI can help with:

- AI Assistant analysis and interpretation
- broader finance-related chat workflows
- model-assisted interpretation in workflows that explicitly use AI
- entry draft assistance where model participation is enabled

Local Assistant query and entry workflows are designed to remain usable without a model API key where supported by the local kernel.

Current AI boundaries:

- AI does not automatically write to the ledger
- write actions require user confirmation
- model behavior may vary by provider and model
- some natural-language parsing capabilities may continue to improve over time
- users are responsible for choosing and trusting their own model provider

For details, see [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md) and [BYOK Setup](./byok-setup.md).

## 4. Local API and MCP Are Advanced Optional Integrations

Local API and MCP are not required for normal desktop use.

They are intended for advanced local integration and external agent workflows.

Current boundaries:

- Local API and MCP access are token-protected local access paths
- MCP is currently read-only
- MCP does not expose write actions
- MCP queries go through XplorOne’s controlled local API and query layers
- MCP does not directly read the database
- MCP is designed around the current active book scope
- external agents are responsible for interpreting structured results

For ordinary users, local bookkeeping, reports, Quick Entry, and in-app AI workflows do not require MCP.

## 5. XplorOne Is Not a Cloud Accounting Suite

XplorOne is local-first by design.

It is not currently:

- a cloud-first accounting suite
- a browser-first SaaS product
- a hosted multi-user accounting platform
- a real-time cloud collaboration system
- a full enterprise finance system for every team or region

This is an intentional product direction.

XplorOne is designed for users who want a desktop finance workspace with clear local data and AI boundaries.

## 6. No Full Multi-Platform Release Yet

At the current stage, XplorOne should not be described as fully cross-platform.

Current public positioning:

- Windows desktop is the current official release line
- macOS, Linux, mobile, and browser end-user releases should not be assumed available unless explicitly published
- Web preview is not a replacement for the desktop release

If platform support matters to your workflow, please check the current release page before relying on XplorOne.

## 7. Not a Tax, Legal, or Accounting Compliance Service

XplorOne helps users organize, review, and understand financial records.

It is not:

- legal advice
- tax advice
- certified accounting advice
- a country-specific tax filing system
- a substitute for a qualified accountant or tax professional

Users remain responsible for reviewing their own financial decisions and local compliance requirements.

## 8. Import and Export Coverage May Vary

XplorOne includes data control and portability workflows, but users should not assume every external format is supported.

Depending on the current release state, supported workflows may include:

- backup
- restore
- export
- import
- archived book migration
- `.xpl` archive package workflows

Current boundaries:

- not every bank, payment platform, or accounting export format may be supported
- imported data should be reviewed by the user
- archive and export workflows may have scope limits
- moving data between machines may require reconfiguring model API keys or local integration tokens

For privacy and credential boundaries, see [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md).

## 9. Credential Portability Has Boundaries

XplorOne treats model API keys and local integration tokens as sensitive local credentials.

This means:

- model API keys should not be stored as plain text in the ledger database
- MCP client tokens are protected local credentials
- exported ledger files should not expose plain-text credentials
- full-app backup workflows may include protected credential metadata
- protected credential backups may depend on the current machine or operating-system credential environment

If you move XplorOne data to another machine, you may need to reconfigure model API keys or local integration tokens.

## 10. Bilingual UI and AI Behavior Are Still Evolving

XplorOne supports Chinese and English UI work, and bilingual AI behavior is being improved over time.

Current boundaries may include:

- some backend error messages may not be fully localized
- some advanced chart labels or technical messages may still need refinement
- model-generated responses may vary by model provider
- English and Chinese natural-language understanding may not be equally complete across all workflows

If you encounter a language issue, please report it with:

- UI language
- input language
- model provider if AI was involved
- expected output language
- actual output language

## 11. Reports and Charts Have Current Scope

XplorOne includes financial reports and charts, but report coverage should be understood within the current release scope.

Current report areas may include:

- Cash Flow
- Income & Expense
- Assets & Liabilities
- account and category views
- selected charts and trend views

Advanced chart availability or visibility may vary by release channel, product tier, or current product navigation.

XplorOne should not be described as a complete enterprise BI suite.

## 12. Roadmap Items Are Not Current Features

Some features may be discussed in roadmap documents, release notes, or community discussions.

Unless a feature is present in the current release and documented as available, it should not be treated as current functionality.

When in doubt, check:

- [README](../README.md)
- [Feature Overview](./feature-overview.md)
- [Software Release History](./software-release-history.md)
- [Releases](https://github.com/SimonZhangM/XplorOne/releases)

## 13. When These Limitations Matter

If one of these limitations affects your workflow, you can:

- ask a question in [Discussions](https://github.com/SimonZhangM/XplorOne/discussions)
- report a clear bug in [Issues](https://github.com/SimonZhangM/XplorOne/issues)
- check [Releases](https://github.com/SimonZhangM/XplorOne/releases) for current availability
- review [Roadmap](../ROADMAP.md) for direction-level information when available

Please avoid posting private financial data, API keys, local tokens, or screenshots containing sensitive information.

## Where to Go Next

- [Getting Started](./getting-started.md) — complete your first workflow
- [Feature Overview](./feature-overview.md) — understand the main product areas
- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md) — understand data, AI, and integration boundaries
- [BYOK Setup](./byok-setup.md) — configure your own model API key
- [Support](../SUPPORT.md) — learn where to ask questions or report problems
