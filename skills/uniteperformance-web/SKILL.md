---
name: uniteperformance-web
description: Find published Unite Performance training, membership prices, centres, events and public terms in Norway.
---

# Unite Performance public information

Use this skill when someone asks about Unite training, HYROX, Functional Fitness, personal training,
centre contacts, age-band prices, events, articles or public membership terms. Norwegian published
copy is authoritative. This skill provides instructions; it does not register a client, grant access,
or perform enrollment.

## Choose the intended site

The current site under evaluation is https://new.uniteperformance.no. Shared preview is
https://dev.uniteperformance.no. Keep discovery navigation on the site the user chose. Check its
`/agent-docs.md` and `/.well-known/ai-catalog.json` before connecting tools. If a deployment does
not yet advertise a capability, use its public Markdown/HTML or report that capability unavailable.
The current canonical SEO origin is https://new.uniteperformance.no. The future production
origin and planned MCP registry identity are https://uniteperformance.no. Until the separately
approved apex cutover, do not move tool requests to the Squarespace site.

## Find published facts

Start at `/llms.txt` or `/index.md`. Read `/pricing.md` for prices and `/contact` for centre contacts.
Section indexes are `/trening/llms.txt`, `/sentrene/llms.txt`, `/arrangementer/llms.txt`,
`/artikler/llms.txt` and `/vilkar/llms.txt`. A missing document is unavailable; never substitute a
private page, a guessed price, or a zero amount.

Where advertised, initialize the selected site's `/mcp`, then use `tools/list` and `tools/call`.
Browser agents may use WebMCP when the browser exposes the supported native API. The HTTP
contracts are at `/openapi.json`; public tool inventory is `/api/public/tools`.

The five public tools are:

- `get_membership_prices`: filter reviewed public offers by age and centre. Keep the annual fee
  separate from monthly training and PT; do not combine unrelated products into an invented bundle.
- `get_centres`: published addresses, contact information and supported timetable links.
- `get_training_options`: published training explanations and adaptations.
- `list_events`: dated events, status and supported participation links. Missing times are unknown.
- `search_public_content`: bounded retrieval of published public content and current public terms.

Cite each result's source URL and review date. A null review date is unknown, not today's date.
Check that a participation link is supported and current before offering it as a handoff. Enrollment
for ages 12–17 is guardian-led; adults may enroll themselves in their reviewed age band. Agreement
acceptance and optional marketing consent are separate decisions. Privacy notices retain their
published review status; a notice marked in review is not an approved agreement.

## Respect the limits

All five tools are public reads. They expose no customer, family, employee, payroll, financial,
booking-availability or payment-status data. They do not enroll, sign, book, pay, activate a membership,
or send messages. Never use M2M credentials to impersonate a member or employee. Do not request
passwords, login codes, cookies or tokens. For authenticated limitations, read `/auth.md`; no generic
external-agent delegation flow is accepted merely because a discovery document exists.

Respect the chosen deployment's robots and noindex policy. A public-launch decision, crawler
permission, training permission and machine commerce support are separate from these instructions.
