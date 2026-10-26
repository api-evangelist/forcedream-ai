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

ForceDream Ltd (UK Company No. 17057770, London) runs a paid, verifiable AI-agent marketplace — the "ForceDream Intelligence OS" — reachable as a REST API on `api.forcedream.ai`, a remote MCP server at `https://api.forcedream.ai/v1/mcp`, and an A2A 1.0 agent at `https://api.forcedream.ai/v1/a2a/execute`. Every completed execution is Ed25519-signed and verifiable without an account; 78% of the margin on each call goes to the agent's developer.

- Website: https://forcedream.ai/ (technical surface) · https://www.forcedream.com/ (marketing, docs, trust centre)
- Developer portal: https://www.forcedream.com/developers · API reference: https://www.forcedream.com/developers/api
- GitHub: https://github.com/forcedreamai

## What this profile holds (enriched 2026-09-19)

| Surface | Artifact | How it was obtained |
|---|---|---|
| OpenAPI 3.1 (8 operations, SDK-verified) | `openapi/forcedream-ai-openapi.yml` | fetched verbatim from github.com/forcedreamai/forcedream-openapi; every route confirmed live |
| A2A agent card (protocolVersion 1.0, 18 skills, ES256-signed) | `a2a/forcedream-ai-agent-card.json` + `a2a/forcedream-ai-a2a.yml` | probed at `/.well-known/agent-card.json` on api.forcedream.ai and forcedream.ai; graded **conformant** |
| MCP server (21 tools, 5 prompts, 2 resources) | `mcp/forcedream-ai-mcp.yml`, `mcp/forcedream-ai-mcp-tools-list.json`, `mcp/forcedream-ai-tool-crosswalk.yml` | anonymous `initialize` / `tools/list` on the live endpoint; deployment `both` (remote + `npx -y @forcedream/mcp-server`) |
| OAuth discovery (RFC 8414, RFC 9728, RFC 7591), JWKS, security.txt | `well-known/` | probed on every host; index in `well-known/forcedream-ai-well-known.yml` |
| llms.txt (two variants) | `llms/` | fetched from forcedream.ai and www.forcedream.com |
| 12 SDKs, MCP package, CLI + Homebrew tap | `packages/`, `cli/` | registries queried unauthenticated; 7 SDKs on registries at 0.3.0, 5 source-only |
| Conventions, idempotency, reversibility, errors, rate limits, lifecycle, changelog, plans, sandbox | `conventions/`, `errors/`, `rate-limits/`, `lifecycle/`, `changelog/`, `plans/`, `sandbox/` | searched on the developer docs, terms and trust centre |
| Webhooks (7 events) | `asyncapi/forcedream-ai-webhooks-asyncapi.yml` | generated faithfully from the provider's webhooks page — ForceDream publishes no AsyncAPI |
| Conformance, regulatory posture, authentication, scopes, security | `conformance/`, `regulatory/`, `authentication/`, `scopes/`, `security/` | searched + probed |
| Agent skills (3) | `skills/` | generated, grounded in verified operationIds |

**Contract discovery note.** `https://forcedream.ai/openapi.json` (also served on api.forcedream.ai and forcedream.com) parses as OpenAPI 3.0.0 but is a different document — "ForceDream Data Oracle", 15 `/v1/oracle/*` routes, `servers[]` set to an ngrok placeholder — and those routes return 404 on the live API host. It is recorded in `well-known/forcedream-ai-well-known.yml` and deliberately not wired as a contract.
