English | [简体中文](./faq_zh-CN.md)

# Frequently Asked Questions

This FAQ answers common questions about XplorOne’s release scope, local-first design, AI features, API keys, MCP, data boundaries, and support.

## 1. What is XplorOne?

XplorOne is a local-first AI finance workspace for solopreneurs, freelancers, one-person businesses, consultants, indie makers, and small studios.

It helps users record financial activity, review accounts and reports, understand cash flow, and optionally use AI-assisted query, entry drafts, and analysis.

## 2. Who is XplorOne for?

XplorOne is designed for people who manage their own financial workflow, such as:

- freelancers
- consultants
- indie makers
- small studio owners
- one-person businesses
- users who care about local-first financial visibility

It is not designed as a full enterprise accounting system for every team, country, or compliance scenario.

## 3. Is XplorOne a normal bookkeeping app?

Not exactly.

XplorOne includes bookkeeping features, but it is positioned as a finance workspace.

The goal is not only to record transactions, but also to help users understand:

- cash flow
- income and expenses
- assets and liabilities
- account structure
- category structure
- financial patterns over time

## 4. What is the current official release line?

The current official release line is the Windows desktop application.

The desktop app is the intended end-user release form.

Web preview is for development and internal preview only. It is not the official end-user release form.

## 5. Does XplorOne require an API key to use?

No.

XplorOne can be used without a model API key.

Without an API key, you can still use core local features such as:

- local bookkeeping
- Quick Entry
- books, accounts, categories, and transactions
- reports and financial views
- basic local queries
- backup, restore, export, import, and archive workflows where available

A model API key is only required for optional AI-assisted features.

## 6. What are AI-assisted features?

AI-assisted features may include:

- AI Assistant analysis and explanation
- broader finance-related chat workflows
- model-assisted interpretation in workflows that explicitly use AI
- entry draft assistance where model participation is enabled

AI is an enhancement layer, not the foundation of the product.

## 7. Can AI automatically write to my ledger?

No.

AI does not automatically write to the ledger.

Write actions require user confirmation.

This applies especially to:

- transaction creation
- entry draft submission
- workflows that would change ledger data

XplorOne is designed so that Local Assistant can help with supported local query and entry workflows, while AI Assistant can help with analysis and broader finance-related conversation.

The user remains responsible for confirming writes.

## 8. Is my financial data uploaded to the cloud by default?

No.

XplorOne is designed as a local-first desktop finance workspace.

Core financial records are stored in the user’s local application data environment.

However, when you use AI-assisted features, XplorOne may send task-relevant context to the model service configured by the user in order to complete that AI task.

## 9. What data may be sent to a model provider?

When AI-assisted features are used, XplorOne may send relevant information needed for that task.

Depending on the workflow, this may include:

- the user’s current question or instruction
- structured financial context needed for the request
- selected report or query context
- entry draft context
- recent conversation context
- AI personalization summary, only if enabled by the user

XplorOne aims to send task-relevant context, not the entire local database by default.

Users should choose a model provider they trust and review that provider’s own data and privacy terms.

## 10. How is my model API key stored?

Model API keys are treated as sensitive local credential data.

XplorOne stores model credentials through Electron `safeStorage` or an equivalent system-protected local credential mechanism.

Model API keys are not intended to be stored as plain text in the ledger database.

For details, see [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md).

## 11. What is BYOK?

BYOK means **Bring Your Own Key**.

In XplorOne, it means you can connect the app to a model service using your own model API key.

BYOK does not mean XplorOne requires AI to be useful.
It only means optional AI-assisted workflows can use the model provider you configure.

For setup details, see [BYOK Setup](./byok-setup.md).

## 12. Are model API keys and MCP tokens the same thing?

No.

They are different credential types:

- **Model API key** connects XplorOne to the model service chosen by the user.
- **Local API token** protects access to XplorOne’s local HTTP API.
- **MCP client token** authorizes external agents such as Codex or WorkBuddy to access XplorOne’s local read-only MCP/query path.

BYOK setup is only about model API keys.

Local API and MCP tokens are managed separately and are not required for normal desktop use.

## 13. What is the difference between Local Assistant and AI Assistant?

Local Assistant handles fast local query and entry workflows.

AI Assistant handles analysis and broader finance-related conversation.

Supported Local Assistant flows do not silently fall back to AI guessing, while AI Assistant uses the user-configured model service when AI capabilities are needed.

## 14. What is MCP in XplorOne?

MCP is an optional local integration path for external agent workflows.

It is mainly intended for tools such as Codex or WorkBuddy.

The current MCP/query path is:

- local
- token-protected
- read-only
- designed around the current active book
- routed through XplorOne’s controlled local API and query layers

MCP is not required for normal bookkeeping, reports, Quick Entry, or in-app AI workflows.

## 15. Does MCP directly read the database?

No.

