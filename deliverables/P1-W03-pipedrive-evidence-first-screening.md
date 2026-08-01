# P1-W03 - Pipedrive Evidence-First Screening

**Status:** Lite-only no-billing trial boundary verified under D-098; configuration and testing unapproved

**Phase:** Phase 1 - CRM candidate comparison

**Updated:** August 1, 2026

**Last signed-off checkpoint:** CP-004

## Approved work-unit outcome

Evaluate Pipedrive as the next independent-work CRM candidate through an evidence-first, evaluator-only process, targeting Lite as the lowest plausible production tier and using a no-billing trial only after a complete execution contract and separate account-creation gate are explicitly approved.

The work unit should determine whether Pipedrive can represent the approved CP-003 customer, opportunity, activity, source, next-action, and Centah-bridge model without custom application development or paid add-ons. It should stop early if the trial cannot be constrained to Lite-equivalent behavior or if Lite cannot pass a mandatory gate.

This outcome was explicitly approved as D-095 on August 1, 2026.

## Approved decision

- **Accepted (D-095):** Approve the P1-W03 proposed outcome and authorize detailed execution-contract drafting plus additional current official-evidence research only.
- **Accepted (D-096):** Approve the complete P1-W03 execution contract, including the Lite-only tier boundary, prototype ownership, execution sequence, minimum configuration, stopping rules, separate action gates, acceptance checks, and CP-007 effect.
- **Accepted (D-097):** Authorize the technical partner to create the bounded `Hazel Kaine` Pipedrive evaluator account and no-credit-card trial, then inspect only the nonprivate edition and feature boundary before stopping.
- **Accepted (D-098):** Authorize changing only the existing no-billing Pipedrive trial from Premium to Lite, removing carried-over trial add-ons, verifying the resulting plan and remaining trial, and then stopping before configuration.
- D-095 does not authorize account creation, trial activation, configuration, fixture entry, testing, integrations, billing, purchases, real data, customer communications, Loryn participation, production use, checkpoint sign-off, or platform selection.
- D-096 approves the contract only and preserves every separate action gate.
- D-097 does not authorize configuration, fixture entry, synthetic testing, integrations, billing, purchases, real data, customer communications, production use, Loryn participation, checkpoint sign-off, or platform selection.
- D-098 authorizes only the completed Lite plan-boundary change and readback. It does not authorize record inspection, configuration, fixture entry, synthetic testing, integrations, billing, purchases, real data, customer communications, production use, Loryn participation, checkpoint sign-off, or platform selection.

## Why Pipedrive is proposed next

- Official pricing offers a 14-day full-access trial with no credit card required.
- Lite is listed at `$14` per seat per month when billed annually, or `$168` per seat per year. The approved two-administrator production model would therefore start at `$336` per year before tax if Lite proves sufficient.
- Lite allows 30 custom fields per company, 2,500 leads and deals per seat, customizable pipelines, import and export, duplicate merging, and API access.
- Pipedrive represents reusable people related to multiple deals and links activities to people, organizations, leads, and deals.
- Official mobile documentation lists Focus, pipeline, activities, calendar, contacts, filtering, offline mode, audio notes, push notifications, and Nearby views on both iOS and Android. Nearby can open an address in the phone's navigation application.
- Global search includes person name and phone number, matching Loryn's stated lookup preferences.
- Deal sorting by next activity, activity reminders, overdue scheduling visibility, and advanced filters provide a plausible path to the morning action center and visible exception reporting.

## Decision-critical risks

- The CP-003 mapping must prove that the 30-field Lite allowance is sufficient after appropriate default fields are used. Do not collapse required data into notes merely to fit the limit.
- Required-field enforcement is Premium-only. Lite must instead prove that filters and practical views visibly expose active records missing a next action, due date, source-specific data, or exception result.
- Direct tenant inspection confirmed that the trial started on Premium and carried LeadBooster, Smart Docs, and Projects into the first change summary. D-098 removed all three and verified a clean Lite billing overview before configuration, resolving the initial contamination blocker.
- M-01 must be proven directly: today's appointments, people to contact, overdue actions, jobs waiting on someone else, and records missing a next action must be practically reachable as one morning action center or an approved equivalent.
- Direct tenant comparison confirms Lite at `$24` per seat per month on monthly billing. Renewal behavior, taxes, trial-retention behavior, exact two-administrator checkout cost, permissions, and access-removal workflow remain to be verified.
- Mobile behavior, save reliability, offline recovery, field search, directions, manual communications, exports, duplicates, and the Centah bridge remain untested.

## Approved candidate and tier boundary

- Evaluate Pipedrive Lite only. Growth, Premium, Ultimate, Projects, LeadBooster, Smart Docs, and other add-ons are documentation-only unless a later decision changes the tier boundary.
- Use the 14-day no-credit-card trial only if the tenant can be constrained to Lite-equivalent behavior without billing information.
- Treat every full-trial or premium capability as unavailable until official evidence and direct tenant inspection both show that it belongs to Lite.
- Do not purchase or enter billing details in P1-W03.

