English | [简体中文](./getting-started_zh-CN.md)

# Getting Started with XplorOne

XplorOne is a local-first AI finance workspace for solopreneurs, freelancers, one-person businesses, consultants, indie makers, and small studios.

This guide helps you complete your first usable workflow:

1. download and install XplorOne
2. create or open a book
3. understand the Home workbench
4. record your first transaction with Quick Entry
5. review your transactions
6. open reports and financial views
7. optionally enable AI features
8. optionally explore local MCP for external agents

This is not a full feature manual.  
For a broader feature map, see [Feature Overview](./feature-overview.md).

## 1\. Download and Install

Download the latest Windows release from [GitHub Releases](https://github.com/SimonZhangM/XplorOne/releases).

After downloading:

1. run the installer
2. complete the installation
3. launch XplorOne

If Windows shows a security prompt, make sure you downloaded the installer from the official release page in this repository.

## 2\. Create or Open Your First Book

A book is the main workspace for your financial records.

Inside a book, you can manage:

* accounts
* categories
* transactions
* reports and financial views

When you launch XplorOne for the first time, create a new book or open an existing one.

You do not need an API key to complete this step.

## 3\. Understand the Home Workbench

The Home page is your financial workbench.

It is designed to help you quickly understand your current financial state and move into common actions.

From the Home workbench, you can typically review:

* monthly income and expenses
* asset overview
* daily income and expense trends
* spending category rankings
* recent transactions
* quick actions such as recording a transaction, viewing transactions, opening reports, or asking AI

The Home page is not just a dashboard.  
It is the starting point for daily financial work.

## 4\. Use Quick Entry for Your First Transaction

The easiest way to begin is to record one transaction with Quick Entry.

You can start from:

* the **Quick Entry** entry in the left sidebar
* the **Quick Entry** shortcut on the Home workbench

For your first transaction, keep it simple:

1. choose the transaction type
2. enter the amount
3. select the account
4. select the category
5. set the date
6. add a note if needed
7. save the transaction

After saving, your transaction becomes part of the local ledger.

You do not need an API key to record transactions.

## 5\. Review Your Transactions

After recording your first transaction, open the transaction list.

You can use the list pages to review:

* transaction records
* income and expense flow
* account-related activity
* category-related activity

This helps you confirm that your first record was saved correctly and gives you a basic view of how XplorOne organizes financial data.

## 6\. Open Reports and Financial Views

After you have a few records, open reports and financial views to understand your data more clearly.

You can review:

* income and expenses
* cash flow
* assets and liabilities
* account states
* category structure
* charts and trends

Reports and financial views are part of the core local workflow.  
They do not require an API key.

## 7\. Optional — Enable AI Features

AI features are optional.

XplorOne remains usable as a local-first finance workspace even without an API key.  
You can still record transactions, review reports, use local views, and run basic queries.

Add your own API key only if you want AI Assistant capabilities such as:

* financial analysis
* trend explanation
* model-assisted interpretation in workflows that explicitly use AI
* entry draft assistance where model participation is enabled
* broader finance-related chat workflows

Local Assistant query and entry workflows remain local-first where supported by the local kernel.

AI Assistant can help with analysis and broader finance-related conversation, but write actions require confirmation.
Nothing is written automatically by AI.

For setup details, see [BYOK Setup](./byok-setup.md).  
For privacy and boundary details, see [Privacy \& AI Boundaries](./privacy-and-ai-boundaries.md).

## 8\. Optional — Use Local MCP for External Agents

Local MCP is optional and intended for external agent workflows.

If you use tools such as Codex or WorkBuddy, XplorOne can provide a token-protected local read-only MCP/query path.

This is not required for:

* local bookkeeping
* recording transactions
* viewing reports
* basic queries
* using XplorOne’s normal desktop workflow

The current MCP path is read-only and goes through XplorOne’s controlled local API and query layers rather than reading the database directly.

For a high-level introduction, see [Feature Overview](./feature-overview.md).  
For data and integration boundaries, see [Privacy \& AI Boundaries](./privacy-and-ai-boundaries.md).

## 9\. Where to Go Next

After completing your first workflow, you can continue with:

* [Feature Overview](./feature-overview.md) — understand the main product areas
* [Privacy \& AI Boundaries](./privacy-and-ai-boundaries.md) — understand local data, AI, and integration boundaries
* [BYOK Setup](./byok-setup.md) — configure your own model API key for AI-assisted features
* [Known Limitations](./known-limitations.md) — understand the current release scope
* [Support](../SUPPORT.md) — learn where to ask questions or report problems

## Need Help?

Use:

* [Discussions](https://github.com/SimonZhangM/XplorOne/discussions) for questions, feedback, ideas, and product discussion
* [Issues](https://github.com/SimonZhangM/XplorOne/issues) for bug reports, installer problems, and clearly actionable issues
* [Releases](https://github.com/SimonZhangM/XplorOne/releases) for downloads and release notes

