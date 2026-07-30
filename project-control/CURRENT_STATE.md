# Current Project State

**Updated:** July 30, 2026

**Overall status:** Active - Phase 1 execution contract approved; account action pending
**Current phase:** Phase 1 - Zoho prototype and HubSpot comparison
**Active work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Work-unit status:** Approved for execution - account creation authorization pending

**Last signed-off checkpoint:** CP-004 - CRM platform evaluation method (July 30, 2026)

## Confirmed baseline

- The product is a mobile-first workflow system for an independent window-covering sales consultant.
- Existing CRM products will be evaluated and configured before considering a custom application.
- Zoho CRM Free is the first prototype candidate; HubSpot Free and the current Centah-only workflow are comparison baselines.
- Centah remains authoritative for Centah-originated identifiers and governed fields until a later mapping decision changes that boundary.
- Each new order receives a new Centah lead number; store that identifier on the opportunity, not the reusable customer record.
- A returning customer may have multiple opportunities.
- Transfer only active and sold Centah leads; exclude canceled/inactive leads.
- Permitted transfer fields are name, phone, email, full address, Centah notes, appointments, quoted amount, and Centah lead number.
- Synthetic-only trials require no company permission. Real records are allowed in the selected production CRM only after access, security, retention, and export controls are configured.
- Real records remain prohibited from this ChatGPT Project, repository, documentation, tests, and trial fixtures.
- The initial post-sale workflow uses a six-week checkpoint after DocuSign. If installation is incomplete, add a note and defer by two to three weeks, repeating until installation is confirmed; then perform one post-install follow-up.
- Ongoing support and future repair-case management are outside the initial CRM scope.
- The project uses guided work units, explicit sign-off, durable checkpoints, and a simple two-person delivery model.
- The CRM must also support independently sourced leads and prospecting for possible future clients outside Centah/Costco.
- Confirmed prospecting sources include referrals, builders, networking, past customers, social media, purchased lists, local businesses, and direct outreach.
- A prospect may begin with a person name, business name, or social identity plus at least one reachable channel or location; source, next action, and follow-up date are always required.
- Approved prospecting activities are calls, texts, emails, social messages, in-person/networking conversations, mailed material, referral requests or introductions, research/preparation, and notes.
- Default reminder intervals are 2 days for engaged prospects, 7 days for warm prospects/referrals, 30 days for cold outreach or purchased-list prospects, 90 days for long-term prospects, and 6 months for past customers with possible future work; all are manually overridable and do not send automatically.
- A prospect converts when a real project is confirmed and the initial meeting is scheduled. The prospecting sequence closes as `Converted`, the customer and activity history remain intact, and one opportunity for that project begins at `Consultation Scheduled` with the morning-of confirmation as its next action. A direct inquiry about an immediate project may enter at this stage without first using prospecting.
- The approved active-job statuses are `New Customer Request`, `Trying to Contact`, `Appointment Scheduled`, `Appointment Completed`, `Preparing Quote`, `Quote Sent - Awaiting Decision`, `Customer Accepted - Handoff Due`, `Handoff Complete - Installation Pending`, `Installed - Customer Follow-Up Due`, and `Finished`. `Lost / Canceled` is an exit available where applicable, and an installation unconfirmed at three months becomes a visible exception.
- Calling hours are Monday through Friday from 9:00 a.m. to 6:00 p.m. and Saturday from 9:00 a.m. to 2:00 p.m. A new request received during those hours requires a manual first-contact attempt by closing time that day. A request received outside those hours is due at 9:00 a.m. on the next working day; Sunday rolls to Monday. The CRM creates a reminder and does not contact the customer automatically.
- After an unanswered first attempt on an active customer request, retry on the next working day. If unanswered again, make a third and final attempt two working days later. A third nonresponse closes the opportunity as `Lost / Canceled - No Response`; retain the record and notes and stop active-job reminders. Costco/Centah leads also follow the approved Centah cancel-to-inactive process. This does not change the separate long-term prospecting rules.
- For an appointment happening that day, create a reminder to send the manual confirmation text at approximately 7:45 a.m. This is a confirmation-text exception only. A confirmation phone call must wait until calling hours begin at 9:00 a.m.
- After a completed appointment that requires a quote, the primary goal is to finish and manually send the quote by the end of that same working day. If it is not sent by closing time, the quote task becomes visibly overdue and remains open until a new due date is recorded or the quote is sent.
- When the same-day quote target is missed, require a short delay reason and set the fallback deadline to the end of the next working day. A missed fallback stays overdue and requires another deliberate date and reason rather than being silently rescheduled.
- Immediately after emailing a quote, send a manual message through the customer's preferred and permitted channel telling them the quote was sent and asking them to check their email. Create the next manual decision-follow-up task for three working days later. If the customer responds first, cancel the reminder and record the response and resulting next action. No message is sent automatically.
- If the three-working-day post-quote follow-up receives no response, create another manual follow-up for one week later during normal calling hours and keep the opportunity at `Quote Sent - Awaiting Decision`.
- Continue unanswered quote follow-ups once a week for no more than three weeks. After the third weekly nonresponse, close the opportunity as `Lost / Canceled - No Decision`, retain the quote and communication history, and stop reminders. If the customer requests more time, use their requested date instead of the weekly schedule.
- When the customer accepts, complete the source-specific handoff by the end of that working day or by 9:00 a.m. on the next working day after an outside-hours acceptance. Costco/Centah requires both DocuSign and the quote emailed to the internal order coordinator; independent work skips DocuSign and requires only the coordinator email. Do not mark the handoff complete until all required items have actually been sent.
- After handoff, check installation at six weeks using the DocuSign-sent date for Costco/Centah work or the coordinator-email date for independent work. If installation is unconfirmed, add a note and check again in two to three weeks. At three months after the sold quote was emailed to the coordinator, stop normal deferral, show an urgent exception, contact the coordinator that day, and contact the customer if necessary. Never mark installation complete without human confirmation.
- After installation is confirmed, complete one manual customer follow-up by the end of the next working day. If the customer confirms everything is satisfactory, mark the job `Finished` and schedule the six-month past-customer reminder. If the customer reports a problem, keep it visibly unresolved with a next action and do not mark it finished; detailed repair-case management remains outside the initial CRM scope.
- If the customer does not answer the one post-install follow-up on a confirmed-installed job, record `Post-Install Follow-Up Attempted - No Response`, mark the job `Finished`, and stop post-install reminders. Schedule the six-month past-customer reminder only if the customer has not opted out and there is no known unresolved problem.
- The approved minimum CRM fields are assigned to customer/contact, opportunity/job, and task/activity records in `../deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`. Centah lead number is required and unique only for Costco/Centah jobs and prohibited for independent jobs.
- After acceptance, Centah/Costco opportunities require DocuSign and an emailed quote to the internal order coordinator in parallel. Opportunities outside Centah/Costco skip DocuSign and require only the emailed quote to the internal order coordinator.
- The six-week installation-check timer starts on the DocuSign-sent date for Centah/Costco sales and on the internal-order-email date for sales outside Centah/Costco.
- Installation should never take more than three months from the date the sold quote is emailed to the internal order coordinator; an unconfirmed installation at that boundary must become a visible exception rather than receiving indefinite routine deferrals.
- At the three-month exception, the CRM creates a same-day task to contact the internal order coordinator, requires a recorded result, prompts customer contact if the coordinator cannot confirm installation, and never marks installation complete without human verification.
- Prospect exit rules are approved: three unanswered attempts move the record to one 90-day nurture attempt; another nonresponse archives it. Declines, do-not-contact requests, invalid information, and duplicates use explicit retained outcomes.
- Prospect records will store preferred channel, acquisition source/date, permission status, overall do-not-contact information, and channel-specific opt-outs. Purchased-list imports and automated outreach require a later communications-compliance review.
- Eligible past customers enter prospecting six months after post-install follow-up for possible additional work and referrals, using a permitted letter, email, text, or call; opted-out customers and unresolved problems are excluded.
- Past-customer reminders may repeat at 6, 12, 18, and 24 months after post-install follow-up, then stop. An explicit rejection or opt-out ends the sequence immediately.
- Only Costco-originated opportunities use Centah. Independently sourced prospects and opportunities remain only in the selected CRM, are not entered into Centah, and do not require a Centah lead number.
- P0-W03 mandatory gates M-01 through M-13 are approved for the draft evaluation and recorded in `../deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`.
- The gates cover the daily action center, source-specific workflow, essential mobile speed, reminders, administration, portability, the approved record model, human-controlled communications, the Centah bridge, save reliability, cost evidence, sustainable administration, and a common synthetic evidence standard.
- Full offline capability remains a weighted preference; silent data loss or duplication is a mandatory failure.
- Loryn is the primary administrator and daily user. One secondary administrator provides occasional setup, troubleshooting, recovery, and other ad hoc administration.
- P0-W03 category weights total 100: mobile daily-work usability 35, workflow visibility and configuration 20, governance/security/administration 15, data portability and reliability 10, cost and maintenance burden 10, and Centah/integration fit 10.
- Mandatory gates override the weighted total; an applicable `Fail` or `Unverified` gate prevents a platform from being preferred.
- Weighted criteria use a common integer scale from 0 to 5 and contribute `criterion weight × score ÷ 5` to the 100-point total.
- Every score requires evidence and confidence. Missing evidence leaves the total incomplete and is never normalized away.
- The 35 mobile points are allocated as daily action center 10, essential task efficiency 10, customer/job search 5, appointment confirmation and directions 5, and mobile note capture and weak-signal behavior 5.
- The 20 workflow points are allocated equally across lifecycle/record configuration, next-action/overdue visibility, source-specific handoff/installation exceptions, and office workflow/activity/reporting.
- The 15 governance points are allocated 4/4/4/3 across secure account access, simple administration/access management, useful activity history, and retention/deletion guidance. Score only right-sized needs for a one-person operation; unused enterprise complexity earns no extra credit.
- The 10 portability/reliability points are allocated as usable data exports 4, understandable customer-to-job relationships after export 3, and saving/synchronization/recovery quality 3.
- The 10 cost/maintenance points are allocated as actual recurring cost for two administrators and required features 5, ongoing training/cleanup/support effort 3, and pricing clarity/forced-upgrade risk 2.
- The 10 Centah/integration points are allocated as practical Costco/Centah job and identifier handling 4, duplicate checking/reconciliation 3, and evidence-backed future import/export/API options 3. Unknown Centah capabilities remain unverified.
- All criterion-level weights now total 100.
- Seven common scenario areas are approved: quick prospect capture, morning action center, Costco/Centah lead handling, appointment workflow, visit/quote follow-up, both accepted-sale handoff branches, and the three-month installation exception.
- Eight fixed synthetic fixtures use clearly fictional identities and relative T0 dates to give all three candidates identical starting conditions, including an intentional missing-next-action negative test.
- TS-01 through TS-07 now have approved common execution rules, exact steps, timing boundaries, no-send/no-travel controls, and expected results.
- Evaluator screening covers all candidates first. Loryn tests no more than two viable finalists in one guided session of about 20 minutes each and receives no homework or follow-up test tasks.
- The evaluator uses one test-run header and one compact result row per gate or criterion; Loryn does no evidence-recording work.
- CP-004 approved the complete P0-W03 platform-evaluation method; no platform has been scored or selected.
- P1-W01 account ownership is approved: Loryn is the account owner and primary administrator, and the technical partner is the secondary administrator for approved ad hoc support.
- Account recovery remains under Loryn's control. Credentials, recovery codes, and MFA secrets are prohibited from Codex and project artifacts.
- The P1-W01 execution contract is approved; account creation and synthetic configuration remain separately unapproved, and no Zoho account action has been authorized.
- The minimum Zoho scope is approved for contract design: standard customer/prospect/job/task records, CP-003 minimum fields, approved stages and source rules, manual next actions, five practical views, eight synthetic fixtures, and manual communications.
- Real data, external connections, automatic messages, custom code, purchases, paid upgrades, detailed quote attachments, HubSpot configuration, and final scoring remain outside P1-W01.
- A Zoho Free limitation must be recorded rather than bypassed through unapproved scope expansion or purchase.
- The approved fixture procedure uses one repository sheet, preloads seven records, creates `SYN-PROSPECT-A` during TS-01, restores T0-relative states before each run, and assigns all setup/reset work to the evaluator.
- Fixture cleanup removes only the test-created prospect and duplicate attempt and restores changed synthetic fixtures; bulk deletion of unrelated records is prohibited.
- Zoho screening proceeds through official-evidence preflight, configuration viability, synthetic scenarios, evaluator mobile timing, and result summary, stopping after a confirmed mandatory failure with no acceptable production-tier or in-scope path.
- Paid-tier possibilities require exact feature and cost evidence for `Conditional Pass`; missing evidence stays `Unverified`, and no tier may be purchased or activated in P1-W01.
- Loryn does not test during P1-W01; her finalist sessions remain deferred until all candidates complete evaluator screening.
- Raw trial captures must remain in ignored local `.trial-evidence/`; only reviewed sanitized summaries, official links, screenshots, or exports may be committed under `evidence/P1-W01/zoho/`.
- Credentials, MFA/recovery material, cookies, tokens, account identifiers, billing details, private notifications, and unrelated personal information are prohibited from evidence artifacts.
- Zoho Free is the only prototype tier. Billing, paid trials, upgrades, and purchases are prohibited in P1-W01.
- A missing Free feature receives `Conditional Pass` only with exact official evidence for the lowest supporting tier, current cost, user limit, and restrictions; temporary promotional features do not count as Free.
- Account creation requires the exact instruction `Authorize Loryn to create the Zoho Free trial account` after contract approval.
- Configuration and testing require the later exact instruction `Begin P1-W01 synthetic configuration`; account creation alone does not authorize them.
- Loryn creates the account herself with private credentials, MFA, and recovery, a neutral synthetic organization label, no employer/Costco/Centah/customer information, and no billing or paid upgrade.
- P1-W01 acceptance requires current official tier, administrator, MFA, export, limit, and cost evidence; verified administrator roles after separate account authorization; the approved minimum configuration or documented limitations; resettable synthetic fixtures; evaluator screening; evidence-backed results; a privacy and secret review; and a clear viable, eliminated, or incomplete outcome.
- Any score remains incomplete while required evidence is `Unverified`, and Loryn performs no P1-W01 testing, setup, reset, evidence capture, or homework.
- CP-005 will approve only the Zoho evaluator result and configuration inventory. It will not select a platform or authorize HubSpot setup, Loryn finalist testing, production use, real data, integrations, purchases, communications, or automation.
- The complete P1-W01 execution contract is approved. Contract approval does not authorize account creation or synthetic configuration.

