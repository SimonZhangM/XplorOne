English | [简体中文](./feature-overview_zh-CN.md)

# XplorOne Feature Overview

XplorOne is a local-first AI finance workspace for solopreneurs, freelancers, one-person businesses, consultants, indie makers, and small studios.

This page gives a practical overview of the main product areas.

It is not a step-by-step setup guide.
For your first workflow, see [Getting Started](./getting-started.md).

## Product Navigation Map

The current XplorOne desktop navigation is organized around these main areas:

- **Quick Entry**
- **Home**
- **Calendar**
- **Lists**
  - Ledger
  - Income & Expense
  - Accounts
- **Reports**
  - Cash Flow
  - Income & Expense
  - Assets & Liabilities
- **Chat**
- **Management**
  - Budget
  - Members
  - Projects

This structure reflects the core product idea:

> Start by recording financial activity, then review it through lists, reports, and AI-assisted understanding.

## 1. Quick Entry

Quick Entry is the fastest way to record financial activity.

It is designed for day-to-day bookkeeping, where you want to add a transaction without losing your current workflow.

Typical use cases:

- record an expense
- record income
- choose account and category
- add date and notes
- enter multiple transactions when needed

Quick Entry is usually the best starting point for a new user.

You do not need an API key to use Quick Entry.

## 2. Home Workbench

Home is the main financial workbench.

It is designed to help you quickly understand the current state of your finances and move into common actions.

The Home workbench can show:

- monthly income and expense summary
- asset overview
- daily income and expense trends
- spending category ranking
- recent transactions
- budget reminders
- AI assistant shortcuts
- quick actions such as recording a transaction, viewing the ledger, opening reports, or asking AI

Home is not just a dashboard.
It is the starting point for daily review and action.

## 3. Calendar

Calendar gives a date-based view of financial activity.

It helps you understand when income and expenses happen across the month.

Typical use cases:

- review income and expenses by day
- check daily transaction patterns
- locate financial activity around a specific date
- compare active and quiet days in a month

Calendar is useful when time rhythm matters more than category structure.

## 4. Lists

The Lists section is where you inspect structured financial records.

It includes:

- Ledger
- Income & Expense
- Accounts

### Ledger

Ledger is the transaction list and cash-flow review area.

Use it to:

- review transaction records
- check inflow and outflow
- filter by time range
- inspect account-related activity
- confirm whether transactions were recorded correctly

Ledger focuses on financial movement.
It is the place to inspect what actually happened.

### Income & Expense

Income & Expense helps you review financial activity by category.

Use it to:

- understand income structure
- understand spending structure
- compare categories
- review category-level totals
- jump into related transaction records

This view is useful when you want to know where money came from or where it went.

### Accounts

Accounts helps you review assets, liabilities, and account-level balances.

Use it to:

- organize asset and liability accounts
- review account balances
- understand account structure
- inspect account-related activity
- separate different financial spaces

This is especially useful for users who manage multiple wallets, cards, bank accounts, or business-related accounts.

## 5. Reports

Reports turn raw financial records into higher-level financial views.

The current report navigation includes:

- Cash Flow
- Income & Expense
- Assets & Liabilities

### Cash Flow

Cash Flow focuses on money movement.

Use it to understand:

- cash inflow
- cash outflow
- net flow
- monthly changes
- cash-flow pressure and rhythm

This view is useful when you care about whether money is actually moving in or out of your financial system.

### Income & Expense Reports

Income & Expense reports focus on earning and spending structure.

Use them to understand:

- total income
- total expenses
- net income
- income and expense trends
- category distribution

This is different from Ledger cash flow.
Ledger focuses on movement; Income & Expense reports focus on accounting-style income and expense structure.

### Assets & Liabilities

Assets & Liabilities helps you understand your financial position.

Use it to review:

- assets
- liabilities
- net assets
- account balance trends
- asset and debt structure

This view is especially useful for users who want to understand not only monthly income and expenses, but also longer-term financial state.

## 6. Chat

Chat is the AI-assisted interaction area.

It can support several types of workflows:

- query
- entry drafts
- analysis
- free finance-related conversation

AI features are optional.

XplorOne remains usable without an API key.
Core local bookkeeping, reports, and basic queries work without model configuration.

If you configure your own API key, AI can help with:

- natural-language finance questions
- structured query interpretation
- entry draft preparation
- trend explanation
- broader finance-related analysis

AI does not automatically write to the ledger.
Write actions require user confirmation.

For more details, see:

- [BYOK Setup](./byok-setup.md)
- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md)

## 7. Management

The Management section contains structured financial management areas.

It includes:

- Budget
- Members
- Projects

### Budget

Budget helps you organize expected spending and compare it with actual spending.

Use it to:

- create monthly budgets
- review budget usage
- compare actual expenses against planned limits
- understand remaining budget

Budget is not required for your first workflow, but it becomes useful once you want to move from recording to planning.

### Members

Members help you organize finance-related people or roles.

Use it to:

- manage member records
- connect transactions to people when relevant
- review member-related financial activity

This is useful for households, small studios, or project-based work where money is connected to people.

### Projects

Projects help you organize financial activity by project.

Use it to:

- manage project records
- connect transactions to a project
- review project-related activity
- separate different business or work streams

This is useful for freelancers, consultants, studios, and one-person businesses that handle multiple client or work projects.

## 8. Data Control and Portability

XplorOne includes data management features for long-term control.

Depending on the release state, data-related workflows may include:

- backup
- restore
- export
- import
- archived book migration
- `.xpl` archive package workflows

These features support the local-first product philosophy:

> Your financial workflow should remain portable, recoverable, and under your control.

For privacy and data boundary details, see [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md).

## 9. Local API and MCP

XplorOne also includes local integration capabilities for AI-native workflows.

This area is optional and not required for normal desktop use.

The current MCP/query path is designed for external agents such as Codex or WorkBuddy.

Key boundaries:

- local API and MCP access are token-protected
- MCP access is currently read-only
- MCP queries go through XplorOne’s controlled local API and query layers
- MCP does not directly read the database
- write actions are not exposed through the current MCP path

This makes MCP useful for external agent workflows while keeping the local ledger boundary clear.

For details, see [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md).

## 10. Settings and Personalization

Settings help you adjust the product to your own workflow.

Settings may include:

- model service configuration
- display preferences
- interface language
- personal profile
- data settings
- reminder settings
- archived books
- local API or MCP-related settings
- license or release-related settings, depending on the release channel

Settings are part of the product control layer.
They help define how XplorOne behaves on your machine.

## 11. Current Product Boundaries

XplorOne is currently best understood as:

- a Windows desktop release line
- a local-first finance workspace
- a product for solopreneurs, freelancers, one-person businesses, and small studios
- a finance workspace with optional AI-assisted features
- a desktop product with explicit data and write boundaries

XplorOne is not currently:

- a cloud-first accounting suite
- an enterprise finance system for every region or team
- a full multi-platform release
- a product that requires AI before it can be useful
- a system where AI can automatically mutate your ledger without confirmation

For more details, see [Known Limitations](./known-limitations.md).

## Where to Go Next

- [Getting Started](./getting-started.md) — complete your first workflow
- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md) — understand local data, AI, and integration boundaries
- [BYOK Setup](./byok-setup.md) — configure your own API key for AI-assisted features
- [Known Limitations](./known-limitations.md) — understand current release scope
- [Support](../SUPPORT.md) — learn where to ask questions or report problems
