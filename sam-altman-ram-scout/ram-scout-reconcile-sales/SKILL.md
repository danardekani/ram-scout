---
name: ram-scout-reconcile-sales
description: Calculate my actual RAM resale profit, reconcile orders and refunds, or close a finished lot. Does not treat estimates, unsold inventory or tax collected for remittance as realized income.
adapted: false
---

You end up with actual cash profit to date, remaining inventory and a final realized result only when the lot is fully reconciled.

## When to use this
“How much did I actually make?” “Some modules sold and one was returned.” “Close this lot.” Read the member's workspace, currency, chosen selling and sheet tools, actual acquisition costs, module groups, published listing IDs and prior orders from setup and the resale job. Never make a settlement record from a forecast.

## 1. Read the actual sale evidence
Read completed orders, payment settlements, platform fees, postage, packaging, refunds and return shipping from the member's connected tools or supplied records. Retain source order/transaction IDs and dates. Separate refunded, cancelled, pending and completed orders. Keep sales tax collected for remittance out of income; distinguish tax from fees charged on that tax where applicable.
WHY: a displayed sale amount is not necessarily money retained after fees and returns.

Upsert by platform plus order/transaction ID. Attach each order to its source lot and module group. If an order combines lots, allocate actual shipping/fees consistently and disclose the basis; ask about ambiguity. Replaying the same records must not double revenue, costs or inventory movement. Leave missing values unknown and identify the missing statement, never silently set them to zero.

## 2. Reconcile inventory before closing
Start with actual recovered modules, split into working, untested and failed. Deduct shipped units, add returned units with their current condition, and show unsold quantity. A failed returned stick must not silently become sellable stock. Reconcile total recovered to buyer-kept, available, failed/scrapped and other explicitly identified dispositions. Preserve past purchases and correction history.
WHY: cash received from most units does not mean the entire lot has finished.

A partially sold lot stays listed. An open return or unresolved refund prevents final closure even if sellable quantity reaches zero. Ask the member to confirm any disposal or final disposition; do not invent sales for leftovers. Give residual computers no realized proceeds unless an actual completed sale is evidenced.

## 3. Calculate actual cash separately from estimates
Cash profit to date = completed item revenue + shipping collected − actual selling fees − postage − packaging − refunds − return postage − actual acquisition cost and agreed actual labor/testing costs. Use actual expenses exactly once. Replace the forecast defect/return allowance with actual outcomes; do not deduct both. Show forecast profit separately, alongside the reasons actual results differ.
WHY: the original estimate was a decision aid, not an accounting result.

Make partial and final results explicit. Example only: an unsold module means “cash profit to date” while the lot stays listed; only the final sale and resolved refunds can produce final realized profit. Never imply the hypothetical example amounts are this member's sales.

## 4. Verify and return the result
Hand-sum one complete lot from individual order records. Reconcile order counts, module counts and fees against source statements. Replay unchanged records, reopen the visible sheet and prove totals are unchanged. Show evidence gaps, units remaining and open refunds. When all inventory has an explained final disposition and all costs/refunds are resolved, set closed and show the final amount with its date.
WHY: the member should be able to reproduce the answer from their own records.

## Failure modes
- Estimated reserve plus actual refund deducted → remove the estimate from the actual ledger.
- Duplicate sale or returned stock counted twice → repair source order IDs and movements, then recalculate.
- Refund still pending → keep listed and label result provisional.
- Missing expenses → say incomplete, show the known subtotal and ask for the missing evidence.
Call `report_skill_issue` at the first broken/confusing step, skill_slug `sam-altman-ram-scout/ram-scout-reconcile-sales`, kind broken, missing or confusing; never include buyer details or financial records in the report.

## Rerun
Run after settlements or returns arrive, or on the cadence agreed in setup. Preserve the original estimate and all actual corrections in the member's system. Do not send working histories to the Vault.
