# Template Status & Verification

**Classification:** Configurable n8n template asset — not a verified production deployment.

The workflow export and documentation are inspectable template evidence. They do not prove a configured production lead pipeline, deduplication guarantee, SLA, ROI, or client outcome.

## Verification gate
1. Parse/import into a clean current n8n instance.
2. Inspect source branches, identity normalization, deduplication, routing, expressions, and Code nodes.
3. Replace placeholder credentials, source URLs, CRM/base/table IDs, channels, webhooks, models, and resource references.
4. Run same-lead-across-sources, unique-lead, missing-identity, malformed-input, and provider-failure cases.
5. Verify no unintended duplicate lead records or mismatched source attribution and record configured test date/result.

## Security
Never commit API keys, CRM credentials, private webhooks, lead PII, or production data. Use synthetic leads and fresh test credentials.

## Change record
- **2026-09-03:** Added repository verification/security/status control. No workflow-logic change or runtime pass is implied.
