# ForceDream

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ForceDream Ltd (UK Company No. 17057770, London) operates a paid, verifiable AI-agent marketplace it calls the ForceDream Intelligence OS: specialist agents for summarisation, structured-data extraction, code generation, security scanning, lead scoring, translation, classification, sentiment and forecasting, each priced per call in GBP pence, with 78% of the margin routed to the agent's developer and every completed execution Ed25519-signed so a third party can verify what ran, which model served it and what it cost without an account. The same catalogue is reachable three ways: a REST API on api.forcedream.ai (an 8-operation, SDK-verified OpenAPI 3.1 published on GitHub; a 206-route reference on the docs site), a remote Model Context Protocol server at https://api.forcedream.ai/v1/mcp that answers an anonymous tools/list with 21 tools (5 keyless) and gates paid tools behind OAuth 2.1 + PKCE with RFC 7591 dynamic client registration, and an A2A 1.0 agent card at /.well-known/agent-card.json declaring 18 skills. Twelve first-party SDKs, a Go CLI, a Homebrew tap and a documented webhook surface round out the developer program.

**Areas:** AI Agents · Agent Marketplace · MCP · A2A · Cryptographic Proofs · AI Inference Routing · Agentic Payments · Agentic Commerce · Agent-Native · United Kingdom

## ForceDream on APIs.io

Everything profiled for ForceDream is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/forcedream-ai/](https://apis.io/providers/forcedream-ai/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [ForceDream MCP Server](https://apis.io/apis/forcedream-ai/forcedream-mcp-server/) — Remote Model Context Protocol server at https://api.forcedream.ai/v1/mcp (Streamable HTTP, protocol version 2025-06-18, serverInfo forcedream 0.12.1) with a…
- [ForceDream A2A Agent](https://apis.io/apis/forcedream-ai/forcedream-a2a-agent/) — Agent2Agent (A2A) protocol surface: a signed (ES256 JWS, kid in /.well-known/jwks.json) agent card served from…
- [ForceDream Account API](https://apis.io/apis/forcedream-ai/forcedream-ai-account-api/) — The Account API from ForceDream — 1 operation(s) for account.
- [ForceDream Agents API](https://apis.io/apis/forcedream-ai/forcedream-ai-agents-api/) — The Agents API from ForceDream — 4 operation(s) for agents.
- [ForceDream Signup API](https://apis.io/apis/forcedream-ai/forcedream-ai-signup-api/) — The Signup API from ForceDream — 1 operation(s) for signup.
- [ForceDream Workforce API](https://apis.io/apis/forcedream-ai/forcedream-ai-workforce-api/) — The Workforce API from ForceDream — 2 operation(s) for workforce.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [ForceDream Webhooks](https://apis.io/asyncapis/forcedream-ai/forcedream-ai-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/webhooks/forcedream](https://apis.io/channels/forcedream-ai/webhooks-forcedream/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [ForceDream](https://apis.io/servers/forcedream-ai/forcedream/)

#### Overlays (5)

OpenAPI overlays, including conversational phrasing for each operation.

- [Forcedream Ai Account Api Phrasing Overlay](https://apis.io/overlays/forcedream-ai/forcedream-ai-account-api-phrasing-overlay/)
- [Forcedream Ai Agents Api Phrasing Overlay](https://apis.io/overlays/forcedream-ai/forcedream-ai-agents-api-phrasing-overlay/)
- [Forcedream Ai Openapi Overlay](https://apis.io/overlays/forcedream-ai/forcedream-ai-openapi-overlay/)
- [Forcedream Ai Signup Api Phrasing Overlay](https://apis.io/overlays/forcedream-ai/forcedream-ai-signup-api-phrasing-overlay/)
- [Forcedream Ai Workforce Api Phrasing Overlay](https://apis.io/overlays/forcedream-ai/forcedream-ai-workforce-api-phrasing-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Forcedream Ai Authentication](https://apis.io/security/forcedream-ai/forcedream-ai-authentication/)
- [Forcedream Ai Domain Security](https://apis.io/security/forcedream-ai/forcedream-ai-domain-security/)
- [Forcedream Ai Trust Center](https://apis.io/security/forcedream-ai/forcedream-ai-trust-center/)
- [Forcedream Ai Vulnerability Disclosure](https://apis.io/security/forcedream-ai/forcedream-ai-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Forcedream Ai Scopes](https://apis.io/scopes/forcedream-ai/forcedream-ai-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Forcedream Ai Plans Pricing](https://apis.io/plans/forcedream-ai/forcedream-ai-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Forcedream Ai Rate Limits](https://apis.io/rate-limits/forcedream-ai/forcedream-ai-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://forcedream.ai/)
- [Documentation](https://www.forcedream.com/developers/docs)
- [Getting started](https://www.forcedream.com/developers/quickstart)
- [API reference](https://www.forcedream.com/developers/api)
- [Pricing](https://www.forcedream.com/pricing)
- [Sign up](https://www.forcedream.com/earn)
- [Support](https://www.forcedream.com/contact)
- [Changelog](https://www.forcedream.com/changelog)
- [Blog](https://www.forcedream.com/blog)
- [Trust centre](https://www.forcedream.com/trust)
- [Terms of service](https://www.forcedream.com/terms)
- [Privacy policy](https://www.forcedream.com/privacy)
- [GitHub](https://github.com/forcedreamai)
- [Status](https://www.forcedream.com/status)

## API Evangelist rating

**Kin Score 72.4** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 44.8 |
| Contract governance | 18.2 |
| Operational transparency | 94.7 |
| Developer ergonomics | 80.4 |
| Access clarity | 92.1 |

**Agent readiness 51.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | conformant |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 55.4** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/forcedream-ai/](https://apis.io/providers/forcedream-ai/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ForceDream: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/forcedream-ai/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
