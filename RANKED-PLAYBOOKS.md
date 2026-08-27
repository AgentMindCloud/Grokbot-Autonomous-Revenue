# Ranked Playbooks — Grokbot Autonomous Revenue

*Updated 2026-08-27 by Master-Synthesis-Daily*

EMR sibling repos (`EMR-repo`, `grokbot-monetization-research`) are still stubs. Seeded from: `grok-bots-monetization` ACTION-PLAN (Whop), live market (x402/Whop/botdirectory/Grok Bot Social), and public Grok Bot money playbooks (Whop rev-share, X research products, skill packs).

Composite = 0.30*speed + 0.25*feasibility + 0.25*autonomy + 0.20*revenue. Speed: 10 if TTFD ≤24h, 8 if ≤48h, 6 if ≤7d, 3 if weeks.

---

## Top 5 (2026-08-27)

### 1. Whop One-Shot X Alpha Brief ($19–49)
- **Exact steps**: Bot pulls live X + web on a buyer-chosen topic → writes 8–12 page brief → posts teaser on X/Grok Bot Social → Whop checkout → webhook → deliver PDF/MD + license.
- **Tools**: Whop (existing), X search, GitHub, Grok Bot Social marketplace, optional Composio Stripe/Gmail.
- **Money**: One-time Whop checkout → payout to connected account.
- **TTFD**: 24–48h after first product + 1 teaser post.
- **Feasibility 9 / Autonomy 8 / Revenue 6 / Composite 8.15**
- **Next experiment**: Create 1 Whop product + 1 public teaser today.

### 2. Paid Skill Pack + License Key (botdirectory / Grok Bot Social)
- **Exact steps**: Package 1 proven workflow as markdown skill → list free teaser on botdirectory.ai + paid full pack on Grok Bot Social / Whop → license key gates the full file.
- **Tools**: botdirectory.ai PR, Grok Bot Social marketplace (already has Revenue + x402 packs), Whop license keys, GitHub.
- **Money**: $9–29 pack sales via Whop or x402 tip rail.
- **TTFD**: 24–72h.
- **Feasibility 9 / Autonomy 8 / Revenue 5 / Composite 7.95**

### 3. x402 Gated Research Drop
- **Exact steps**: Publish free 20% teaser gist → 402-protect full markdown/API → agent or human pays USDC on Base → auto-unlock.
- **Tools**: x402 (Coinbase/LF), USDC wallet (separate, dual-approval), GitHub Pages or Cloudflare, Grok Bot Social x402 patterns pack.
- **Money**: Per-request USDC to bot wallet.
- **TTFD**: 48–96h (rail setup is the drag).
- **Feasibility 7 / Autonomy 9 / Revenue 7 / Composite 7.70**

### 4. One-Creator Whop Rev-Share Operator
- **Exact steps**: Pick 1 mid-level X creator → bot runs content + Whop product ops → 20–30% rev-share contract (human signs).
- **Tools**: Whop CLI/API, X, Discord optional, Composio.
- **Money**: Rev-share of creator offer; first $ possible when they have existing audience.
- **TTFD**: 3–7d (sales cycle).
- **Feasibility 7 / Autonomy 6 / Revenue 8 / Composite 6.55**

### 5. Prompt Arsenal Pack $9–19 (Whop)
- **Exact steps**: Curate 20 Grok Bot prompts from existing fleet work → one-time Whop product → X thread + botdirectory listing.
- **Tools**: Whop, X, GitHub, botdirectory.
- **Money**: Impulse digital good.
- **TTFD**: 24h if product already sketched.
- **Feasibility 10 / Autonomy 7 / Revenue 4 / Composite 7.55** (kept #5: lower ceiling than 1–3).

## Kill / defer
- Niche directory business: weeks to traffic before $1.
- botdirectory sponsored slot: 14/15 taken, not a product.
- Full 50-bot fleet before first dollar: path-dependent cost trap.

## 48h experiment (only one)
**Ship Whop product #1: "X Alpha Brief — Grok Bot Niche Scan" at $19.**
1. Create product + checkout URL in Whop dashboard (30 min).
2. Bot generates one real sample brief from last 14d X (2h).
3. Post teaser thread + Grok Bot Social listing with checkout (1h).
4. Manual fulfill first 3 sales; wire webhook after sale #1.
Kill if 0 checkouts after 20 qualified views.

## Common tools
Whop, X APIs/search, GitHub, Grok Bot Social marketplace, botdirectory.ai, Composio (Stripe/Gmail later), separate USDC wallet + dual-approval for x402.

## Gaps for tomorrow
- EMR daily bots never wrote outputs — need Market-Validation and Pricing-Simulations to actually run.
- Confirm Whop company_id + live API key.
- Confirm x402 wallet exists and is not on shared computer.
- Price test $19 vs $29 on the brief.
- Count Grok Bot Social pack installs vs conversions (currently 3–4 installs, $0 tracked).
