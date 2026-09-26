# TA Confluence Scoring Formula (Hard Reasoning Core)

Inputs: Multi-asset OHLCV + funding + OI + orderbook depth + multi-TF structure + sentiment.

Process:
1. Parallel factor scoring (each factor 0-100 with confidence)
2. Weighted confluence = sum (weight_i * score_i)
3. Conflict detection: flag any contradictory high-confidence signals
4. Scenario branching: bull / base / bear with probabilities
5. Formal consistency check (no unaddressed contradictions)
6. Sensitivity analysis + historical robustness snippet

Output:
- Public teaser: bias + key levels
- Full x402: table, score 0-100, CI, alternatives, invalidation, trade ideas

Formal properties enforced: consistency, no-unaddressed-contradiction, sensitivity.