## Active work-unit contract

**Status:** Approved for execution; both account action gates remain closed.

**Outcome:** Create and evaluate the smallest useful synthetic Zoho CRM Free prototype against the CP-004 mandatory gates and scenarios, then determine whether Zoho remains viable for the candidate pool.

**Inputs:**

- The signed CP-003 lifecycle, next-action, and minimum-field specification.
- The signed CP-004 scorecard, mandatory gates, fixtures, scenarios, burden limit, and evidence format.
- Approved P1-W01 decisions D-075 through D-083.

**Acceptance checks:**

- Current official evidence records tier, two-administrator support, MFA, exports, limits, and expected production cost.
- Account ownership and administrator roles are verified after separately authorized account creation.
- The approved minimum configuration is completed or unsupported items are documented with evidence.
- All eight synthetic fixtures can be restored to their approved T0-relative baseline without real data.
- TS-01 through TS-07 receive evaluator screening unless an approved early-stop condition applies.
- Every applicable gate and criterion records its result or score, evidence, confidence, and uncertainty; totals remain incomplete when required evidence is `Unverified`.
- Privacy and secret review passes, and the result identifies Zoho as viable, eliminated, or incomplete with named blockers.
- Loryn performs no P1-W01 testing, evidence capture, fixture setup, reset, or homework.

