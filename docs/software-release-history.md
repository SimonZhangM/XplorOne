# XplorOne Software Release History

This page records user-facing XplorOne release notes.  
It is based on the existing project changelog and rewritten in the newer public release-note format for GitHub, website, and marketing use.

---

# XplorOne v0.3.8

Release date: 2026-04-24

This release focuses on the international desktop experience, settings polish, model configuration, and safer handling of existing book data. XplorOne now presents accounts, categories, projects, common errors, reminders, and core list pages more consistently across Chinese and English, while adding global currency-symbol preferences and improving basic English entry parsing.

## Added

- Added a global currency-symbol preference with support for `￥`, `$`, and `€`.
- Added model preset persistence and clearer enabled-model status in Model Settings.
- Added basic English natural-language entry parsing for common categories, accounts, transfers, repayments, salaries, and time expressions such as `3 PM`.
- Added shared localized API error handling so English UI users see English error messages for common data, license, archive, and restore failures.

## Changed

- Reordered Settings navigation to prioritize daily-use preferences before ledger, model, license, data, and archive settings.
- Changed Display Settings and Reminder Settings to a single-card layout with internal section dividers.
- Moved new public release notes out of the old root changelog and into the dedicated software release history documents.

## Improved

- Improved bilingual display for account names, account types, category names, project names, member/project management entries, templates, and emoji/icon mapping.
- Improved category and budget pages so language switching does not create or display duplicate bilingual category groups.
- Improved account, category, ledger, report, calendar, home, and settings page spacing, headings, month labels, table alignment, and tooltip wording.
- Improved desktop update and About dialogs with localized text and edition information.
- Improved model requests in Electron by using the desktop networking path when available.

## Fixed

- Fixed mixed Chinese and English account/category names appearing after switching UI language.
- Fixed several missing category emoji mappings in the English UI.
- Fixed reminder time display issues caused by native time input localization.
- Fixed settings page scrolling so the sidebar stays fixed while the right panel scrolls.
- Fixed seed logic that could reinsert default accounts, categories, members, or projects into books that already had data.

## Security & Stability

- Strengthened model configuration storage by retaining preset metadata alongside the saved provider configuration.
- Reduced the risk of accidental data mutation during upgrades by making default data seeding conditional on empty or clearly legacy data.

---

# XplorOne v0.3.7

Release date: 2026-04-24

This release improves the bilingual AI chat experience. XplorOne can now respond in Chinese or English based on the user's current message, with better English query parsing and smoother follow-up questions.

## Added

- Added backend chat language context detection based on the current message, the previous clear user language in the same session, and UI language as fallback.
- Added local English query parsing for common questions such as `this month total income`, `how much did I spend this month`, `account balance`, and `top expense categories this year`.
- Added time-only follow-up support in query chats. Prompts like `and last month?` or equivalent Chinese follow-ups can reuse the previous query and only replace the time range.

## Changed

- Chat response language is no longer forced by the interface language. It now primarily follows the current user input.
- New Query, Analysis, FreeChat, and Entry draft messages can now use the detected response language.
- The renderer now sends the current UI language as fallback and uses backend `response_language` for action button labels.

## Improved

- Improved bilingual query answers, clarification prompts, table titles, table columns, amount labels, and period labels.
- Improved Analysis and FreeChat prompts so English questions receive more natural English responses.
- Improved Entry draft titles, field labels, missing-field hints, confirmation, cancellation, and submission messages.

## Fixed

- Fixed cases where Chinese input in an English UI could still receive English output.
- Fixed time-only follow-ups that previously failed to reuse the previous query context.

## Known Issues

- English natural-language entry parsing is not included yet. Sentences such as `spent 20 on lunch from cash` will be implemented in a later dedicated phase.

---

# XplorOne v0.3.6

Release date: 2026-04-23

This release improves budget-page loading and shares budget cache between the home page and budget page.

## Changed

- Replaced the old aggregated budget-page loading path with two lighter calls: `list_budget_months` and `get_budget_month`.
- Shared renderer-side budget cache between the home page and budget page.

## Improved

- Improved budget request deduplication, abort-on-leave behavior, and loading triggers.
- Improved navigation from home to budget by reusing already loaded budget data.

## Fixed

- Fixed repeated same-month budget requests.
- Removed temporary budget timing logs and restored development `StrictMode`.

---

# XplorOne v0.3.5

