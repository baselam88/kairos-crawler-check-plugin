# Gatecheck — AI Crawler Check, plugin for Grok Bot, Cursor, and MCP hosts

**What it does.** Gatecheck reads your website's public robots.txt
and tells you, in plain language, which AI crawlers you've let in.
Two lists come back:

- **Training crawlers** — the bots that learn from your site's pages.
- **Citation crawlers** — the bots that keep your business findable
  and its links previewing in AI answers.

Every known crawler is marked **turned away**, **let in**, or **not
mentioned** — and not mentioned means let in by default, which is the
most common finding. A site with no robots.txt at all gets a straight
answer too: every crawler is let in by default.

robots.txt has been the web's front-door list since Martijn Koster
published the standard in 1994. Gatecheck simply reads yours the way
an AI company would, and translates it.

The check is free, needs no account, and quotes no prices in chat. It
ends with a next-step link; anything beyond the check happens only if
you open it and sign up yourself.

**Tools**

| Tool | Label | What it does |
|---|---|---|
| `check_ai_crawlers` | Read | Takes one domain and returns the two-part verdict, a one-line meaning, and the next-step link |

**Configure variables.** None. The check endpoint is public and
rate-limited; no key, no sign-in, no credentials of yours are ever
requested or stored.

**Privacy.** The check reads one public file — the robots.txt any
visitor can see — and stores nothing about you. The verdict reports
what your file says; whether each crawler honours the file is that
crawler's behaviour.

## Test locally

The package points at the hosted endpoint in `mcp.json`. To exercise
the tool from any MCP client, add the server from `mcp.json` and ask
your agent: "Check my site's AI crawlers" — then give it a domain.
Try `kairosasi.com`: its split is set deliberately.

Cursor IDE local load:

```bash
ln -s /path/to/kairos-crawler-check ~/.cursor/plugins/local/kairos-crawler-check
```

Then reload the window and confirm the `kairos-crawler-check` skill
and MCP server load.

## Submit

- Grok Bot / Cursor marketplace: https://x.ai/bot/marketplace/submit-a-plugin
- License: MIT (see LICENSE) — the plugin package is open; the check
  service itself is hosted by KAIROS AI Systems.

Built by KAIROS AI Systems — https://kairosasi.com
