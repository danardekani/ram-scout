---
name: ram-scout-find-lots
description: Find office computer lots near me, refresh today's RAM candidates, or set up my daily auction search. Does not value unknown RAM, place bids or turn partial coverage into a complete market scan.
adapted: false
---

You end up with a fresh, deduplicated list of relevant computer lots and a visible explanation of which sources were actually checked.

## When to use this
“Find computer lots near me.” “Refresh today's auction candidates.” “Change the search to my new pickup area.” Reads the member's business, customers, geography, total acquisition budget, qualifications, testing ability, timezone, schedule, workspace and connected roles from setup. If missing, run setup or ask only for the missing input.

## 1. Open the member's current work
Read preferences and existing candidate rows. Reapply changed preferences to all unbought lots, including previously passed lots; keep purchase/sale history. Refresh travel cost and eligibility when the area changes. Check available budget after pending and won lots. Use the AI/browser collector and sheet connected in setup.
WHY: a preference change must alter what the member sees, not only a configuration file.

## 2. Read the four listing sources directly
Use each source selected in setup, preserving the four-site method. Search office desktops, workstation bundles and relevant surplus lots within the member's area. Read listing detail, photos and sale terms, not just search snippets. Follow pagination until the requested bounded scan ends. Save pages inspected, detail count, returned count, next-page status and last successful read separately per source. A partial scan stays partial.
WHY: a category page can contain cable lots or show only the first page of a large result set.

Recognize login pages, CAPTCHAs, 401/403/429 responses, empty app shells and rate limits. These are blocked or partial coverage, never zero matches. Keep other sources running. Respect retry intervals and use a bounded retry; do not bypass authentication or technical blocks. If the member must sign in, identify that source. Preserve direct scraping; do not silently replace it with email alerts or another workflow.

## 3. Extract only supported facts
For each relevant lot, retain source/listing ID, canonical URL, title, location, PC count, models, described installed RAM, photos, current bid, minimum next bid, increment or increment tiers, close time with timezone, price basis, buyer premium, tax terms, collection window, eligibility and checked timestamp. Read the labelled current bid region, not the first currency string: a hidden purchase modal may contain zero while the real bid is positive. Distinguish per-computer from whole-lot pricing. Leave ambiguous fields unknown.
WHY: plausible-looking prices or advertised maximum RAM can make a bad lot look profitable.

Exclude unrelated equipment, ineligible recycler-only lots and qualifications the member lacks. Do not invent certification. RAM excluded or components not guaranteed becomes a passed reason. Unconfirmed removable RAM can remain checking; soldered memory is unsuitable for this removal loop. Do not count a model's maximum supported capacity as installed RAM.

## 4. Update and reopen the visible result
Upsert one row per canonical website plus listing ID. Different sources remain separate unless reliable evidence proves a cross-posted lot; attach that evidence instead of guessing. Found → checking → ready → bought → listed → closed; rejected lots close as passed. Only the pricing job can make a lot ready. No results is valid.
WHY: repeated scans should refresh evidence, not inflate the opportunity count.

Read the sheet back, show source coverage and row counts, and inspect one real row against its source. Replay unchanged data to prove no duplicates. If no live row is available, use a labelled temporary fixture for the duplicate check and keep it out of buying views. Hand off supported candidates to `ram-scout-evaluate-lots`.

## 5. Run again on a real schedule
If requested in setup, create a daily job using the selected runtime, timezone, persisted workspace and available credentials. Specify what runs, where, last/next execution and where failures appear. Read back the created enabled job before promising a next run; run once and reopen its output. A local runtime may need the app/computer awake. If unavailable, deliver the run-now procedure and mark scheduling untested.
WHY: a skill file alone cannot wake up and scrape tomorrow.

## Failure modes
- $0 modal mistaken for price → reread labelled bid/minimum; make unknown if ambiguous.
- More rows after unchanged replay → repair canonical keys before further imports.
- “No deals” with blocked sources → separate coverage from zero qualifying rows.
- Changed radius leaves stale candidates → refresh every unbought view and pickup assumption.
- Schema changed → retain raw evidence locally, pause that parser and report the failure.
Call `report_skill_issue` immediately for breakage/confusion, skill_slug `sam-altman-ram-scout/ram-scout-find-lots`, kind broken, missing or confusing; omit private records and credentials.

## Rerun
Run daily or on request. Reuse source keys and preserve history. A broken source must not stop successful sources or turn stale rows into current recommendations.
