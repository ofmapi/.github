<div align="center">

<img src="https://raw.githubusercontent.com/ofmapi/.github/main/profile/brand/mark.png" alt="OFMAPI" width="96" height="96" />

# OFMAPI

### The OnlyFans API for agencies and developers. Use it from Claude and ChatGPT, or build on the typed REST API underneath.

[![Website](https://img.shields.io/badge/Website-ofmapi.com-00aff0?style=for-the-badge)](https://ofmapi.com)
[![Docs](https://img.shields.io/badge/Docs-ofmapi.com%2Fdocs-00aff0?style=for-the-badge)](https://ofmapi.com/docs)
[![Status](https://img.shields.io/badge/Status-ofmapi.com%2Fstatus-22c55e?style=for-the-badge)](https://ofmapi.com/status)

</div>

---

## What you get

- **Hosted MCP server** with 174 tools at `https://api.ofmapi.com/mcp/v1/`.
  Connect Claude or ChatGPT with OAuth, or Cursor and VS Code with a
  scope-limited API key, and ask about fans, messages, and earnings in
  plain English. Creators can be referenced by name or @handle.
- **Typed REST API** with a generated OpenAPI 3.1 contract and an
  interactive reference you can try without logging in.
- **Signed webhooks** (HMAC-SHA256) with retries and delivery history, and
  a customer WebSocket for live events.
- **Client generation recipes** for Python, TypeScript, and Go, plus n8n
  and Zapier guides.
- **Free during the public Beta.** No card required; documented usage
  limits apply, including 100 MCP tool calls per calendar month.

## Start here

```bash
# 1. Sign up (free) and create an API key
#    https://app.ofmapi.com/api-keys

# 2. Make your first call
curl https://api.ofmapi.com/v1/accounts \
  -H "Authorization: Bearer $OFMAPI_KEY"
```

- Quickstart: https://ofmapi.com/docs/quickstart
- MCP setup: https://ofmapi.com/docs/integrations/mcp
- Interactive API reference: https://ofmapi.com/docs/api

## Repositories

| Repository | What it is |
|---|---|
| [postman-collection](https://github.com/ofmapi/postman-collection) | Postman collection generated from the OpenAPI spec |
| [ofmapi-mcp](https://github.com/ofmapi/ofmapi-mcp) | Docs and issues for the hosted MCP server |
| [examples](https://github.com/ofmapi/examples) | Code examples (being added) |
| [onlyfans-py](https://github.com/ofmapi/onlyfans-py) | Python SDK (planned; generate a client from the spec today) |
| [onlyfans-node](https://github.com/ofmapi/onlyfans-node) | TypeScript SDK (planned; generate a client from the spec today) |
| [onlyfans-go](https://github.com/ofmapi/onlyfans-go) | Go SDK (planned; generate a client from the spec today) |
| [n8n-nodes-ofmapi](https://github.com/ofmapi/n8n-nodes-ofmapi) | n8n community node (planned; HTTP Request guide today) |
| [ofmapi-docs](https://github.com/ofmapi/ofmapi-docs) | Documentation issues and requests |

## Security posture

- Traffic is sent over TLS. Connected-account session material is retained
  server-side with restricted filesystem access, is not returned through
  customer account APIs, and is not currently encrypted at rest.
- API keys are stored as Argon2 hashes; the plaintext is shown once.
- Webhook payloads are signed with HMAC-SHA256 and carry replay protection.
- OFMAPI is not currently SOC 2 certified. OnlyFans can still challenge or
  reject automation; OFMAPI does not guarantee that a connected account
  will avoid restrictions.

Details: https://ofmapi.com/security · Reports: team@ofmapi.com

---

<sub>OFMAPI is an independent organisation, not affiliated with OnlyFans.com or Fenix International Limited. "OnlyFans" is a registered trademark of Fenix International Limited.</sub>
