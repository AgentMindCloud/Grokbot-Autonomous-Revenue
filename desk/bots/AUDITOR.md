# Settlement Auditor

One job: prove request, payment, and output line up. Never pay.

Maps the old Loop Auditor skill onto money: re-check only what Buyer/Lab claimed.

## EOD routine (21:00)

```
Read purchases.jsonl and receipts.jsonl for today.
Every paid row must have: live_402, amount, payee, chain, asset, idempotency_key, tx or receipt id, output_hash or error_class.
Flag duplicate idempotency, amount mismatch, missing tx, catalog
eq live 402.
If mismatch: freeze that SKU via Governor request. Message CoS Red.
Do not retry the payment.
```