**CP-005 effect:** Approve only the completed Zoho evaluator result and configuration inventory.

**Out of scope:** Platform selection, HubSpot setup, Loryn finalist testing, production use, real records, external integrations, purchases, customer communications, or automation.

## Open items

- D-011: production CRM tenant, sign-in method, access removal, and security/retention controls.
- D-012: Centah API, webhook, export, sandbox, limits, and support model.
- D-013: retention and deletion periods.
- D-014: exact Costco program fields and restrictions.
- D-016: final platform trial result.
- D-017: whether a Centah adapter is justified after the manual bridge.
- Complete the current communications-compliance review before purchasing/importing prospect lists or enabling automated outreach.
- Deferred: whether detailed quote files enter the CRM and whether the personal Google account may connect directly.

## Completed checkpoints

CP-001 approved `../deliverables/P0-W01-current-workflow-and-permission-boundary.md`. Decisions D-020 through D-023 record the approved production boundary, transfer filter and Centah identifier model, post-install reminder rule, and initial support scope.

CP-002 approved `../deliverables/P0-CR01-independent-leads-and-prospecting-scope.md`. Decisions D-024 through D-029 record the separate prospecting lifecycle, Costco-only Centah boundary, prospect cadence and outcomes, source-specific post-sale handoff, installation exception, past-customer outreach, and communication controls. Word is intentionally deferred and marked stale until a release or sharing milestone.

