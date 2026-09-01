# Tool Feedback Loop — 2026-09-01

Live paid skills: TA Confluence Signal only (pre-revenue).
Health: 3.2/10 (was 3.0 on 08-29). Still 0 calls / 0 USDC. Score does not rise until a callable endpoint exists.

## Proxy metrics
| metric | value |
|--------|-------|
| teaser_calls | 0 |
| paid_calls | 0 |
| USDC | 0 |
| p95_ms | n/a |
| error_rate | n/a |
| repeat_agent_id | n/a |
| social pack installs | ~3–4 / $0 |
| repo issues/PRs | 0 |

## YAML delta to ship
```yaml
name: ta-confluence-btc-3h
tools:
  - name: ta_confluence_teaser
    payment: free
    timeout_ms: 800
    output: [bias, key_levels, confluence_bucket]
  - name: ta_confluence_full
    payment: x402
    asset: USDC
    chain: base
    price: "2.00"
    timeout_ms: 2500
    output: [score_table, ci, invalidation, scenarios]
log: analytics/mcp-calls.jsonl
```

Kill new skills until paid_calls >= 1.
