---
name: xquik-x-data
description: "Use Xquik for X data workflows: search posts, fetch user timelines, start extraction jobs, monitor accounts or keywords, and register webhooks through the REST API or MCP endpoint."
license: MIT
metadata:
  author: Xquik
  homepage: https://docs.xquik.com
  repository: https://github.com/Xquik-dev/x-twitter-scraper
  version: "1.0.0"
---

# Xquik X Data

Use this skill when a user needs current X data, bulk extraction, monitoring,
webhook delivery, or a confirmation-gated X action through Xquik.

## Setup

1. Create an API key in the Xquik dashboard.
2. Store it in `XQUIK_API_KEY`.
3. Use `https://docs.xquik.com` as the source of truth for endpoint schemas.

Never ask for X passwords, cookies, recovery codes, or browser exports. Never
paste API keys into chat, logs, commits, issues, or generated files.

## Workflow

1. Identify the task: search, user timeline, extraction, monitor, webhook, or
   write action.
2. Check the current docs for required parameters and response shape.
3. For read-only tasks, keep result limits bounded and explain the target.
4. For monitors, webhooks, exports, or write actions, ask for explicit
   confirmation with the exact target and payload before calling the API.
5. Return concise results with source links or IDs when available.

## Common API Paths

- Search posts: `GET /api/v1/x/tweets/search`
- Fetch user posts: `GET /api/v1/x/users/{id}/tweets`
- Start extraction: `POST /api/v1/extractions`
- Create monitor: `POST /api/v1/monitors`
- Register webhook: `POST /api/v1/webhooks`

## MCP

Use the remote MCP endpoint at `https://xquik.com/mcp` with the same account
authorization model documented at `https://docs.xquik.com/mcp/overview`.

## Example Prompt

```
Use Xquik to find recent public posts about a launch, summarize recurring
themes, and include source post links.
```
