# Changelog

This file summarizes major XplorOne release changes for the GitHub product hub.

For complete user-facing release notes, see:

- [Software Release History](./docs/software-release-history.md)

XplorOne is currently moving from an early local-first desktop finance workspace into a more complete product release line, with work across Windows packaging, local data boundaries, AI workflows, bilingual UI, reporting, budget stability, and read-only local MCP integration.

---

## Latest Release

### v0.3.8 - 2026-04-24

**Focus: English desktop experience, safer existing-book handling, and settings polish**

This release improves the English desktop experience across labels, settings, budget views, menus, and existing-book display behavior, while reducing the risk of accidental data mutation during upgrades.

#### Highlights

- Added a global currency-symbol preference.
- Added model preset persistence and clearer model-setting status indicators.
- Added basic English entry parsing for common bookkeeping sentences, including income, expense, transfer, loan, repayment, refund, account, relative-date, and AM/PM time expressions.
- Renamed the English `Ledger` surface to `Transactions` across navigation, page titles, actions, confirmations, and export text.
- Improved display-language mapping for existing book data without rewriting existing account, category, project, member, or template records.
- Improved budget, account, category, home, report, settings, personalization, menu, About, and update-dialog localization and layout polish.
- Fixed mixed Chinese and English account, category, and project names after switching UI language.
- Fixed seed logic that could reinsert default accounts, categories, members, or projects into books that already contain data.

#### Security and stability

- Reduced the risk of accidental data mutation during upgrades by making default data seeding conditional on empty or clearly legacy data.
- Improved existing-book language switching by localizing at display time instead of writing translated duplicate data into the book.
- Preserved model preset metadata alongside provider configuration for more reliable model-setting restore and enable flows.

---

## Recent Releases

### v0.3.7 - 2026-04-24

**Focus: bilingual AI chat and English query experience**

- Improved bilingual AI chat responses based on the user's current message.
- Added backend chat language context detection using current message, previous clear user language, and UI language fallback.
- Added local English query parsing for common finance questions such as monthly income, monthly spending, account balance, and top expense categories.
- Added time-only follow-up support in query chats, such as `and last month?`.
- Improved Query, Analysis, Free Chat, and Entry draft language behavior.
- Fixed cases where the response language did not follow the user's actual input.

### v0.3.6 - 2026-04-23

**Focus: budget-page loading and shared cache**

- Replaced the older aggregated budget-page loading path with lighter budget calls.
- Shared budget cache between the Home page and Budget page.
- Improved budget request deduplication, abort-on-leave behavior, and loading triggers.
- Fixed repeated same-month budget requests.

### v0.3.5 - 2026-04-23

**Focus: budget stability and local-preview error feedback**

- Stabilized budget loading and annual budget saving.
- Improved budget-page cache, month summaries, table loading, and optimistic updates.
- Improved budget balance display, year chips, filters, and footer alignment.
- Improved bilingual local-preview runtime errors and fallback messages.
- Fixed mismatches between month summaries and budget tables after switching months.

### v0.3.4 - 2026-04-23

**Focus: Cash Flow report and chart scaling**

- Added the Cash Flow report page.
- Unified chart scaling across Income & Expense and Cash Flow mirrored trend charts.
- Improved report icons, chart areas, spacing, and bilingual labels.
- Fixed misleading bar proportions caused by independently scaled mirrored charts.

### v0.3.3 - 2026-04-22

**Focus: renderer type-check cleanup and management-page polish**

- Cleared historical renderer type-check errors.
- Added the full create-member flow.
- Added shared normalizers for stable renderer-side result handling.
- Unified action buttons across member, project, account, and income/expense pages.
- Improved visual consistency across Ledger, Income & Expense, Accounts, and Calendar pages.

---

## 0.3 Series Highlights

The 0.3 series focuses on English product readiness, bilingual AI chat, budget stability, cash-flow reporting, renderer cleanup, licensing foundations, and internationalized desktop surfaces.

- Added commercial licensing foundations and bilingual book-template assembly.
- Improved Settings, Reports, Home, Calendar, Ledger/Transactions, Budget, and management-page internationalization.
- Added the Cash Flow report and aligned mirrored trend chart scaling.
- Clarified Ledger cash-flow semantics separately from income/expense accounting statistics.
- Improved budget loading, shared budget cache, annual budget saving, and local-preview error feedback.
- Improved bilingual AI chat behavior, English query parsing, and follow-up query handling.

---

## 0.2 Series Highlights

The 0.2 series moved XplorOne from an early desktop finance workspace toward a more productized release line. It added local MCP foundations, model-service configuration improvements, Windows release packaging, UI internationalization, `.xpl` archive migration, and budget database consolidation.

- Added the XplorOne Read-Only MCP v1 baseline.
- Added Codex and WorkBuddy client-token management foundations.
- Added `.xpl` single-file export and import foundations for archived books.
- Merged the separate budget database into the main XplorOne database.
- Added reminder-center and display-preference foundations.
- Added lightweight `zh-CN / en-US` UI internationalization infrastructure.
- Added Windows portable and NSIS release packaging foundations.
- Added release privacy verification to reduce the risk of shipping private local files.
- Improved model-service presets, API-key reuse, testing, activation, and response cleanup.
- Encrypted MCP client tokens with Electron `safeStorage`.

---

## Early Development Releases

### v0.0.5 - v0.1.9 - 2026-04-01 to 2026-04-16

These versions record XplorOne's transition from early prototype to a local-first desktop finance workspace.

- Added core finance modules such as Accounts, Categories, Members, Projects, Transactions, Home Overview, and basic reports.
- Added early AI Query, AI Entry, AI Analysis, and Free Chat flows.
- Added book settings, data settings, budget management, and multi-book foundations.
- Added professional chart types such as treemap, sunburst, waterfall, dual-axis, and heatmap.
- Evolved the app from a single-page prototype into a multi-module desktop workspace.
- Reworked navigation, toolbars, charts, tables, repository layers, service layers, and shared contracts across many early iterations.
- Improved model adaptation, query parsing, time-range parsing, and AI response display.

Early release notes were reconstructed from historical tags and commit summaries, so they are less detailed than later releases.

---

## Detailed Release Notes

For full per-version user-facing release notes, including Added / Changed / Improved / Fixed / Known Issues sections, see:

- [Software Release History](./docs/software-release-history.md)
