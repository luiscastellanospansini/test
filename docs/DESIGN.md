# Household Finance — Design Standards

## Existing UI

Existing inspected page uses a light background, navy sidebar, white content panels, and teal/blue accents. Preserve current application language and visual structure unless a redesign is requested. Inspect current code rather than relying only on this description.

## Usability priorities

- On mobile, reduce friction for adding and splitting transactions.
- Maintain a visible and understandable mapping of payer, merchant, category, payment method, and amounts.
- Display money with currency, correct signs, and consistent decimals. Never bury adjustments or transfers inside generic expense totals.
- Make filters and chart periods explicit. Include sensible empty states and legends.
- For Costco/warehouse purchases, support splitting categories without losing merchant identity.
- Visually distinguish category budgets, month-to-date totals, available funds, reconciliation exceptions, and payment methods.

## UI QA

Check small phone, tablet, desktop; keyboard-visible transaction forms; long merchant names; multi-line split editing; chart axes; category color accessibility; and PWA safe areas. Verify that user changes are saved and synced and do not appear to revert after a refresh.
