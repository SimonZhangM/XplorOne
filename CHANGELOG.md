# Changelog

This file summarizes major XplorOne release changes for the GitHub product hub.

For complete user-facing release notes, see:

- [Software Release History](./docs/software-release-history.md)

XplorOne is currently moving from an early local-first desktop finance workspace into a more complete product release line, with work across Windows packaging, local data boundaries, AI workflows, bilingual UI, reporting, budget stability, and read-only local MCP integration.

---

## Latest Release

### v0.3.7 — 2026-04-24

**Focus: bilingual AI chat and English query experience**

This release improves the bilingual AI chat experience. XplorOne can now respond in Chinese or English based on the user's current message, with better English query parsing and smoother follow-up questions.

#### Highlights

- Improved bilingual AI chat responses.
- Added backend chat language context detection using current message, previous clear user language, and UI language fallback.
- Added local English query parsing for common finance questions such as:
  - `this month total income`
  - `how much did I spend this month`
  - `account balance`
  - `top expense categories this year`
- Added time-only follow-up support in query chats, such as `and last month?`.
- Improved Query, Analysis, Free Chat, and Entry draft language behavior.
- Fixed cases where the response language did not follow the user's actual input.

#### Still pending

- English natural-language entry parsing is not included yet.

---

## Recent Releases

### v0.3.6 — 2026-04-23

**Focus: budget-page loading and shared cache**

- Replaced the older aggregated budget-page loading path with lighter budget calls.
- Shared budget cache between the Home page and Budget page.
- Improved budget request deduplication, abort-on-leave behavior, and loading triggers.
- Fixed repeated same-month budget requests.

### v0.3.5 — 2026-04-23

**Focus: budget stability and local-preview error feedback**

- Stabilized budget loading and annual budget saving.
- Improved budget-page cache, month summaries, table loading, and optimistic updates.
- Improved budget balance display, year chips, filters, and footer alignment.
- Improved bilingual local-preview runtime errors and fallback messages.
- Fixed mismatches between month summaries and budget tables after switching months.

### v0.3.4 — 2026-04-23

**Focus: Cash Flow report and chart scaling**

- Added the Cash Flow report page.
- Unified chart scaling across Income & Expense and Cash Flow mirrored trend charts.
- Improved report icons, chart areas, spacing, and bilingual labels.
- Fixed misleading bar proportions caused by independently scaled mirrored charts.

### v0.3.3 — 2026-04-22

**Focus: renderer type-check cleanup and management-page polish**

- Cleared historical renderer type-check errors.
- Added the full create-member flow.
- Added shared normalizers for stable renderer-side result handling.
- Unified action buttons across member, project, account, and income/expense pages.
- Improved visual consistency across Ledger, Income & Expense, Accounts, and Calendar pages.

### v0.3.2 — 2026-04-22

**Focus: Ledger cash-flow semantics**

- Separated Ledger cash-flow statistics from income/expense accounting statistics.
- Changed Ledger totals to:
  - Net Flow
  - Cash Inflow
  - Cash Outflow
- Counted transfers as inflow/outflow in single-account views while keeping ordinary transfers excluded from the global view.
- Improved jump-to-ledger filters from Income & Expense and Accounts pages.

### v0.3.1 — 2026-04-21

**Focus: Settings and Reports internationalization cleanup**

- Localized more Settings panels, dialogs, status messages, and web-preview fallback text.
- Moved more basic report-page labels into the dictionary layer.
- Improved English flows for file picking, path opening, restore confirmation, and import confirmation.
- Fixed a report-page `t is not defined` runtime crash.

### v0.3.0 — 2026-04-21

**Focus: licensing foundation and bilingual book templates**

- Added the China-market commercial licensing foundation.
- Added local license-code storage, signature validation, trial state, and Standard/Pro tiers.
- Added a License Center panel for tier, trial, validation, and feature-boundary visibility.
- Added bilingual book-template assembly for English UI book creation.
- Added commercial permission checks for MCP and external connection entry points.

---

## 0.2 Series Highlights

The 0.2 series moved XplorOne from an early desktop finance workspace toward a more productized release line. It added local MCP foundations, model-service configuration improvements, Windows release packaging, UI internationalization, `.xpl` archive migration, and budget database consolidation.

### v0.2.12 — 2026-04-21

**Focus: high-frequency page internationalization**

- Added Chinese/English UI coverage to Home, Ledger, Quick Entry, Accounts, Income & Expense, and Budget pages.
- Normalized `accounts.owner_type` to stable English values:
  - `personal`
  - `business`
  - `mixed`
- Improved Follow System language detection so Chinese systems are no longer detected as English.

### v0.2.11 — 2026-04-20

**Focus: first UI internationalization foundation**

- Added lightweight i18n infrastructure with `zh-CN / en-US` dictionaries.
- Added interface language preferences:
  - Follow System
  - Simplified Chinese
  - English
- Localized the top shell, sidebar navigation, settings sections, notification popover, window controls, and personalization page.
- Unified Electron and web-preview system language entry points.

### v0.2.10 — 2026-04-20

**Focus: NSIS installer and release privacy checks**

