English | [简体中文](./byok-setup_zh-CN.md)

# BYOK Setup

BYOK means **Bring Your Own Key**.

In XplorOne, this means you can connect the app to a model service using your own model API key.

A model API key is optional.
XplorOne can still be used for core local bookkeeping, reports, financial views, and basic local queries without an API key.

## 1. What BYOK Is For

A model API key is only required for AI-assisted features.

Depending on your enabled workflows, AI-assisted features may include:

- AI Assistant analysis and explanation
- broader finance-related chat workflows
- model-assisted interpretation in workflows that explicitly use AI
- entry draft assistance where model participation is enabled

Local Assistant query remains a local-first workflow and does not require an API key for supported local queries.

You do **not** need a model API key for:

- local bookkeeping
- Quick Entry
- books, accounts, categories, and transactions
- reports and financial views
- basic local queries
- backup, restore, export, import, and archive workflows where available

In short:

> XplorOne works as a local-first finance workspace without an API key.
> The API key only unlocks AI-assisted capabilities on top of the core local workflow.

## 2. What You Need Before Setup

Before configuring a model service, prepare:

- provider or service name
- base URL
- model name
- API key

XplorOne is designed around OpenAI-compatible model-service configuration patterns.

Different providers may use different:

- endpoint formats
- model names
- rate limits
- billing rules
- response behavior

Please check your model provider’s own documentation if you are unsure about the correct base URL or model name.

## 3. How to Configure a Model API Key

Open XplorOne and go to:

`Settings -> Model Service`

Then complete the configuration:

1. choose a provider preset or custom provider
2. enter the base URL
3. enter the model name
4. enter your API key
5. save the AI configuration
6. test the connection
7. activate the current configuration

XplorOne separates these actions:

- **Save AI Config** stores the current draft configuration
- **Test Connection** checks whether the current configuration can call the model service
- **Activate Current Config** sets the current configuration as the model used by AI workflows

Saving a configuration does not always mean it is already active.
If AI features are not using the expected model, check which configuration is currently activated.

## 4. Try Your First AI Assistant Workflow

After activating the model configuration, you can try an AI Assistant workflow in Chat.

Example questions:

> Summarize my income and expenses this month.

> Explain why my dining expenses increased this quarter.

> What patterns should I review before planning next month's budget?

Supported Local Assistant queries are handled by the local query kernel without requiring a model API key.
AI Assistant is used when you intentionally enter model-assisted analysis or broader finance-related conversation.

## 5. API Key Storage

Model API keys are treated as sensitive local credential data.

XplorOne stores model credentials through Electron `safeStorage` or an equivalent system-protected local credential mechanism.

Model API keys are not intended to be stored as plain text in the ledger database.

Non-sensitive configuration metadata may be stored locally, such as:

- provider name
- base URL
- model name
- enabled status
- configuration state

These metadata fields help XplorOne remember which model configuration to use, without treating the API key as ordinary ledger data.

For more details, see [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md).

## 6. API Key and Local Tokens Are Different

A model API key is not the same thing as a Local API token or MCP token.

- **Model API key**
  Connects XplorOne to the model service chosen by the user.

- **Local API token**
  Protects access to XplorOne’s local HTTP API.

- **MCP client token**
  Authorizes external agents such as Codex or WorkBuddy to access XplorOne’s local read-only MCP/query path.

BYOK setup is only about model API keys.

Local API and MCP tokens are managed separately and are not required for normal desktop use.

## 7. Replacing or Removing an API Key

You can replace or remove your model API key from the model service settings.

You may want to do this if:

- the key has expired
- the key was exposed
- you changed model providers
- you want to use another model
- the provider account or billing state changed

If an API key may have been exposed, also rotate or revoke it in the provider’s own console.

## 8. Backup and Migration Notes

XplorOne may include protected credential metadata in some full-app backup workflows.

However:

- exported ledger files should not expose API keys as plain text
- protected credential backups are not the same as portable plain-text key exports
- credential recovery may depend on the current machine or operating-system credential environment
- when moving to another machine, you may need to reconfigure your model API key

If you are moving XplorOne data between machines, plan to re-enter or re-test your model configuration after migration.

## 9. Common Setup Problems

### The connection test fails

Check:

- whether the API key is correct
- whether the base URL is correct
- whether the model name exists for that provider
- whether the provider account has enough credits or quota
- whether the provider requires a special endpoint format
- whether the network connection is available

### AI features still do not work after saving

Saving a configuration and activating it are different actions.

Check whether you have activated the current configuration.

### The provider returns unexpected output

Different models and providers may behave differently.

Some providers may:

- return text instead of strict JSON
- include reasoning or wrapper text
- require provider-specific request settings
- handle temperature or structured output differently

XplorOne includes compatibility handling for some model behaviors, but provider behavior may still vary.

### The response language is not what you expected

XplorOne may consider:

- your current message language
- previous clear user language in the same session
- UI language as fallback

If language behavior looks wrong, include the input language, UI language, provider, and expected response language when reporting the issue.

## 10. Security Tips

Please do not:

- share your API key
- paste your API key into public issues
- commit your API key to GitHub
- include your API key in screenshots
- send your API key to third parties

If you need support, remove sensitive information from logs, screenshots, and examples before posting.

If a key may have been exposed, revoke or rotate it through your model provider.

## 11. What BYOK Does Not Mean

BYOK does not mean:

- XplorOne requires AI before it can be useful
- XplorOne includes free model credits
- XplorOne controls your model provider account
- AI can automatically write to your ledger
- all local data is sent to the model provider by default

BYOK only means:

> You can choose and configure your own model service for optional AI-assisted workflows.

## Where to Go Next

- [Getting Started](./getting-started.md) — complete your first workflow
- [Feature Overview](./feature-overview.md) — understand the main product areas
- [Privacy & AI Boundaries](./privacy-and-ai-boundaries.md) — understand local data, AI, and integration boundaries
- [Known Limitations](./known-limitations.md) — understand current release scope
- [Support](../SUPPORT.md) — learn where to ask questions or report problems