Release date: 2026-04-23

This release stabilizes budget loading, annual budget saving, and local-preview error messaging.

## Changed

- Consolidated budget-page loading so month summaries and current month details can be returned together.
- Changed annual budget saving to truly cover January through December of the selected year.
- Renamed several sidebar terms for a more polished product language.

## Improved

- Improved budget-page cache, month summary synchronization, table loading, and optimistic updates.
- Improved budget balance display, year chips, filter triggers, and footer alignment.
- Improved bilingual local-preview runtime errors and fallback messages.

## Fixed

- Fixed mismatches between left month summaries and right-side budget tables after switching months.
- Fixed unclear timeout and error feedback in budget preview and save flows.

---

# XplorOne v0.3.4

Release date: 2026-04-23

This release adds the Cash Flow report and aligns chart scaling across mirrored trend charts.

## Added

- Added a Cash Flow report page using the same cash-flow definition as the Ledger page.

## Changed

- Unified the vertical axis scaling for Income & Expense and Cash Flow monthly trend charts.
- Unified the Ledger sidebar filter trigger style with the shared time-range pattern.

## Improved

- Improved report icons, spacing, chart areas, and bilingual labels across income, expense, account, and cash-flow pages.

## Fixed

- Fixed misleading bar proportions caused by independently scaled mirrored charts.

---

# XplorOne v0.3.3

Release date: 2026-04-22

This release clears historical renderer type-check issues and improves member, project, and management-page interactions.

## Added

- Added the full create-member flow.
- Added shared normalizers for stable renderer-side result handling.

## Changed

- Replaced scattered `result.data` assertions with shared normalize/read helpers.
- Unified SVG action buttons across member, project, account, and income/expense pages.

## Improved

- Improved cached member/project management page loading with background refresh.
- Improved grouped table corner fills, status chips, action columns, borders, and spacing.
- Improved visual consistency across Ledger, Income & Expense, Accounts, and Calendar pages.

## Fixed

- Fixed historical renderer `typecheck` errors.
- Fixed unstable front-end result object handling in several pages.

---

# XplorOne v0.3.2

Release date: 2026-04-22

This release separates Ledger cash-flow statistics from income/expense accounting statistics.

## Changed

- Changed Ledger totals and time buckets to cash-flow terms: Net Flow, Cash Inflow, and Cash Outflow.
- Counted transfers as inflow/outflow in single-account views while keeping ordinary transfers excluded from the global view.

## Improved

- Improved Ledger explanation text to reduce confusion between cash-flow and income/expense reports.
- Improved jump-to-ledger filters from Income & Expense and Accounts pages.
- Improved bilingual notification-center messages and English date/range labels.

## Fixed

- Fixed confusion caused by mixing Ledger cash-flow statistics with income/expense statistics.

---

# XplorOne v0.3.1

Release date: 2026-04-21

This release continues English UI cleanup for Settings and Reports, and fixes a real report-page i18n runtime error.

## Changed

- Localized more Settings panels, dialogs, status messages, and web-preview fallback text.
- Moved more basic report-page labels into the dictionary layer.

## Improved

- Improved English flows for file picking, path opening, restore confirmation, and import confirmation.
- Improved long English labels in the Reports sidebar.
- Updated the XplorOne Codex skill documentation around active-book and read-only query boundaries.

## Fixed

- Fixed a report-page `t is not defined` runtime crash caused by missing translation-function propagation.

---

# XplorOne v0.3.0

Release date: 2026-04-21

This release introduces the commercial licensing foundation, bilingual book templates, and more internationalized home/calendar details.

## Added

- Added the China-market commercial licensing foundation, including trial state, local license code storage, signature validation, and Standard/Pro tiers.
- Added a License Center panel for tier, trial, validation, and feature-boundary visibility.
- Added bilingual book-template assembly so English UI can create books with English template content.

## Changed

- MCP and external connection entry points now check commercial permissions.
- Web preview and local Node API gained development-only commercial bypass switches.

## Improved

- Improved English date labels, ranking titles, tool buttons, export buttons, and generated placeholder labels on Home and Calendar pages.
- Improved pricing and authorization documentation.

## Security & Stability

- Strengthened professional-feature permission checks at entry points.

---

# XplorOne v0.2.12

Release date: 2026-04-21

This release continues high-frequency page internationalization and normalizes account ownership values.

## Changed

