English | [简体中文](./data-storage-and-backup_zh-CN.md)

# Data Storage and Backup

This document explains how to think about local data, backups, exports, archives, and moving XplorOne between computers.

It is not a recovery guarantee. Users should keep their own safe backups.

## Where Data Lives

XplorOne is designed as a local-first desktop finance workspace.

Runtime data is stored in the user's local application data environment. This can include:

- books
- accounts
- categories
- transactions
- budgets
- reports and derived views
- settings and local metadata
- local integration configuration

Exact paths may vary by operating system, release channel, and user configuration.

## What Backups May Contain

Depending on the workflow and release version, backups may include:

- financial records
- book metadata
- categories and accounts
- budget data
- archive metadata
- settings
- protected credential metadata for same-machine recovery, where supported

Even if credentials are not exposed as plain text, backups can still contain sensitive financial data.

## Export, Archive, and Full Backup

Different data workflows serve different purposes.

| Workflow | Typical purpose | Notes |
|---|---|---|
| Export | move or inspect selected financial data | may not include every app setting |
| Archive / `.xpl` | preserve or move book-like data packages | scope depends on current release support |
| Full backup | preserve a broader app state | may include protected metadata and local-environment assumptions |

Do not assume that every workflow is interchangeable.

## API Keys and Tokens

Model API keys, Local API tokens, and MCP client tokens should not appear as plain text in exported ledger files.

Some full-app backup workflows may include protected credential metadata for same-machine recovery. Protected credential backup is not the same as a portable plain-text key export.

When moving to another computer, plan to:

- re-enter or re-test model API keys
- regenerate Local API or MCP tokens if needed
- re-check model-service configuration
- verify that imported or restored financial data is correct

## Moving to Another Computer

A careful migration usually looks like this:

1. Make a current backup or export from the old computer.
2. Keep an untouched copy of that backup.
3. Install XplorOne on the new computer from an official source.
4. Restore or import the data.
5. Review accounts, categories, transactions, reports, and budgets.
6. Reconfigure model API keys and local integration tokens if needed.
7. Test AI, backup, and export workflows before relying on the new setup.

## Restore and Overwrite Risks

Restore workflows may change local state.

Before restoring:

- confirm which book or app state will be affected
- keep a separate backup of the current state
- avoid testing restore with your only copy of real financial data
- review restored data before continuing daily use

## Cloud Sync Boundary

XplorOne is not currently positioned as an automatic cloud-sync product.

Cross-device use should be managed through backups, exports, archives, or future published sync capabilities when explicitly available.

## Related Documents

- [Privacy](../PRIVACY.md)
- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md)
- [Known Limitations](./known-limitations.md)
- [Support](../SUPPORT.md)

