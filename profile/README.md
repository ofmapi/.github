<div align="center">

<img src="https://raw.githubusercontent.com/ofmapi/.github/main/profile/brand/mark.png" alt="OnlyFans API by OFMAPI" width="96" height="96" />

# OnlyFans API for developers and agencies

### Typed REST endpoints, signed webhooks, and a hosted MCP server that lets Claude, ChatGPT, Cursor, and VS Code work with OnlyFans fans, messages, and earnings. Built by OFMAPI. Free during the public Beta.

[![Website](https://img.shields.io/badge/OnlyFans_API-ofmapi.com-CC97FF?style=for-the-badge)](https://ofmapi.com)
[![Docs](https://img.shields.io/badge/Docs-ofmapi.com%2Fdocs-CC97FF?style=for-the-badge)](https://ofmapi.com/docs)
[![API reference](https://img.shields.io/badge/API_reference-try_without_login-CC97FF?style=for-the-badge)](https://ofmapi.com/docs/api)
[![Status](https://img.shields.io/badge/Status-ofmapi.com%2Fstatus-22c55e?style=for-the-badge)](https://ofmapi.com/status)

</div>

---

## What the OnlyFans API does

OnlyFans has no public developer API. OFMAPI is an independent, unofficial
OnlyFans API: a creator (or the agency managing them) connects their own
OnlyFans account once, and from then on every part of that account is
available as a typed HTTPS API, as webhook events, and as tools inside AI
assistants.

- **Fans and subscribers**: list fans, subscription state, spend history,
  lists, notes, and tags.
- **Messages and chats**: read conversations, send direct messages and paid
  PPV messages, mass messaging through OnlyFans' own scheduler, saved
  messages, message queues.
- **Posts, vault, and stories**: publish and schedule posts, upload media,
  manage the vault, post stories.
- **Earnings and statistics**: transactions, balances, earnings charts,
  monthly statements, reach and engagement.
- **Live events**: signed webhooks and a customer WebSocket for new
  messages, tips, subscriptions, likes, and more.
- **AI assistants**: a hosted MCP server with 174 tools, so an assistant can
  answer "who are my top spenders this week" or draft a re-engagement DM
  without any code.

Everything returns a stable, typed schema that OFMAPI maintains as the
customer contract; the raw upstream payload is available on request for
debugging.

## Start in five minutes

```bash
# 1. Create a free account and an API key
#    https://app.ofmapi.com/api-keys

# 2. Connect an OnlyFans account in the dashboard, then list it
curl https://api.ofmapi.com/v1/accounts \
  -H "Authorization: Bearer $OFMAPI_KEY"
```

- Quickstart: https://ofmapi.com/docs/quickstart
- Interactive API reference (no login): https://ofmapi.com/docs/api
- OpenAPI 3.1 spec: https://ofmapi.com/openapi.json
- Webhooks: https://ofmapi.com/docs/webhooks
- Rate limits and Beta usage limits: https://ofmapi.com/docs/rate-limits

## Use the OnlyFans API from AI assistants (MCP)

The MCP server is hosted; there is nothing to install.

```
https://api.ofmapi.com/mcp/v1/
```

Claude and ChatGPT connect with OAuth; Cursor, VS Code, and other
config-based hosts use a scope-limited API key. Creators can be referenced
by name or @handle. Setup for every host: https://ofmapi.com/docs/integrations/mcp

## Repositories

| Repository | What it is |
|---|---|
| [ofmapi-mcp](https://github.com/ofmapi/ofmapi-mcp) | OnlyFans API MCP server: config files and issues for the hosted server |
| [examples](https://github.com/ofmapi/examples) | OnlyFans API code examples: webhook receivers, send a message, export earnings |
| [postman-collection](https://github.com/ofmapi/postman-collection) | OnlyFans API Postman collection generated from the OpenAPI spec |
| [onlyfans-py](https://github.com/ofmapi/onlyfans-py) | OnlyFans API for Python: typed client generation recipe |
| [onlyfans-node](https://github.com/ofmapi/onlyfans-node) | OnlyFans API for TypeScript and Node.js: typed client generation recipe |
| [onlyfans-go](https://github.com/ofmapi/onlyfans-go) | OnlyFans API for Go: typed client generation recipe |
| [n8n-nodes-ofmapi](https://github.com/ofmapi/n8n-nodes-ofmapi) | OnlyFans API in n8n: HTTP Request and Webhook node guide |
| [ofmapi-docs](https://github.com/ofmapi/ofmapi-docs) | Documentation issues and requests |

## Frequently asked

**Is there an official OnlyFans API?**
No. OnlyFans does not publish a developer API. OFMAPI is an independent
service that works with the creator's own login and is not affiliated with
OnlyFans.com or Fenix International Limited.

**What can I build with the OnlyFans API?**
Chatbots and AI assistants for fan messaging, agency CRMs and dashboards,
mass-messaging and PPV tooling, earnings analytics, content scheduling,
and automations in n8n or Zapier. The examples repository has working
webhook receivers and scripts.

**How do I get an OnlyFans API key?**
Sign up at https://app.ofmapi.com, connect an OnlyFans account, and create
a key under API keys. Keys are scoped and stored as Argon2 hashes; the
plaintext is shown once.

**Does the OnlyFans API work with ChatGPT and Claude?**
Yes, through the hosted MCP server. Add `https://api.ofmapi.com/mcp/v1/`
as a connector or app, authorize with OAuth, and ask questions in plain
English.

**Is there a Python, Node, or Go SDK?**
Not published yet. Generate a typed client from the OpenAPI 3.1 spec in
about a minute; each SDK repository has the exact commands. Do not install
the unrelated `onlyfans` packages on PyPI or npm expecting an OFMAPI client.

**What does the OnlyFans API cost?**
Nothing during the public Beta. No card is required; documented usage
limits apply, including 100 MCP tool calls per calendar month.

**Can a connected account get restricted?**
OnlyFans can still challenge or reject automation. OFMAPI does not
guarantee that a connected account will avoid restrictions. The current
security posture, including how session material is stored, is documented
at https://ofmapi.com/security.

## Contact

Questions, bugs, integration requests, and security reports go through
https://ofmapi.com/contact (customers can open tickets from the dashboard).
Replies arrive by email.

---

<sub>OFMAPI is an independent organisation, not affiliated with OnlyFans.com or Fenix International Limited. "OnlyFans" is a registered trademark of Fenix International Limited.</sub>
