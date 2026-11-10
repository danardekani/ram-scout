---
name: ram-scout-prepare-resale
description: Prepare a computer-lot purchase brief, help me identify recovered RAM, or draft accurate resale listings. Does not buy, collect, physically remove/test memory or publish without approval.
adapted: false
---

You end up with a purchase brief, a reconciled list of recovered modules and resale drafts that describe the parts the member actually has.

## When to use this
“I'm considering this lot.” “I bought the computers.” “Help me list the RAM.” Read the chosen lot, the member's approved limit, country, selling account, testing ability, workspace and connected roles from setup and evaluation. Do not copy an example budget, city or hardware model into the member's operation.

## 1. Prepare the decision
Refresh current bid, minimum valid next bid, closing timezone, buyer premium, taxes, payment deadline, collection requirements, loading, qualifications and maximum bid. Confirm the full acquisition budget remains available after other commitments. Present the exact source URL, ceiling and unanswered questions. The member places bids, pays and collects. No bid or purchase is implied by “ready”.
WHY: a price calculation does not authorize spending or satisfy pickup conditions.

After the member confirms a completed purchase, attach actual invoice price, fees, tax and pickup cost to its source listing key. Replace the pending budget reservation with actual committed cost. Set bought only from confirmation or authoritative purchase evidence.

## 2. Guide physical preparation for the exact model
Identify each actual model and revision from the member's photos and labels. Open the manufacturer's service manual for that model. Explain the relevant preparation, power-down/unplug and static precautions, required removal steps and compatible testing equipment. The member handles modules by their edges, removes them and runs tests; you cannot perform physical work. If access is unclear or they lack confidence, pause that hardware step rather than inventing a safe procedure.
WHY: one generic disassembly sequence can be wrong for another chassis.

Ask for clear module label photos, counts and actual test results. Separate part number, capacity, DDR, speed, form factor, ECC/buffering and condition. Compare recovered count with expected count and explain differences. Keep failed, untested and working modules separate. Never call untested RAM tested. Do not promise compatibility solely from matching capacity.

## 3. Draft the resale
Refresh exact sold evidence through the connected selling-research tool; read the current seller plan and shipping assumptions. Draft listings with exact part and quantity, honest condition/test details, the member's own photos, supported compatibility, shipping and return terms. One module and a matched kit need different quantities and comparisons. If the tool cannot create a draft remotely, provide ready-to-paste content in the member's workspace and label it a local draft.
WHY: a fabricated test result or stock image can turn a profitable estimate into a return.

Show each draft, intended account, price, fees and inventory quantity. Require the member's approval for publishing. If approved and the connected tool supports it, publish only the reviewed listing and read it back; otherwise guide the member through the remaining action. Do not count a local draft as a live listing. Attach actual listing IDs to the module group; set listed only after it is live.

## 4. Verify the handoff
Reopen the purchase and module rows and every created draft. Confirm recovered counts reconcile with working, failed and untested units. Check title, part number, quantity, photos and price against evidence. Show what is ready to approve and what still requires the member's physical work. Hand off completed sales to `ram-scout-reconcile-sales`.
WHY: draft completion should be visible and recoverable after the chat ends.

## Failure modes
- Different hardware arrives → update actual parts, pause old valuation and reevaluate before listing.
- No model manual found → ask for the exact label; don't apply another machine's procedure.
- No tests supplied → mark untested honestly; don't reuse tested-condition comparisons.
- Publishing tool absent → save local drafts and identify the manual action without claiming success.
Call `report_skill_issue` immediately for broken or confusing steps, skill_slug `sam-altman-ram-scout/ram-scout-prepare-resale`, kind broken, missing or confusing; omit private photos, orders and credentials.

## Rerun
Use after each confirmed purchase, recovered batch or listing revision. Reuse purchase and module IDs so a repeated draft does not double inventory or budget.
