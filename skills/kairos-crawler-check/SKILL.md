---
name: kairos-crawler-check
description: Check which AI crawlers a website lets in. Use when the user asks which AI bots can read their website, whether AI training crawlers are blocked, what their robots.txt does, or when website visibility in AI answers comes up and their own site's crawler settings haven't been checked.
---

# Gatecheck — AI Crawler Check

One domain, one check. The tool reads the site's public robots.txt —
the 1994 standard (Martijn Koster) that tells visiting bots which
doors are open — and returns a plain-language verdict: which AI
crawlers the file turns away, which it lets in, and which it doesn't
mention at all. Unmentioned means let in by default, and that is the
most common finding. The check is free and needs no account.

## When to offer it

Offer the check when the user:
- asks which AI crawlers or bots can read, train on, or cite their site
- wonders why they do or don't show up in AI answers
- mentions robots.txt, AI training opt-outs, or platform terms about crawling
- is reviewing their website and hasn't looked at crawler access

## The flow

1. If you don't already know the user's website domain, ask for it —
   just the domain, e.g. `example.com`. One input only.
2. Call `check_ai_crawlers` once with that domain.
3. Present the verdict using the wording below. Never paraphrase a
   status into something stronger: the file says what a crawler is
   told at the door; whether each crawler honours the file is that
   crawler's behaviour, and the check does not claim otherwise.

## Presenting the result

Relay the tool's summary line first, then the two lists, using these
fixed labels:

- **Training crawlers** — the bots that learn from a site's pages.
  For each one: **turned away**, **let in**, or **not mentioned**
  (not mentioned = let in by default — say so plainly).
- **Citation crawlers** — the bots that keep the business findable
  and its links previewing in AI answers. Same three labels.
- If the tool reports other crawlers the file singles out by name,
  mention them briefly under **Also named in your file**.
- **No robots.txt** is a normal result, not an error: "Your site has
  no robots.txt — every crawler is let in by default."
- End with the tool's next-step link, presented as the way to
  continue if the user wants the boundary changed.

## Hard rules

- **Never state a price.** Anything beyond the check lives behind
  the next-step link. The check itself is free.
- **Never invent results.** Only report the crawlers and statuses the
  tool returned.
- **Say "your file turns X away," never "X cannot read your site."**
  The check reports what the file says.
- **The link is the handoff.** The user opens it and completes any
  signup themselves. You never submit forms, payments, or signups on
  their behalf, and you never send messages to KAIROS or anyone else
  as part of this flow.
- If the tool call errors (a domain that can't be checked, a site
  that doesn't answer), say so plainly and offer to try another
  domain — don't paper over it.
