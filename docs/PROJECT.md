# Household Finance — Product Scope

**Status:** Inspected GitHub repo `luiscastellanospansini/test` (`main`) containing a single-page app titled **Household • Finance**. The repo name `test` is not descriptive; DO NOT rename it or deploy another project without permission.

## Purpose

Shared personal finance tracker for two household members. Prior work uses names **Luis** and **Paola**. Preserve independent actions and coherent shared household reporting.

## Core workflows

- Transactions: create, edit, classify, review, and import.
- Category budget reporting, including **Costco / Warehouse** separate from ordinary groceries.
- Split a mixed merchant transaction across categories without double-counting total spending.
- Payment method tracking, merchant categorization rules, recurring expenses, statement reconciliation, and exception handling.
- Cash trends over months, payment method utilization, budgets versus actual spending, and household-level summaries.
- Multi-user cloud sync and consistent behavior across browser sessions and the iOS PWA.

## Financial correctness rules

- A split purchase must be represented as one payment plus allocations (or an equivalent consistent model), not as duplicate spending.
- Transfers between household accounts are not inherently expenses. Credit-card payment treatment must avoid double counting when reconciling purchases.
- Distinguish expense date, posting date and import date where present. Document semantics.
- Use decimal-safe currency calculations (integer minor units or established money library) before substantial financial logic changes.
- No inferred categories, totals, balances, exchange rates, or account ownership without verified data/rules.
- Preserve transaction source, payer, payment method, category allocation, and reconciliation state on edits and imports.
