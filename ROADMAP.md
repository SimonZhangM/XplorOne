English | [简体中文](./ROADMAP_zh-CN.md)

# XplorOne Roadmap

This roadmap describes the current product direction for XplorOne.

It is directional, not a delivery promise.
Priorities may change based on product stability, user feedback, technical constraints, and release readiness.

XplorOne is currently focused on becoming a reliable local-first desktop finance workspace for solopreneurs, freelancers, one-person businesses, consultants, indie makers, and small studios.

## Guiding Principles

XplorOne’s roadmap follows several product principles:

- **Local-first by default**
  Core financial records should remain under the user’s control.

- **Desktop workflow first**
  The current official release line focuses on the desktop application.

- **AI as an optional enhancement**
  XplorOne should remain useful without a model API key. AI features enhance query, entry drafts, and analysis, but do not replace the core local workflow.

- **Explicit write boundaries**
  AI can assist with interpretation, analysis, and draft preparation, but write actions require user confirmation.

- **Clear data and integration boundaries**
  Local API and MCP integrations should remain controlled, token-protected, and explicit.

- **Practical finance workflows over feature sprawl**
  The goal is not to become an all-in-one enterprise accounting suite, but to help independent operators understand and manage their financial reality.

---

## Now

The current focus is to verify the v0.4.x Windows release line and keep the public product hub accurate as the desktop product continues to move forward.

### v0.4.x Windows release verification

Current priorities include:

- verifying the Windows desktop release after each software update
- checking installer behavior, startup behavior, and update paths
- keeping release artifacts free of private runtime data, credentials, tokens, and local databases
- publishing clear release notes, checksums, and download guidance where available
- making sure GitHub Releases, Changelog, and Software Release History stay aligned

### Installer, auto-update, and release trust

Current priorities include:

- keeping installer and auto-update behavior predictable
- clarifying official download channels
- improving user-facing release notes
- documenting security and privacy boundaries around downloads, backups, logs, and support files
- maintaining legal and third-party notice files as public trust materials

### Import foundation and first-user onboarding

Current priorities include:

- improving the first-use path from download to first book
- clarifying Quick Entry, Home, Transactions, Reports, and Budget workflows
- preparing the import foundation for real-world statements and payment-platform exports
- improving backup, restore, export, archive, and migration explanations
- reducing places where users might misunderstand current release scope

The near-term product goal is simple:

> Users should be able to record financial activity, review their books, and understand their current financial state without needing AI.

### AI Assistant behavior polish

Current priorities include improving:

- Local Assistant and AI Assistant separation
- bilingual AI behavior
- model configuration clarity
- response language behavior
- AI analysis discipline and financial-risk boundaries
- safer confirmation flows for write-related workflows

AI remains optional.
Core local bookkeeping, reports, and supported local queries should continue to work without a model API key.

### Documentation maintenance

The GitHub product hub foundation is now in place.

Current documentation work is focused on maintenance rather than first-time scaffolding:

- keeping README, FAQ, Support, Roadmap, and Known Limitations current
- keeping Privacy, Security, AI, MCP, and data-storage docs aligned with implementation
- keeping screenshots and WAIC materials accurate
- keeping issue templates and community entry points useful

---

## Next

The next stage focuses on making XplorOne more useful for real-world financial data and stronger as an AI-assisted local finance workspace.

### Bank statement and mainstream payment import

This is a key Next-stage priority.

XplorOne should improve import support for real-world statements and export files from banks and mainstream payment tools.

The focus includes:

- bank statement import
- mainstream payment tool import
- better CSV and spreadsheet import handling
- format detection and mapping
- import preview
- duplicate detection
- user confirmation before final import
- safer review of imported transactions
- clearer import error messages

The goal is not to claim support for every financial institution or payment platform immediately.

The goal is to build a reliable import foundation that can gradually support common real-world formats and help users move from historical records into a structured local ledger.

### AI query and entry draft improvement

Future AI improvements may include:

- better local-first query routing
- stronger natural-language understanding
- more accurate time-range interpretation
- better category and account matching
- improved entry draft correction
- clearer missing-field prompts
- better bilingual query behavior
- more useful explanations of financial results

Write boundaries remain unchanged: AI-generated write actions require user confirmation.

### Reports and financial views

Future report improvements may include:

- clearer cash-flow views
- stronger income and expense analysis
- better assets and liabilities visibility
- improved chart explanations
- better navigation from reports to underlying transactions
- more consistent bilingual labels and terminology

The goal is to help users understand patterns, not just view numbers.

### Data control and portability

Future work may include:

- improved backup and restore clarity
- better export options
- stronger archive workflows
- safer import validation
- clearer migration guidance
- better handling of cross-machine credential boundaries

XplorOne should continue to treat financial data and credential data differently.

### BYOK and model provider experience

Future work may include:

- clearer model-provider setup guidance
- improved connection testing
- better error messages
- more provider compatibility handling
- better response-language handling
- clearer distinction between model API keys and local integration tokens

The core product should remain usable without a model API key.

### Local MCP and external agent workflows

Future work may include:

- improving the local read-only MCP workflow
- better documentation for Codex and WorkBuddy usage
- clearer MCP status and token management
- improved structured result formats
- better agent-facing query examples
- stronger separation between user-facing desktop workflows and external agent workflows

Current MCP direction remains read-only.

---

## Later

Later-stage work may include broader product expansion after the core workflow becomes stable.

### macOS and additional platform evaluation

XplorOne may evaluate additional platform support in the future.

However:

- Windows remains the current official release line
- macOS, Linux, mobile, or browser end-user releases should not be assumed available unless explicitly published
- platform expansion should not come at the cost of core product stability

### More advanced import coverage

After the import foundation becomes stable, XplorOne may gradually expand coverage for additional statement types, export formats, and payment workflows.

### Deeper financial analysis

Later-stage analysis may include:

- stronger period comparison
- better project-based financial views
- better member-related analysis
- deeper cash-flow interpretation
- improved financial health summaries
- more useful recommendations based on local ledger structure

These features should remain grounded in user-controlled data and clear AI boundaries.

### More agent and integration workflows

XplorOne may continue exploring external agent workflows, local skills, and controlled integration paths.

The product direction remains:

- local-first
- token-protected
- explicit
- user-confirmed for write-related operations

---

## Not Currently Planned as Core Direction

XplorOne is not currently trying to become:

- a cloud-first accounting suite
- a hosted multi-user accounting platform
- a full enterprise finance system for every region
- a tax filing product
- a legal or accounting compliance service
- a product that requires AI before it can be useful
- a system where AI can automatically mutate ledger data without confirmation

These are intentional boundaries, not temporary omissions.

---

## How to Give Roadmap Feedback

Roadmap feedback is welcome.

The most useful feedback explains:

- what problem you are trying to solve
- what workflow you are using today
- what is missing in XplorOne
- whether the need is personal, freelance, studio, or business-related
- whether the request relates to bookkeeping, import, reports, AI, MCP, backup, or settings

Use:

- [Discussions](https://github.com/SimonZhangM/XplorOne/discussions) for roadmap ideas and product discussion
- [Issues](https://github.com/SimonZhangM/XplorOne/issues) for clear bugs and actionable problems
- [Support](./SUPPORT.md) for support guidance

Please do not post private financial data, API keys, Local API tokens, MCP tokens, license codes, or unredacted screenshots publicly.
