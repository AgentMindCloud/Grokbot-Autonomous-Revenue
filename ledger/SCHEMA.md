# Ledger schema

Append-only JSONL. One object per line. Never edit a past line.
Files:

- `ledger/research.jsonl`
- `ledger/purchases.jsonl`
- `ledger/receipts.jsonl`
- `ledger/tests.jsonl`
- `ledger/decisions.jsonl`
- `analytics/mcp-calls.jsonl` (SKU-0 plus any MCP pay)

## research

```json
{"id":"r-YYYYMMDD-##","ts":"ISO","bot":"scout","status":"live|spec|thin|hype","endpoint":"","protocol":"x402|mpp|a2a|mcp","price_catalog":null,"operator":"","evidence_url":"","note":""}
```

## purchases

```json
{"id":"p-YYYYMMDD-##","ts":"ISO","bot":"buyer","experiment_id":"","endpoint":"","method":"","sku":"","max_usd":0.25,"live_402":{},"payee":"","chain":"base","asset":"USDC","approval_id":"standing|human-...","idempotency_key":"","lab_self_test":false}
```

## receipts

```json
{"id":"rc-YYYYMMDD-##","ts":"ISO","purchase_id":"p-...","tx":"","facilitator":"","settled_usd":0.02,"latency_ms":0,"http_status":200,"output_hash":"","error_class":null,"ok":true}
```

## tests

```json
{"id":"t-YYYYMMDD-##","ts":"ISO","bot":"lab","purchase_id":"p-...","scorer":"v1","quality":0.0,"schema_ok":true,"repeatable":true,"kill_or_scale":"hold","lab_self_test":false}
```

## decisions

```json
{"id":"d-YYYYMMDD-##","ts":"ISO","bot":"cos","subject":"sku0|counterparty|bot","action":"kill|hold|reprice|scale|accept-skill","human":true,"reason":""}
```

## mcp-calls

```json
{"ts":"ISO","tool":"web_search|web_synthesis","paid":true,"usd":0.02,"ms":0,"agent_id":"lab|external-unknown","lab_self_test":true,"http_status":402,"tx":null}
```

Self-tests must set `lab_self_test: true`. CoS and dashboards MUST exclude those from demand and revenue.