- Added the `dist:win:nsis` installer build command.
- Added NSIS installer configuration, including install directory selection, shortcuts, and uninstall display name.
- Reused the Windows prepackaged release pipeline for both portable and NSIS targets.
- Extended release privacy checks to inspect portable, NSIS, and packaged `app.asar` output.

### v0.2.9 — 2026-04-20

**Focus: Windows release flow, model settings, and settings-page structure**

- Added the DeepSeek model-service preset.
- Added release privacy verification to keep databases, tokens, credential seeds, `.xpl` files, and private runtime files out of release artifacts.
- Improved synchronization between the active model and the current model-service draft preset.
- Improved silent refresh after creating, editing, or deleting transactions.
- Improved Personalization and Data Settings into a single-card structure.

### v0.2.8 — 2026-04-19

**Focus: portable release stabilization and legal files**

- Stabilized the Windows portable release pipeline.
- Added repository-level legal files:
  - `LICENSE`
  - `EULA.md`
  - `THIRD_PARTY_NOTICES.md`
  - distribution-policy documentation
- Replaced the Windows icon with a real multi-size `.ico`.
- Improved final portable metadata, product name, copyright, and icon resources.

### v0.2.7 — 2026-04-19

**Focus: model-service configuration and activation semantics**

- Added MiniMax, Moonshot/Kimi, and Zhipu/GLM model presets.
- Split model service actions into:
  - Save AI Config
  - Test Connection
  - Activate Current Config
- Allowed saved API keys to be reused when switching models under the same API endpoint.
- Improved OpenAI-compatible testing for Kimi, GLM, MiniMax, and similar providers.
- Improved active-model display behavior and model response cleanup.

### v0.2.6 — 2026-04-17

**Focus: reminder settings and web-preview polish**

- Renamed General Settings to Reminder Settings.
- Added `public/logo.ico` as the web-preview favicon.
- Fixed noisy `/favicon.ico` 404 behavior in web preview.

### v0.2.5 — 2026-04-16

**Focus: communication-page structure and layout cleanup**

- Continued refining communication-related entries and page structure toward a stable chat module.
- Improved page layout, sidebar structure, and chat-related visual behavior.

### v0.2.4 — 2026-04-16

**Focus: reminder center and display preferences**

- Added reminder-center foundations for bookkeeping, budget, and backup reminders.
- Added display settings for:
  - dates
  - numbers
  - font size
  - Quick Entry defaults
- Improved Settings grouping and reminder-entry experience.

### v0.2.3 — 2026-04-16

**Focus: archived-book `.xpl` export and import**

- Added `.xpl` single-file export for archived books.
- Added `.xpl` import as a new active book.
- Improved `.xpl` preview, filename sanitization, repeated-import behavior, and ID remapping.
- Fixed `.xpl` as a gzip-compressed UTF-8 JSON package with size limits.

### v0.2.2 — 2026-04-16

**Focus: archived migration-package planning and documentation**

- Improved `.xpl` migration-package design notes.
- Improved import confirmation experience.
- Improved root documentation around current implementation boundaries.

### v0.2.1 — 2026-04-16

**Focus: budget database merge**

- Merged `xplorone-budget.db / budget.db` into the main `xplorone.db`.
- Updated budget pages, home budget summaries, snapshots, restore, CSV, and future `.xpl` flows to rely on main database budget tables.
- Improved legacy budget merge behavior so old budget databases are only used as one-time migration sources.

### v0.2.0 — 2026-04-16

**Focus: Read-Only MCP v1, external integration, and productization foundation**

- Added the XplorOne Read-Only MCP v1 baseline.
- Added Codex and WorkBuddy client-token management foundations.
- Added versioned in-repository XplorOne skill content.
- Changed external agent queries to prefer Local API / QueryExecutor instead of direct SQLite access.
- Confirmed MCP as read-only, without write support or explicit cross-book queries.
- Encrypted MCP client tokens with Electron `safeStorage`.
- Improved Local API, MCP, Settings, and external-tool documentation boundaries.

---

## Early Development Releases

### v0.0.5 – v0.1.9 — 2026-04-01 to 2026-04-16

These versions record XplorOne's transition from early prototype to a local-first desktop finance workspace.

#### Major foundations

- Added core finance modules:
  - Accounts
  - Categories
  - Members
  - Projects
  - Transactions
  - Home Overview
  - Basic reports
- Added early AI workflows:
  - AI Query
  - AI Entry
  - AI Analysis
  - Free Chat
- Added book settings, data settings, budget management, and multi-book foundations.
- Added professional chart types:
  - treemap
  - sunburst
  - waterfall
  - dual-axis
  - heatmap

#### Product evolution

- Evolved the app from a single-page prototype into a multi-module desktop workspace.
- Reworked navigation, toolbars, charts, and tables across many pages.
- Expanded database, repository, service, and shared contract layers.
- Improved Quick Entry, transaction filters, account management, category management, member/project management, and reports.
- Unified page visuals, icons, emoji, buttons, dialogs, filters, and statistic cards.
- Improved model adaptation, query parsing, time-range parsing, and AI response display.

#### Note

Early release notes were reconstructed from historical tags and commit summaries, so they are less detailed than later releases.

---

## Detailed Release Notes

For full per-version user-facing release notes, including Added / Changed / Improved / Fixed / Known Issues sections, see:

- [Software Release History](./docs/software-release-history.md)