Current MCP access goes through XplorOne’s controlled local API and query layers.

It does not directly read the database and does not bypass the application’s query boundary.

## 16. Can MCP write or edit my ledger?

No.

The current MCP path is read-only.

It does not expose write actions.

## 17. Are backups and exported files safe to share?

Backups and exported files may contain sensitive financial data.

Even when credentials are not exposed as plain text, financial records themselves are sensitive.

Users should not publicly share:

- backups
- exported ledger files
- screenshots with financial data
- API keys
- local tokens
- model credentials

If you need support, remove private financial data and credentials before posting.

## 18. Do exported ledger files include my API key?

Exported ledger files should not expose model API keys or MCP tokens as plain text.

Some full-app backup workflows may include protected credential metadata for same-machine recovery, but protected credential backup is not the same as a portable plain-text key export.

If you move data to another machine, you may need to reconfigure model API keys or local integration tokens.

## 19. Can I migrate XplorOne data to another computer?

Depending on the backup or export workflow, financial data may be portable.

However, protected credentials may depend on the current machine or operating-system credential environment.

When moving to another machine, you may need to:

- restore or import financial data
- reconfigure model API keys
- regenerate local API or MCP tokens
- re-test AI model configuration

## 20. Does XplorOne support every bank or payment platform import format?

Not necessarily.

Import and export coverage may vary by release.

Users should not assume every bank, payment platform, or accounting export format is supported.

Imported data should be reviewed by the user.

## 21. Is XplorOne a tax, legal, or accounting compliance service?

No.

XplorOne helps users organize, review, and understand financial records.

It is not:

- legal advice
- tax advice
- certified accounting advice
- a country-specific tax filing system
- a substitute for a qualified accountant or tax professional

Users remain responsible for their own financial decisions and local compliance requirements.

## 22. Is XplorOne open source?

No, not unless explicitly stated otherwise.

XplorOne is proprietary software.

This repository serves as the public product hub for documentation, releases, roadmap updates, and community feedback. It is not a full open-source code landing page.

For details, see [LICENSE.md](../LICENSE.md).

## 23. Where should I download XplorOne?

Use the official download links provided by this repository or the official website.

For GitHub users, start from [GitHub Releases](https://github.com/SimonZhangM/XplorOne/releases).

Make sure you are downloading from an official source.

## 24. What is the difference between GitHub Releases and the official website?

GitHub Releases can serve as a public release and version history channel.

The official website may provide product pages, download guidance, documentation links, and release information.

Depending on the release channel, the download experience may differ, but users should always use official links.

## 25. Why is there a Web preview if the desktop app is the official release?

Web preview is used for development and internal preview.

It is not the official end-user release form.

Some desktop capabilities, such as system file dialogs or local desktop integration, may not behave the same way in Web preview.

## 26. Why is Windows the current official release line?

XplorOne is currently focused on making the Windows desktop release stable and usable.

Other platforms should not be assumed available unless explicitly published.

For current availability, check [Releases](https://github.com/SimonZhangM/XplorOne/releases).

## 27. What should I do if AI responses are in the wrong language?

When reporting a language issue, include:

- UI language
- input language
- model provider
- expected response language
- actual response language
- whether the issue happened in Local Assistant or AI Assistant

XplorOne may consider the current message language, previous clear user language in the session, and UI language as fallback.

## 28. What should I do if model connection testing fails?

Check:

- whether the API key is correct
- whether the base URL is correct
- whether the model name exists for that provider
- whether the provider account has enough credits or quota
- whether the provider requires a special endpoint format
- whether your network connection is available

For more details, see [BYOK Setup](./byok-setup.md).

## 29. Where should I ask questions or report problems?

Use:

- [Discussions](https://github.com/SimonZhangM/XplorOne/discussions) for questions, ideas, feedback, and product discussion
- [Issues](https://github.com/SimonZhangM/XplorOne/issues) for clear bugs, installer problems, and actionable reports
- [Releases](https://github.com/SimonZhangM/XplorOne/releases) for downloads and release notes

Before posting publicly, remove private financial data, API keys, local tokens, and personal information.

## 30. What information should I include in a bug report?

A useful bug report usually includes:

- XplorOne version
- Windows version
- where the issue happened
- steps to reproduce
- expected behavior
- actual behavior
- screenshots if helpful
- whether AI, BYOK, Local API, or MCP was involved

Do not include API keys, tokens, private financial data, or full unredacted logs.

## 31. Where should I go next?

- [Getting Started](./getting-started.md) — complete your first workflow
- [Feature Overview](./feature-overview.md) — understand the main product areas
- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md) — understand data, AI, and integration boundaries
- [BYOK Setup](./byok-setup.md) — configure your own model API key
- [Known Limitations](./known-limitations.md) — understand current release scope
- [Support](../SUPPORT.md) — learn where to ask questions or report problems
