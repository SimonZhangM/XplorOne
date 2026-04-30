English | [简体中文](./ai-assistant-behavior_zh-CN.md)

# AI Assistant Behavior

This document explains how XplorOne separates local workflows, AI analysis, and broader finance-related conversation.

XplorOne's AI is not positioned as a generic chatbot that can freely mutate your books.

## Assistant Modes

| Mode | Main role | Typical use | Key boundary |
|---|---|---|---|
| Local Assistant | local query and entry workflows | lookup, summaries, entry drafts | supported flows stay local-first and writes require confirmation |
| AI Analysis | structured financial interpretation | trends, explanations, period comparison, risk review | uses task-relevant financial context and does not replace user judgment |
| Free Chat | broader finance-related conversation | concepts, planning discussion, workflow thinking | not the default direct ledger-query path |

## Local Assistant

Local Assistant is designed for faster deterministic workflows.

It can help with:

- local finance queries
- transaction lookup
- basic summaries
- entry draft workflows

Supported local query and entry flows do not silently fall back to AI guessing.

Entry drafts must be reviewed and confirmed by the user before anything is written.

## AI Analysis

AI Analysis can use structured financial context to help explain patterns.

It can help with:

- trend explanation
- income and expense comparison
- period comparison
- budget or category review
- cash-flow interpretation
- financial state discussion

AI Analysis should not claim that it performed actions such as writing, deleting, exporting, navigating, or editing unless those actions actually occurred through the app.

## Free Chat

Free Chat is for broader finance-related conversation.

It can help with:

- explaining financial concepts
- breaking down planning questions
- discussing business or personal finance workflows
- thinking through options before the user acts

Free Chat is not positioned as the default path for direct ledger query.

## What XplorOne AI Does Not Do

XplorOne AI should not be treated as:

- automatic bookkeeping without confirmation
- a tax, legal, audit, or accounting compliance authority
- deterministic investment advice
- a replacement for professional judgment
- a system that can claim invisible actions happened
- a tool that can bypass local data and write boundaries

## Personalization and Language

If AI personalization is enabled, XplorOne is intended to use a controlled natural-language summary rather than raw settings JSON.

Personalization context should follow the current response language, so Chinese conversations and English conversations can receive language-appropriate context.

## User Responsibility

AI output should be reviewed by the user.

For financial decisions, users remain responsible for:

- checking records
- confirming writes
- reviewing model output
- choosing trusted model providers
- following local legal, tax, and accounting obligations

## Related Documents

- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md)
- [BYOK Setup](./byok-setup.md)
- [Local API and MCP](./local-api-and-mcp.md)
- [Known Limitations](./known-limitations.md)