## Approved prototype ownership

- The technical partner is the sole evaluator administrator under D-093.
- Loryn performs no setup, testing, evidence capture, reset, or homework. She remains deferred until a separately approved finalist session.
- Final production ownership and administrator roles remain undecided; cost evidence still uses the approved two-administrator target model.
- Keep credentials, MFA methods, recovery details, private emails, account identifiers, and session data out of all project artifacts.

## Approved execution sequence

1. Complete the Lite field-capacity map and direct official-feature inventory.
2. Obtain separate account-creation authorization.
3. Create a `Hazel Kaine` evaluator-only trial with no billing information, external connections, real data, or vendor sample data retained for testing.
4. Confirm the tenant's plan and feature boundary; stop if Lite-equivalent behavior cannot be isolated. Completed under D-098: Lite is active with no selected add-ons, no billing details, and the 14-day trial label preserved.
5. Obtain separate synthetic-configuration authorization.
6. Configure only the approved fields, pipeline, activity types, filters, and practical morning views.
7. Load the CP-004 synthetic fixtures, run TS-01 through TS-07, perform mobile timing, and export the synthetic result unless an early mandatory failure stops the run.
8. Remove or archive test-created artifacts using a verified narrow cleanup procedure and prepare the evidence-backed result.

## Approved minimum configuration

- Reusable people, Leads Inbox prospects, deals for individual jobs, and linked activities.
- The approved active-job stages and retained outcomes without adding an unapproved parallel project module.
- No more than the mapped 22 custom fields unless a later evidence-backed correction remains within Lite's 30-field limit.
- One distinct deal-level Centah lead-number field used only for Costco/Centah jobs.
- Practical filters or views for today's appointments, calls due today, overdue actions, waiting-on-others jobs, records missing a next action, and source-specific exceptions.
- Manual communications only. Do not connect email, calendar, maps accounts, Centah, or another external service; native address handoff to the phone's navigation app may be tested without signing into another service.

## Approved stopping rules

- Stop before account creation if the field map exceeds 30 or official evidence eliminates Lite.
- Stop before configuration if the trial cannot be constrained to Lite-equivalent behavior.
- Stop when a confirmed mandatory failure makes Pipedrive nonviable, except for one short check needed to document the failure.
- Record, rather than bypass, missing required-field enforcement, deal-level uniqueness, morning-view, mobile, export, or integration behavior.
- Never activate a higher tier, add-on, paid commitment, external connection, or custom application to make Pipedrive pass.

## Approved separate action gates

- Complete contract approval does not authorize an account.
- Account creation requires the later explicit instruction `Authorize the Pipedrive Lite trial account`.
- Configuration and synthetic testing require the later explicit instruction `Begin P1-W03 synthetic configuration`.
- A paid tier, billing action, production pilot, real data, external connection, Loryn finalist session, checkpoint, and platform selection each require separate later approval.

## Approved acceptance checks

- Exact tenant edition, trial-expiry behavior, two-administrator production cost, material limits, and higher-tier contamination are recorded.
- The 22-field map is directly confirmed or corrected without exceeding Lite's 30-field limit or hiding required facts in notes.
- The configured model or documented stopping failure covers every CP-003 record and next-action requirement.
- M-01 through M-13 and the weighted criteria contain evidence, confidence, and uncertainty; missing required evidence keeps the score incomplete.
- Search by last name and phone number, directions, appointments, notes, reminders, missing-next-action detection, deal-level Centah duplicate review, save reliability, mobile behavior, and export reconstructability are directly tested while the candidate remains viable.
- The committed evidence contains only sanitized summaries and synthetic data and passes a secret/privacy review.
- The result identifies Pipedrive as viable, eliminated, or incomplete; Loryn remains uninvolved.

## Approved CP-007 effect

CP-007 would approve only a completed Pipedrive evaluator result, configuration inventory, exact tier and cost record, and evidence-backed comparison status. It would not select Pipedrive, authorize payment or production use, connect Centah or another service, import real data, permit customer communication, or start a Loryn finalist session.

## Continuing boundary

- The bounded account shell, trial, and Lite-only plan boundary are complete under D-097 and D-098. Record inspection, configuration, fixture entry, testing, integrations, billing, purchases, real data, customer communications, Loryn participation, production use, checkpoint sign-off, and platform selection remain unapproved.
- Loryn remains uninvolved until a candidate becomes one of no more than two viable finalists and a separate finalist-session gate is approved.

## Current action gate

The D-098 plan transition is complete. Direct evidence in `../evidence/P1-W03/pipedrive/tenant-shell-inspection.md` confirms Lite, one seat, `$24` monthly pricing, `$0` during the trial, no active add-ons, no billing details, and the preserved `14-day free trial` label. The exact calendar expiration date was not displayed. The Activities count changed from three to four during the vendor plan transition, but no record was inspected and all preloaded content remains untouched.

The next gate is the separately required `Begin P1-W03 synthetic configuration` authorization. Until that exact approval is received, do not inspect or clean preloaded records, configure fields or lifecycle elements, enter fixtures, or run tests.
