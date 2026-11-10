---
name: ram-scout-evaluate-lots
description: Check what the RAM is worth, work out my maximum bid, or compare computer lots within my budget. Does not infer installed parts, invent sold comps or guarantee profit.
adapted: false
---

You end up with up to five supported buying options, each with an exact RAM breakdown, net-profit estimate and valid maximum bid; zero is an acceptable result.

## When to use this
“Which lots are worth a closer look?” “What can I bid?” “Does this still work with my new profit target?” Read the member's area, currency, budget, cost assumptions, seller plan, minimum net profit and workspace from setup. Read new/changed candidates and existing purchase commitments. Use the evidence collector, selling research surface and sheet connected in setup.

## 1. Verify the recoverable RAM
Read description, photos and model-specific service/specification evidence. Separate model, PC quantity, installed module part, capacity per module, module count, DDR generation, speed, UDIMM/SODIMM format, ECC, registered/unbuffered and condition. A supported maximum is not installed RAM. Mixed or unclear lots stay unpriced. Exclude soldered memory and lots whose terms remove or do not guarantee internal parts.
WHY: two 8GB modules cannot borrow the price of one 16GB module.

## 2. Find exact sold comparisons
Read actual completed sales through the connected sold-price surface. Match the exact module and condition; part number is strongest when available. Keep sale date, item amount, shipping, currency and source URL. Asking prices, unsold completed listings and hidden accepted offers are not verified sales amounts. Use the actual accepted amount only when the research tool exposes it. Deduplicate the same sale by source sale ID.
WHY: a visible crossed-out price or a current listing can overstate what buyers paid.

Calculate median sold item price, sample size and date range for each exact type. Flag a thin sample; never invent a median if access or exact matches are missing. Multiply only confirmed installed quantities. Keep shipping separate. Recheck fresh evidence before purchase; don't describe an old snapshot as today's bid.

## 3. Build the costs from the member's facts
Acquisition cost = bid + buyer premium + applicable purchase tax + pickup/shipping + agreed labor/testing. Read premium and tax basis for that exact sale. Expected net proceeds = RAM item revenue + shipping collected − marketplace fees − postage − packaging − agreed defect/return allowance. Use the member's actual fee plan, country, category and order size. Tax collected for remittance is not revenue but can be in the fee base. Charge per-order fees per expected order. Give leftover PCs no speculative value.
WHY: the video’s gross screen alone does not establish profit.

If currency differs, obtain a current conversion rate and identify its date/costs. Ask for unknown member-specific costs, never quietly set them to zero. Keep assumptions visible and separate from observed facts.

## 4. Solve the ceiling and allocate budget
Require gross RAM item value strictly greater than twice acquisition cost AND estimated net profit at least the member's target. Solve the highest bid satisfying both and available acquisition budget. Anchor allowed bids to the minimum next bid plus whole increments, checking tiered increments. Example only: minimum125.01, increment2.50, cap130 gives127.51. Equality at the two-times boundary fails. If the next allowed bid exceeds the ceiling, pass.
WHY: a mathematically affordable number may not be a bid the auction accepts.

Present the best five as alternatives unless the member chooses a combined allocation. Reserve all-in acquisition costs across pending/won lots before proposing additional purchases; replace a reservation with actual cost when won, not both. Unknown fees, parts or terms mean needs information. Retain why every passed lot failed. Reapplying a changed profit goal must update the visible shortlist and allow previously passed unbought rows to requalify; keep purchase history unchanged.

## 5. Check and deliver
For each candidate show link, deadline, evidence timestamp, gross item value, all acquisition costs, net proceeds, net profit, valid max bid, sample count and gaps. Hand-calculate one supported row and its next higher bid; verify that the ceiling passes and the next bid fails. Reopen the visible sheet. Only fully supported eligible lots become ready. A missing sold source means no priced recommendation, not an invented bargain.

## Failure modes
- One fee rate applied to every plan → read the actual seller schedule and recalculate per order.
- Gross margin called profit → rebuild the selling-cost side.
- Five cheap lots exceed combined cash → reserve total acquisition costs, not bids alone.
- Missing RAM or hidden best offer → leave value unknown until evidence is supplied.
Call `report_skill_issue` with skill_slug `sam-altman-ram-scout/ram-scout-evaluate-lots` and kind broken, missing or confusing as soon as a step fails; share no private records.

## Rerun
Run after each fresh scan, a bid/fee/price change, or changed preferences. Refresh again immediately before the member makes a purchase. Leave bidding and payment to them.
