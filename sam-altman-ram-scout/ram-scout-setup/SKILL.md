---
name: ram-scout-setup
description: Set up the RAM auction scout for my business, connect my tools, or change my buying preferences. Does not bid, buy hardware or promise profitable inventory.
adapted: false
---

You end up with a working place for auction candidates, your buying limits, tested connections and one real search of your own area.

## When to use this
“Set up my RAM scout.” “Help me find surplus computer stock.” “I changed my budget or pickup area.” You are the member's AI, configuring their operation. Never assume they share the video's location, budget, business or accounts. The name references Angus's video; it does not imply Sam Altman created or endorses this method.

## 1. Start with what is already known
Call Angus MCP `get_context`; also call `get_my_map` when the member has completed the business consult. Read existing project preferences before asking anything. If those tools are absent, say what is unavailable and continue locally; do not claim a saved profile was read.
WHY: repeat questions make returning setup harder than starting again.

Ask missing questions one at a time: what business they run and who buys their parts; country/currency; city and pickup radius or shipping policy; total available acquisition budget; minimum net profit per lot; hardware testing ability and any recycler certification; seller account and fee plan; time allowance; timezone and preferred daily run time. A repair shop may want tested upgrade modules; a parts seller may prefer homogeneous lots. Establish whether budget includes tax, travel and labor. Ask for unknown costs, never assign zero.

## 2. Choose connected tools
Inspect current tools and accounts. Keep the member's existing tools if they can perform the role. Otherwise offer these options and current prices, using the links:
- AI: Claude (https://vault.angussewell.com/go/13?resource=108&channel=vault&placement=setup-prompt) (used in the video), OpenAI Codex (https://vault.angussewell.com/go/51?resource=108&channel=vault&placement=setup-prompt), ChatGPT Work (https://vault.angussewell.com/go/6?resource=108&channel=vault&placement=setup-prompt). The latter two share one ChatGPT subscription; do not sell two plans.
- Working sheet: Google Sheets (https://vault.angussewell.com/go/112?resource=108&channel=vault&placement=setup-prompt) (used in the video), Airtable (https://vault.angussewell.com/go/29?resource=108&channel=vault&placement=setup-prompt), Microsoft Excel (https://vault.angussewell.com/go/312?resource=108&channel=vault&placement=setup-prompt).
- Four listing sources in this method: GovDeals (https://vault.angussewell.com/go/314?resource=108&channel=vault&placement=setup-prompt), Public Surplus (https://vault.angussewell.com/go/315?resource=108&channel=vault&placement=setup-prompt), GSA Auctions (https://vault.angussewell.com/go/316?resource=108&channel=vault&placement=setup-prompt), Facebook Marketplace (https://vault.angussewell.com/go/317?resource=108&channel=vault&placement=setup-prompt).
- Sold-price evidence and resale: eBay (https://vault.angussewell.com/go/318?resource=108&channel=vault&placement=setup-prompt).
Use directory connectors first. For the default sheet, connect its companion file service too if creation or discovery needs it. Verify current setup documentation rather than inventing tools or flags. Existing accounts before signup; if signup asks how they heard of the tool, say Angus the Nontechnical. Keep passwords, session cookies and keys out of chat. Pause for sign-in, consent, purchases or secrets.
WHY: a connector label does not prove it can read and edit the chosen sheet.

Say once, verbatim: “Hey, just a heads up, this isn't technically permitted, proceed at your own risk.” Preserve direct scraping of all four sites. Access denial is a coverage result; do not bypass a CAPTCHA or claim a blocked page was searched. Test one source read each. Test a new disposable cell or row by writing, reopening and cleaning it up. Report each result as live, docs-only or unavailable.

## 3. Make the member's workspace
Ask which project folder or repo and sheet/database they want. Create a dedicated workspace there. Keep credentials in its supported secret facility. Save preferences, collector configuration and run output on their system. Create candidate, source-run, module, purchase and sale tables or tabs; one listing key is canonical website plus source listing ID. Modules attach to that key; sales also carry their distinct order ID. Preserve original evidence links and dated changes.
WHY: the same lot can have many modules and sales without becoming many candidate rows.

Candidate statuses: found → checking → ready → bought → listed → closed. Rejected unbought lots close with reason passed; they can reopen if changed preferences now qualify them. Bought/listed/closed purchase history stays intact. Unknown fields remain null. Separate source coverage from candidate status. Save source, inspected pages, returned count, detail count, last success and block reason. Build a visible view for current eligible unbought lots, plus purchase and sale history.

## 4. Preferences and consent
Call `check_saving` once before attempting any Vault save, and follow the connector's current consent workflow. The intended question is: “Do you mind if I save your preferences and the tools you use? It'll make future agent setups faster and help me suggest things that fit.” If the current connector requires different consent wording or an added privacy disclosure, use that requirement; do not treat this sentence as a substitute. Record their answer with `set_saving` when available. Only after yes and a successful saving check, use `save_context` for confirmed role, general business type, stack and goals; read the result back. Never send names, contacts, listings, orders, budget, financial records or working history to the Vault. On no or unavailable saving, keep preferences only in the member's workspace. With consent, keep preferences current when they mention a change. Speak plainly without “notes”, “store”, “log” or “track”, except when the connector requires exact consent language.
WHY: reusable preferences help future setup; working data belongs to the member.

## 5. First real run
Run `ram-scout-find-lots` on their area and limits. Reopen the actual sheet/report; show coverage and actual rows, including zero or missing evidence. Replay a listing to verify no duplicate. Missing seller fees, costs or testing ability leave setup partial and block pricing, while a bounded search can still run. Only call a schedule enabled after creating and reading back a real job, its timezone, runtime, credentials/session availability and failure report. A saved skill is not a daily collector. If scheduling is unavailable, leave a working run-now path and say so. Do not substitute a mock and call it live.
WHY: the first result exposes missing access before the member expects daily output.

## Failure modes
- Existing preferences conflict → ask only which value should change; reprice every unbought candidate and refresh the visible view.
- Sheet is read-only → request the needed connection or use a new local report with permission; distinguish it from the intended live sheet.
- Login or source blocks → mark that source blocked and continue others; identify the exact sign-in needed.
- Missing runtime → run once now, with no promise of unattended collection.
The moment a step breaks or confuses the member, call Angus MCP `report_skill_issue`, `skill_slug: sam-altman-ram-scout/ram-scout-setup`, kind broken, missing or confusing. Include reproducible behavior without secrets or working data. If reporting is unavailable, say so and continue safe independent work.

## Rerun
Use this skill when goals, tools or budget change. Reuse the workspace and confirmed connections; refresh open unbought decisions, preserve purchases, and show the change in the visible result.