- Added Chinese/English UI coverage to Home, Ledger, Quick Entry, Accounts, Income & Expense, and Budget pages.
- Normalized `accounts.owner_type` to stable English values: `personal`, `business`, and `mixed`.

## Improved

- Improved Follow System language detection so Chinese systems are no longer detected as English.
- Improved compatibility for legacy Chinese account ownership values.

## Fixed

- Removed deprecated internal Chinese constants and unused mappings that could confuse later i18n work.

---

# XplorOne v0.2.11

Release date: 2026-04-20

This release adds the first front-end UI internationalization foundation.

## Added

- Added lightweight i18n infrastructure with `zh-CN / en-US` dictionaries, `t(key, params)`, and fallback behavior.
- Added interface language preferences: Follow System, Simplified Chinese, and English.
- Added unified Electron and web-preview system language entry points.

## Changed

- Localized the top shell, sidebar navigation, settings sections, notification popover, window controls, and personalization page.

## Improved

- Improved system-language resolution so pages do not individually read browser or OS language state.

## Known Issues

- This phase only covers front-end UI shell text. Backend errors, AI prompts, and professional chart labels are not included yet.

---

# XplorOne v0.2.10

Release date: 2026-04-20

This release improves the Windows release pipeline with an NSIS installer target and unified privacy checks.

## Added

- Added the `dist:win:nsis` installer build command.
- Added NSIS package configuration, including install directory selection, shortcuts, and uninstall display name.

## Changed

- Fixed `dist:win` as the default portable release command.
- Reused the same Windows prepackaged release pipeline for portable and NSIS targets.

## Improved

- Improved `scripts/win-prepackaged-release.js` to generate portable or NSIS packages by target.
- Improved release documentation around whitelists and private-data boundaries.

## Security & Stability

- Extended `verify:release:privacy` to inspect portable, NSIS, and packaged `app.asar` output.

---

# XplorOne v0.2.9

Release date: 2026-04-20

This release formalizes the Windows release flow and improves model settings, silent refresh, and settings-page structure.

## Added

- Added the DeepSeek model-service preset.
- Added a release privacy verification script to keep databases, tokens, credential seeds, `.xpl` files, and private runtime files out of release artifacts.

## Changed

- Fixed the Windows release flow to the Windows prepackaged release pipeline.
- Simplified sidebar navigation while keeping hidden professional chart implementations available.

## Improved

- Improved synchronization between the active model and the current model-service draft preset.
- Improved silent refresh after creating, editing, or deleting transactions.
- Improved Personalization and Data Settings into a single-card structure with separators.

## Security & Stability

- Strengthened release privacy checks to reduce the risk of shipping sensitive local files.

---

# XplorOne v0.2.8

Release date: 2026-04-19

This release stabilizes the Windows portable release pipeline and adds legal files and proper Windows icon resources.

## Added

- Added repository-level legal files: `LICENSE`, `EULA.md`, `THIRD_PARTY_NOTICES.md`, and distribution-policy documentation.

## Changed

- Changed Windows portable packaging to a two-stage controlled build flow.
- Replaced the Windows icon with a real multi-size `.ico`.

## Improved

- Improved final portable metadata, product name, copyright, and icon resources.

## Security & Stability

- Verified legal files are included in the packaged resources directory.

---

# XplorOne v0.2.7

Release date: 2026-04-19

This release refines model-service configuration, test, and activation semantics.

## Added

- Added MiniMax, Moonshot/Kimi, and Zhipu/GLM model presets.
- Added collapsible display for model `<think>...</think>` content.

## Changed

- Split model service actions into Save AI Config, Test Connection, and Activate Current Config.
- Allowed saved API keys to be reused when switching models under the same API endpoint.

## Improved

- Improved OpenAI-compatible testing for Kimi, GLM, MiniMax, and similar providers.
- Improved Kimi K2.5 temperature handling, strict JSON fallback, and response cleanup.

## Fixed

- Fixed active-model display being incorrectly affected by draft preset switches.
- Fixed several cases where a model could test successfully but fail to save or activate.

---

# XplorOne v0.2.6

Release date: 2026-04-17

This release renames General Settings to Reminder Settings and adds a favicon for web preview.

## Changed

- Renamed the Settings sidebar entry from General Settings to Reminder Settings.
- Declared `public/logo.ico` as the favicon for web preview.

## Improved

