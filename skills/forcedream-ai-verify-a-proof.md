---
generated: '2026-09-19'
method: generated
name: Verify a ForceDream proof without an account
description: Given a task_id, fetch the public proof and the Ed25519 signing key and verify the signature in your own process.
api: openapi/forcedream-ai-openapi.yml
operations: [getProof, getProofPublicKey]
source: >-
  operationIds verified in openapi/forcedream-ai-openapi.yml; canonicalisation rules from the spec's
  x-forcedream-canonicalization extension and forcedream-docs troubleshooting.
---

# Verify a ForceDream proof without an account

Both routes are anonymous. Nothing here spends money.

## Steps
1. **Fetch the proof** — `getProof` (`GET /v1/workforce/proof/{task_id}/public`). The body carries `proof_id`, `task_id`, `input_hash`, `output_hash`, `cost_pence`, `algorithm` (`Ed25519` or `Ed25519-batched`), `key_id` and `signature` (base64).
2. **Fetch the key** — `getProofPublicKey` (`GET /v1/workforce/proof/public-key`) returns `{algorithm: "Ed25519", public_key_pem, key_id}`. Confirm `key_id` matches the proof's. The same key is also published as the EdDSA entry in `https://api.forcedream.ai/.well-known/jwks.json`.
3. **Canonicalise** — build the signable object from the proof fields named in `x-forcedream-canonicalization` (task_id, agent_id, input_hash, output_hash, cost_pence, budget_pence, started_at, completed_at, plus external_cost_hash and retrieved_count when present), sort keys alphabetically, serialise exactly as the extension specifies.
4. **Verify** — for `Ed25519`, verify the signature over the canonical bytes; for `Ed25519-batched`, rebuild the Merkle root from `inclusion_proof.siblings` and verify the root signature. A verifier that only implements the simple case will wrongly reject valid batched proofs.

## Errors
- A 404 within ~50 s of task completion is a propagation delay, not a missing proof — retry.
- `/v1/audit/merkle/verify` is a different, paid platform-audit tool; do not use it for task proofs.

## Alternatives
- MCP tool `forcedream_verify_proof` (anonymous) and the `fd-verify` CLI in `@forcedream/mcp-server` implement exactly this flow; the browser page `https://www.forcedream.com/proof` does it client-side.
