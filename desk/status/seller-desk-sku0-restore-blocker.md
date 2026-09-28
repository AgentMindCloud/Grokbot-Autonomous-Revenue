# Seller Desk — SKU-0 restore WAITING (vercel grant)

- date: 2026-09-28 20:52 Asia/Ho_Chi_Minh
- cos: NAMED YES 2026-09-28 — human grants Seller Desk Vercel project access for aggregator-beta.vercel.app
- prior: HOLD (skipped grant) superseded by named yes above
- goal: sample→200 + paid→402; never pay; never list
- last repro (pre-grant): /health 200 mock=false v0.2.0; /api/search + web_search_sample + /api/sample → 500
- box: no VERCEL_* env; no vercel CLI; AgentMindCloud/agent-search-pro still 404
- state: WAITING — no further probe until Vercel token/invite lands
- access needed (exact):
  1. Vercel token with Project access to the deployment behind https://aggregator-beta.vercel.app → save as box secret `VERCEL_TOKEN` (Seller Desk only)
  2. Project id/name (or confirm team slug) so `vercel link` / API can target the right project
  3. Prefer also: GitHub (or other) source URL linked to that Vercel project for code patch; if env-only, Deployment → Environment Variables for the search provider key(s)
- clear HUMAN must only after restored + Lab CLEAR