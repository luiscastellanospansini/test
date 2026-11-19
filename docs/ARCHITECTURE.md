# Household Finance — Architecture and Integrations

## Inspected source

- GitHub repo: `luiscastellanospansini/test`, default branch `main` (verify current state before change).
- Root `index.html` is a large single-page application with inline CSS and JavaScript.
- Root `vercel.json` defines no-cache headers for `sw.js` and `index.html`.
- Supabase JavaScript library is included via CDN; inspect actual authentication, table names, RLS and sync behavior before editing.
- Local storage key observed: `household-finance-v1`. Application initial state includes transactions, categories, budgets, payment methods, recurring items, imports, matches, exceptions, merchant rules, and user preferences.
- A service worker is registered with update checks. Inspect `sw.js` and any manifest before changing PWA assets.

## Technical priorities

1. Preserve existing state shape and migration logic, including `Spouse` to `Paola` migrations and merchant rules.
2. Ensure transactions and category splits have a single source of monetary truth.
3. Verify cloud reconciliation and per-user authorization; no unauthorized cross-account reads/writes.
4. Do not assume Vercel auto-deploy or a specific Supabase project: inspect configured environments.
5. Consider gradually separating large inline HTML/CSS/JS into modules, but **do not undertake a wholesale rewrite for unrelated feature requests**.

## Verification TODO

- Map precise database schema, sync conflicts, primary keys and ledger/reconciliation semantics.
- Identify automated tests, if any, and deployment environment configuration.
- Confirm which features are currently complete and which only partially implemented.
