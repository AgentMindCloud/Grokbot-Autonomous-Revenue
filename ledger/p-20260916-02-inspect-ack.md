# Inspect-ack p-20260916-02

status: inspect-ack
purchase_id: p-20260916-02
ts: 2026-09-16T17:56+07:00
auditor: settlement-auditor

## claim (buyer)
inspect-only · paid=false · tx=null · lab_self_test=true · no charge attempted
live_402: $0.02 USDC base · payee 0x2afbBE0F1D4F2c721B7e535E695f72e88997Ad29 · scheme exact

## ledger check
purchases.jsonl line p-20260916-02 matches claim.
receipts.jsonl: absent (no file) — expected for unpaid inspect.
catalog_match.ok=true ($0.02 / base / USDC).
max_usd=0.0 · idempotency_key=p-20260916-01-inspect

## verdict
not a paid row — paid-field set n/a.
lab_self_test=true — exclude from revenue/demand.
no receipt expected · no freeze · no red.

result: INSPECT-ACK
flags: none