CP-003 approved `../deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`. Decisions D-033 through D-048 record prospect conversion, the active-job stages, contact and quote timing, follow-up limits, source-specific handoff, installation and post-install rules, and the minimum customer/job/task fields. D-035 and D-040 were superseded during the signed design sequence. At CP-003, the authoritative Markdown master was Version 1.24; Word remains intentionally stale until a release or sharing milestone.

CP-004 approved `../deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`. Decisions D-049 through D-061 record the mandatory gates, D-062 through D-069 record the complete 100-point scorecard and scoring rule, D-070 through D-072 record the scenarios, fixtures, and scripts, D-073 records the staged test-burden rule, and D-074 records the evaluator-only evidence format. At CP-004, the authoritative Markdown master was Version 1.39; Word remains intentionally stale.

P1-W01 is in progress. D-075 through D-083 record the approved execution contract in `../deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`, including the limited CP-005 effect and separate account action gates. Both account actions remain unapproved. The authoritative Markdown master is Version 1.48; Word remains intentionally stale.

## Chat and artifact protocol

- Keep the current guided checkpoint in one pinned project chat.
- Use separate project chats for materially different outcomes and reconcile their results into the guided checkpoint before sign-off.
- Treat Markdown and project-control files as authoritative; chat transcripts and Word copies are not restart sources.
- Generate and fully verify Word only at a final release or explicit sharing milestone.
- Use `COLLABORATOR_PACKET.md` to collect asynchronous mobile input in a shared ChatGPT Project. Its handoffs remain unapproved until reconciled and explicitly signed off through this repository workflow.

