---
generated: '2026-09-19'
method: generated
name: Obtain credentials and check balance without a human
description: Self-issue a ForceDream billing key and account key from an email address, receive the trial credit, and read the balance.
api: openapi/forcedream-ai-openapi.yml
operations: [signup, getBalance]
source: >-
  operationIds verified in openapi/forcedream-ai-openapi.yml; credential semantics from the agent card's
  self-service-credentials/v1 extension and the quickstart.
---

# Obtain credentials and check balance without a human

## Steps
1. **Sign up** — `signup` (`POST /api/signup`, no auth) with `{"email": "...", "source": "optional-attribution"}`. Returns `live_key` (prefix `fd_live_`, spends balance), `api_key` (prefix `sk_fd_`, account management — not interchangeable) and `user_id` (`usr_...`). The email is not verified before the credential is issued; no card and no human step.
2. **Note the grant** — the agent card states a credit grant of 1,000 pence GBP with no expiry, and a signup rate limit of 5 per IP per 3,600 seconds.
3. **Check balance** — `getBalance` (`GET /v1/account/balance`) with `Authorization: Bearer <key>`; the quickstart example returns `{"balance_gbp": "£0.08", "withdrawal_eligible": false}`.

## Rules
- Keys are shown once; there is no recovery except `POST /api/recover-key` and rotation via `POST /v1/account/keys/revoke` (prose reference only). Treat `fd_live_` as a secret.
- Top-ups are Stripe Checkout (`POST /api/checkout`, `amount_gbp` 5–10,000) and are non-refundable except where required by law (Terms 8.5); disputes within 14 days to billing@forcedream.com.
- Erasure is `DELETE /api/user/data` (immediate anonymisation).

## Errors
- `400` on a missing/invalid email; `429` when the per-IP signup limit is hit — wait for the window (`errors/forcedream-ai-problem-types.yml`).