- Improved the location and naming of reminder-related settings.

## Fixed

- Fixed the browser's default `/favicon.ico` request producing a noisy 404 in web preview.

---

# XplorOne v0.2.5

Release date: 2026-04-16

This release continues communication-page structure and page-layout cleanup.

## Changed

- Continued refining communication-related entries and page structure toward a stable chat module.

## Improved

- Improved page layout, sidebar structure, and chat-related visual behavior.

---

# XplorOne v0.2.4

Release date: 2026-04-16

This release adds reminder-center and display-preference foundations.

## Added

- Added reminder-center foundations for bookkeeping, budget, and backup reminders.
- Added display settings for dates, numbers, font size, and Quick Entry defaults.

## Improved

- Improved Settings grouping and reminder-entry experience.
- Improved display-preference save, reset, and preview flows.

---

# XplorOne v0.2.3

Release date: 2026-04-16

This release advances archived-book `.xpl` export and import.

## Added

- Added `.xpl` single-file export for archived books.
- Added `.xpl` import as a new active book.

## Improved

- Improved `.xpl` preview, filename sanitization, and repeated-import behavior.
- Improved import ID remapping and consistency validation.

## Security & Stability

- Fixed `.xpl` as a gzip-compressed UTF-8 JSON package with size limits to reduce malformed-file risk.

---

# XplorOne v0.2.2

Release date: 2026-04-16

This release improves archived-book migration-package planning and project documentation.

## Improved

- Improved `.xpl` migration-package design notes and import confirmation experience.
- Improved root documentation around current state and implementation boundaries.

---

# XplorOne v0.2.1

Release date: 2026-04-16

This release merges the budget database into the main XplorOne database.

## Changed

- Merged `xplorone-budget.db / budget.db` into the main `xplorone.db`.
- Updated budget pages, home budget summaries, snapshots, restore, CSV, and future `.xpl` flows to rely on main database budget tables.

## Improved

- Improved legacy budget merge behavior so old budget databases are used only as one-time migration sources.
- Improved merge metadata and idempotent imports.

## Security & Stability

- Budget migration now uses a main-database transaction and can safely retry if it fails before completion.

---

# XplorOne v0.2.0

Release date: 2026-04-16

This release starts the XplorOne 0.2 series with MCP, external integration, archived migration, and productization foundations.

## Added

- Added the XplorOne Read-Only MCP v1 baseline.
- Added Codex and WorkBuddy client-token management foundations.
- Added versioned in-repository XplorOne skill content.

## Changed

- External agent queries now prefer Local API / QueryExecutor instead of direct SQLite access.
- MCP is read-only and does not support writes or explicit cross-book queries.

## Improved

- Improved Local API, MCP, Settings, and external-tool documentation boundaries.
- Improved compatibility between structured MCP results and text-channel clients.

## Security & Stability

- MCP client tokens are encrypted with Electron `safeStorage`.
- Local API and MCP lifecycles now distinguish user-started API state from MCP temporary API leasing.

---

# Early Development Releases v0.0.5 - v0.1.9

Release period: 2026-04-01 to 2026-04-16

These versions record XplorOne's transition from early prototype to a local-first desktop finance workspace. For public readability, the many early internal iterations are summarized here as a development-history section.

## Added

- Added core finance modules such as Accounts, Categories, Members, Projects, Transactions, Home Overview, and basic reports.
- Added early AI Query, AI Entry, AI Analysis, and FreeChat flows.
- Added book settings, data settings, budget management, and multi-book foundations.
- Added professional chart types such as treemap, sunburst, waterfall, dual-axis, and heatmap.

## Changed

- Evolved the app from a single-page prototype into a multi-module desktop workspace.
- Reworked navigation, toolbars, charts, and tables across many pages.
- Expanded database, repository, service, and shared contract layers to support books, transactions, reports, and AI chat.

## Improved

- Improved Quick Entry, transaction filters, account management, category management, member/project management, and reports over many iterations.
- Unified page visuals, icons, emoji, buttons, dialogs, filters, and statistic cards.
- Improved model adaptation, query parsing, time-range parsing, and AI response display.

## Fixed

- Fixed multiple early layout, chart, account-category, transaction-filter, and statistic issues.
- Documented duplicate historical tags without inventing release differences.

## Known Issues

- Early release notes were reconstructed from historical tags and commit summaries, so they are less detailed than later releases.
