# Unite Performance public agent skill

Find published Unite Performance training, prices, centres, events and public terms in Norway.
This package contains instructions for public information only. It includes no login flow,
private data, execution hooks or scripts.

## Install

Review `skills/uniteperformance-web/SKILL.md`, then install the skill for a supported agent:

```sh
bunx skills add frodeste/uniteperformance-agent-skills --skill uniteperformance-web
```

Alternatively, install the skill directly from the public website:

```sh
bunx skills add https://new.uniteperformance.no --skill uniteperformance-web
```

The same directory is a Claude Code plugin:

```sh
claude plugin validate .
claude --plugin-dir .
```

The instructions discover the selected site's current capabilities before using its public
Markdown, HTTP, MCP or native WebMCP tools. An agent client must support the interface it uses.
The plugin itself does not register tools or perform enrollment, bookings, payments or messages.

## Published sources

- [Public developer guide](https://new.uniteperformance.no/developers)
- [Agent instructions](https://new.uniteperformance.no/agent-docs.md)
- [Published information index](https://new.uniteperformance.no/llms.txt)
- [Public HTTP contract](https://new.uniteperformance.no/openapi.json)
- [Authentication limits](https://new.uniteperformance.no/auth.md)

Norwegian published information and its review status remain authoritative. A missing fact or
capability is unavailable. Review dates are not inferred from installation dates.

## Policy

Public search and user-requested agents are allowed; model training is prohibited. Preserve the
site's current crawl and noindex policy. Private customer, family, employee, payroll and financial
information is outside this package. Never request passwords, login codes, session cookies or
tokens to impersonate a user.

## Directory listing

The published [skills.sh listing](https://skills.sh/frodeste/uniteperformance-agent-skills/uniteperformance-web)
links this repository and skill. A directory listing is not a security endorsement or audit.
The future production identity is https://uniteperformance.no; use the current new-site tools
until the separately approved apex cutover.
