English | [简体中文](./PRIVACY_zh-CN.md)

# Privacy

Last Updated: 2026-04-30

This document explains XplorOne's public privacy position for the desktop product, GitHub repository, downloads, support, and related public materials.

XplorOne is designed as a local-first desktop finance workspace. This privacy document is intended for user understanding and public trust. It does not replace the applicable EULA, third-party provider terms, or local legal requirements.

## Local Data by Default

XplorOne's core finance workflow is designed around local application data.

By default, your books, accounts, categories, transactions, reports, budgets, local settings, and related workspace data are stored in your local desktop environment.

Core bookkeeping, reports, financial views, and supported local queries do not require a model API key.

XplorOne is not designed around uploading your full local database to a cloud-first accounting system by default.

## Optional AI and Model Providers

AI-assisted features are optional.

When you use AI-assisted workflows, XplorOne may send task-relevant context to the model service that you configure.

Depending on the workflow, this may include:

- your current question or instruction
- structured financial context needed for the task
- selected report or query context
- entry draft context
- recent conversation context
- language-specific AI personalization summary, if you enabled personalization

XplorOne aims to send task-relevant context, not the entire local database by default.

Your model provider may process data according to its own terms and privacy practices. Users should choose providers they trust.

## API Keys and Local Tokens

XplorOne may handle several credential types:

- **Model API keys** connect XplorOne to the model service chosen by the user.
- **Local API tokens** protect local HTTP API access.
- **MCP client tokens** authorize external agents to use the local read-only MCP/query path.

These credential types are different and serve different purposes.

Model API keys and MCP client tokens are treated as sensitive local credentials. XplorOne is designed to store protected credentials through Electron `safeStorage` or an equivalent system-protected local credential mechanism where available.

Users should not share API keys, Local API tokens, MCP tokens, license codes, local endpoints containing secrets, screenshots exposing credentials, or unredacted logs.

## Backups, Exports, Logs, and Support Files

Backups, exports, archive packages, logs, screenshots, and issue attachments may contain sensitive financial or local environment information.

Before sharing anything publicly, remove:

- private financial records
- model API keys
- Local API tokens
- MCP client tokens
- license codes
- full database files
- full backups
- exported ledger files containing real data
- personal identity information
- local usernames, private paths, or provider account details

If a sample is needed, use fake or redacted data.

## GitHub, Website, Downloads, and Email Support

Public channels such as GitHub, the official website, download pages, release pages, Discussions, Issues, and email support may involve limited information that users choose to provide.

This may include:

- GitHub username and public comments
- issue or discussion content
- release download context visible to GitHub or hosting providers
- email address and message content when contacting support
- redacted screenshots, logs, or examples provided by the user

Please do not submit sensitive financial data through public GitHub Issues or Discussions.

Security-sensitive or private reports should be sent by email:

- simonzhang2026@163.com

## Third-Party Services

XplorOne may rely on third-party systems for distribution, hosting, GitHub repository features, model-provider connectivity, operating-system services, and bundled software components.

Third-party components and services remain subject to their own terms and privacy practices.

For third-party component notices, see [THIRD_PARTY_NOTICES.md](./THIRD_PARTY_NOTICES.md).

## User Responsibilities

Local-first software still requires careful handling by the user.

Users are responsible for:

- protecting their computer account
- choosing trusted model providers
- protecting backups and exported files
- rotating keys or tokens if exposed
- reviewing AI outputs before acting on them
- confirming write actions before ledger changes are saved

## Related Documents

- [Privacy & AI Boundaries](./docs/privacy-and-ai-boundaries.md)
- [Data Storage and Backup](./docs/data-storage-and-backup.md)
- [BYOK Setup](./docs/byok-setup.md)
- [Security](./SECURITY.md)
- [Support](./SUPPORT.md)

