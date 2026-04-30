English | [简体中文](./SECURITY_zh-CN.md)

# Security

Last Updated: 2026-04-30

This document explains how to report security-sensitive issues for XplorOne.

## Supported Versions

Security review and fixes focus on the current public Windows release and recent public release line.

Users should download XplorOne from official sources:

- [GitHub Releases](https://github.com/SimonZhangM/XplorOne/releases)
- the official website when available

Older versions may not receive the same level of review, documentation updates, or compatibility fixes.

## Reporting a Security Issue

Please do not report security-sensitive issues in public GitHub Issues or Discussions.

Send security-sensitive reports to:

- simonzhang2026@163.com

Helpful reports include:

- XplorOne version
- Windows version
- installer or update source
- affected area
- steps to reproduce
- expected behavior
- actual behavior
- screenshots or logs only if redacted

## Do Not Share Publicly

Do not post the following publicly:

- model API keys
- Local API tokens
- MCP client tokens
- license codes
- full local databases
- full backups
- exported ledger files with real data
- unredacted logs
- screenshots containing financial data or credentials
- local endpoints containing secret tokens

## Security Scope

Security-sensitive areas may include:

- installer and update behavior
- local credential storage
- model API key handling
- Local API token handling
- MCP client token handling
- local API access boundaries
- read-only MCP/query behavior
- backup, export, archive, and restore handling
- release packaging that might accidentally include private runtime data
- AI request boundaries where sensitive financial context may be involved

## Non-Security Issues

Use GitHub Issues or Discussions for ordinary product feedback, bugs, documentation problems, feature requests, installation questions, or model configuration questions that do not expose sensitive information.

- [Issues](https://github.com/SimonZhangM/XplorOne/issues)
- [Discussions](https://github.com/SimonZhangM/XplorOne/discussions)
- [Support](./SUPPORT.md)

