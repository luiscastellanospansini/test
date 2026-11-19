# Household Finance — Testing and Release Gates

## Data correctness tests

1. A single-category expense updates the correct month, budget and payment-method usage.
2. A multi-category purchase allocates exactly the original total, including rounding cents.
3. Updating/deleting a split transaction reverses prior allocations and avoids duplicated totals.
4. Costco merchant rule acts on applicable transactions but permits manual category splits.
5. Credit-card payments and internal transfers do not inflate expense totals.
6. Refunds, reimbursements, negative amounts and duplicate bank imports are handled consistently.
7. Recurring transactions, statement imports, reconciliation matches, and exceptions preserve state on reload.
8. Payer filters and household totals correctly handle Luis and Paola.
9. Monthly cash trend and payment utilization graphs match underlying ledger data.
10. Cloud synchronization preserves user authorization, offline edits, and conflict behavior.

## Visual and release checks

- Validate transaction form on iPhone and desktop and PWA updates in installed mode.
- Test loading and error states, broken email verification/sign-in links if relevant, and private-window behavior.
- Run existing tests; document missing ones rather than claiming they passed.
- Verify deployed URL serves latest code and browser interaction actually works.
- Test all financial changes against synthetic fixtures, never production financial data.
