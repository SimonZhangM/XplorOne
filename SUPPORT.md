English | [简体中文](./SUPPORT_zh-CN.md)

# Support

This page explains how to ask questions, report problems, and share feedback for XplorOne.

XplorOne is a local-first desktop finance workspace. Because it may involve financial data, model API keys, local tokens, backups, and screenshots, please read the safety notes before posting publicly.

## 1. Before Asking for Help

Before opening a new issue or discussion, please check:

- [Getting Started](./docs/getting-started.md)
- [Feature Overview](./docs/feature-overview.md)
- [FAQ](./docs/faq.md)
- [Known Limitations](./docs/known-limitations.md)
- [BYOK Setup](./docs/byok-setup.md)
- [Privacy & AI Boundaries](./docs/privacy-and-ai-boundaries.md)
- [Privacy](./PRIVACY.md)
- [Security](./SECURITY.md)
- [Releases](https://github.com/SimonZhangM/XplorOne/releases)

Also make sure you are using the latest available release unless you are intentionally testing an older version.

## 2. Where to Ask

### General questions, ideas, and usage discussion

Use [Discussions](https://github.com/SimonZhangM/XplorOne/discussions) for:

- product questions
- usage questions
- feature ideas
- workflow feedback
- documentation suggestions
- early user experience feedback

Discussions are the best place when the topic is exploratory or not clearly a bug.

### Bugs and actionable problems

Use [Issues](https://github.com/SimonZhangM/XplorOne/issues) for:

- reproducible bugs
- installer problems
- crashes
- broken UI behavior
- incorrect results
- clear feature defects
- model configuration problems that can be reproduced
- MCP or Local API problems that can be described clearly

Issues work best when the report includes steps, environment details, and expected vs. actual behavior.

When opening an issue, please use the available issue form instead of posting an empty report.

### Security or sensitive reports

Do **not** post security-sensitive information publicly.

Email sensitive reports to:

- simonzhang2026@163.com

Use private contact for:

- token exposure
- API key exposure
- suspected credential handling problems
- private financial data exposure
- security-sensitive installation or update problems

### Business, licensing, OEM, or commercial inquiries

For licensing, redistribution, integration, OEM, white-label, or commercial cooperation inquiries, contact:

- simonzhang2026@163.com
- www.xplorone.com

## 3. What Not to Share Publicly

Please do not post the following in public Issues or Discussions:

- model API keys
- Local API tokens
- MCP client tokens
- license codes
- private financial records
- real bank statements
- exported ledger files
- full backups
- unredacted logs
- screenshots containing private financial data
- personal identity information
- provider account details

Before posting screenshots or logs, remove sensitive information.

## 4. What to Include in a Bug Report

A useful bug report usually includes:

- XplorOne version
- Windows version
- where the issue happened
- what you were trying to do
- steps to reproduce
- expected behavior
- actual behavior
- screenshots, if helpful and redacted
- whether the issue involves AI, BYOK, Local API, MCP, import/export, backup, or installer behavior

Suggested format:

```text
XplorOne version:
Windows version:
Page or feature:
What I tried:
Steps to reproduce:
Expected result:
Actual result:
Does it involve AI / BYOK / MCP / import / backup:
Screenshots or logs:
Sensitive data removed: yes / no
```

## 5. Installer or Windows Release Problems

For installer or release problems, include:

- XplorOne version
- installer file name
- download source
- Windows version
- whether the installer came from GitHub Releases or the official website
- error message or screenshot
- whether this is a first install, update, reinstall, or uninstall problem

Do not upload installer logs if they contain private paths, tokens, usernames, or other sensitive information unless they are redacted.

## 6. AI or BYOK Problems

For AI or BYOK-related problems, include:

- provider name
- base URL type, but not secret values
- model name
- whether connection test passed
- which assistant was used:
  - Local Assistant
  - AI Assistant
- which capability was involved:
  - Query
  - Entry
  - Analysis
  - Free Chat
- input language
- expected response language
- actual response language
- error message, if any

Do **not** include your API key.

For setup details, see [BYOK Setup](./docs/byok-setup.md).

## 7. Local API or MCP Problems

For Local API or MCP-related problems, include:

- XplorOne version
- external client name, such as Codex or WorkBuddy
- whether the issue is about Local API, MCP, or both
- what tool or query was attempted
- expected result
- actual result
- relevant error message
- whether XplorOne was running at the time

Do **not** include:

- Local API token
- MCP client token
- full endpoint with secret token
- private financial output

The current MCP path is read-only and goes through XplorOne’s controlled local API and query layers. It does not directly read the database.

For details, see [Privacy & AI Boundaries](./docs/privacy-and-ai-boundaries.md) and [Local API and MCP](./docs/local-api-and-mcp.md).

## 8. Import, Export, Backup, or Data Problems

For data-related problems, include:

- XplorOne version
- operation type:
  - backup
  - restore
  - export
  - import
  - archive
  - `.xpl` workflow
- source file type
- whether this is current-book data or archived-book data
- what you expected to happen
- what actually happened
- error message, if any

Do not upload private financial files publicly.

If a sample file is needed, create a fake or redacted sample that does not contain real financial data.

## 9. Feature Requests

Feature requests are welcome in [Discussions](https://github.com/SimonZhangM/XplorOne/discussions).

A helpful feature request usually explains:

- what problem you are trying to solve
- your current workaround
- why the existing workflow is not enough
- whether this is a personal, freelance, studio, or business workflow
- whether the request relates to bookkeeping, reports, AI, import/export, MCP, or settings

Please avoid turning feature requests into broad “all-in-one” product requests. XplorOne is intentionally focused on local-first finance workflows for solopreneurs and small studios.

## 10. Response Expectations

Support is handled on a best-effort basis.

Public Issues and Discussions may not receive an immediate response.

Clear, reproducible reports are easier to investigate.

Reports that include sensitive data publicly may be edited, closed, or removed for safety.

Commercial support terms, if any, are handled separately from public GitHub support.

## 11. Useful Links

- [README](./README.md)
- [Getting Started](./docs/getting-started.md)
- [Feature Overview](./docs/feature-overview.md)
- [FAQ](./docs/faq.md)
- [Known Limitations](./docs/known-limitations.md)
- [BYOK Setup](./docs/byok-setup.md)
- [Privacy & AI Boundaries](./docs/privacy-and-ai-boundaries.md)
- [Privacy](./PRIVACY.md)
- [Security](./SECURITY.md)
- [Data Storage and Backup](./docs/data-storage-and-backup.md)
- [AI Assistant Behavior](./docs/ai-assistant-behavior.md)
- [Local API and MCP](./docs/local-api-and-mcp.md)
- [Releases](https://github.com/SimonZhangM/XplorOne/releases)
- [Discussions](https://github.com/SimonZhangM/XplorOne/discussions)
- [Issues](https://github.com/SimonZhangM/XplorOne/issues)