## Repository backup

- **Remote:** `https://github.com/jonah-dawg/loryn-work-optimization.git`
- **Branch:** `main`
- **Local checkout:** `C:\Users\jonah\Documents\GitHub\loryn-work-optimization`
- **Tracked scope:** authoritative Markdown deliverables and project-control files, plus repository guidance.
- **Excluded from routine checkpoints:** the stale Word distribution copy, rendering/QA intermediates, ChatGPT-synced source mirrors, credentials, real customer data, and local temporary files.
- Until the repository folder is attached or opened as the primary Codex project, the app-managed project folder remains the interactive working copy and the repository is refreshed from it at saved checkpoints.

## Next work-unit starting point

Phase 0 is complete at CP-004. Phase 1 has started with an approved P1-W01 execution contract. Both account action gates remain closed.

## Exact next action

If account creation should proceed, obtain the exact instruction `Authorize Loryn to create the Zoho Free trial account`. Do not treat contract approval as account authorization, and do not begin configuration or testing after account setup.

## Resume instruction

Read this file, Sessions S-039 through S-048 in `SESSION_LOG.md`, `../deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`, `../deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`, and the Phase 1 and platform-trial sections of `../deliverables/window-sales-operations-master-plan.md`. The P1-W01 contract is approved. Do not create a CRM account unless the user gives the exact account-creation authorization, and do not configure or test it unless the user later gives the separate exact configuration authorization. Continue to prohibit real data, external connections, purchases, customer communications, and platform selection.
