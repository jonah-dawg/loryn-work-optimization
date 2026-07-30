# Current Project State

**Updated:** July 29, 2026  
**Overall status:** Active - guided execution underway  
**Current phase:** Phase 0 - Authority, workflow, and evaluation design  
**Active work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields  
**Work-unit status:** In progress; Decisions 1 through 9 approved, Decision 10 next
**Last signed-off checkpoint:** CP-002 - Independent leads and prospecting scope (July 29, 2026)

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
- After acceptance, Centah/Costco opportunities require DocuSign and an emailed quote to the internal order coordinator in parallel. Opportunities outside Centah/Costco skip DocuSign and require only the emailed quote to the internal order coordinator.
- The six-week installation-check timer starts on the DocuSign-sent date for Centah/Costco sales and on the internal-order-email date for sales outside Centah/Costco.
- Installation should never take more than three months from the date the sold quote is emailed to the internal order coordinator; an unconfirmed installation at that boundary must become a visible exception rather than receiving indefinite routine deferrals.
- At the three-month exception, the CRM creates a same-day task to contact the internal order coordinator, requires a recorded result, prompts customer contact if the coordinator cannot confirm installation, and never marks installation complete without human verification.
- Prospect exit rules are approved: three unanswered attempts move the record to one 90-day nurture attempt; another nonresponse archives it. Declines, do-not-contact requests, invalid information, and duplicates use explicit retained outcomes.
- Prospect records will store preferred channel, acquisition source/date, permission status, overall do-not-contact information, and channel-specific opt-outs. Purchased-list imports and automated outreach require a later communications-compliance review.
- Eligible past customers enter prospecting six months after post-install follow-up for possible additional work and referrals, using a permitted letter, email, text, or call; opted-out customers and unresolved problems are excluded.
- Past-customer reminders may repeat at 6, 12, 18, and 24 months after post-install follow-up, then stop. An explicit rejection or opt-out ends the sequence immediately.
- Only Costco-originated opportunities use Centah. Independently sourced prospects and opportunities remain only in the selected CRM, are not entered into Centah, and do not require a Centah lead number.

## Active work-unit contract

**Outcome:** Approve the connected prospecting and active-opportunity lifecycles, stage-specific next-action rules, and minimum CRM field set.

**Inputs:**

- The signed P0-W01 Centah/Costco workflow and permission boundary.
- The signed P0-CR01 independent-lead and prospecting scope.
- Decisions D-024 through D-029 governing lifecycle separation, source branching, reminders, installation exceptions, and communication controls.

**Acceptance checks:**

- Every meaningful prospect and opportunity state has one defined stage or explicit substate.
- Every active prospect and opportunity has a next action and due date, or a documented closed/exception state.
- Contact attempts, consultation, quote, accepted/sold, canceled/inactive, installation-check, three-month exception, post-install follow-up, and past-customer re-entry are represented.
- Required fields are assigned to the correct record type and limited to what the workflow uses.
- Centah lead number is required and unique only for transferred Costco/Centah opportunities, never for independent prospects or opportunities.
- A sanitized example can traverse prospect-to-opportunity conversion and the Costco/Centah lead path without relying on text history or memory.

**Out of scope:** Creating CRM accounts, configuring Zoho or HubSpot, importing real records, connecting Centah/Google/calendar/email, selecting the final platform, purchasing prospect lists, sending customer communications, or implementing automation.

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

CP-002 approved `../deliverables/P0-CR01-independent-leads-and-prospecting-scope.md`. Decisions D-024 through D-029 record the separate prospecting lifecycle, Costco-only Centah boundary, prospect cadence and outcomes, source-specific post-sale handoff, installation exception, past-customer outreach, and communication controls. The authoritative Markdown master is Version 1.7. Word is intentionally deferred and marked stale until a release or sharing milestone.

## Chat and artifact protocol

- Keep the current guided checkpoint in one pinned project chat.
- Use separate project chats for materially different outcomes and reconcile their results into the guided checkpoint before sign-off.
- Treat Markdown and project-control files as authoritative; chat transcripts and Word copies are not restart sources.
- Generate and fully verify Word only at a final release or explicit sharing milestone.

## Repository backup

- **Remote:** `https://github.com/jonah-dawg/loryn-work-optimization.git`
- **Branch:** `main`
- **Local checkout:** `C:\Users\jonah\Documents\GitHub\loryn-work-optimization`
- **Tracked scope:** authoritative Markdown deliverables and project-control files, plus repository guidance.
- **Excluded from routine checkpoints:** the stale Word distribution copy, rendering/QA intermediates, ChatGPT-synced source mirrors, credentials, real customer data, and local temporary files.
- Until the repository folder is attached or opened as the primary Codex project, the app-managed project folder remains the interactive working copy and the repository is refreshed from it at saved checkpoints.

## Approved progress within current work unit

P0-W02 Decisions 1 through 9 were explicitly approved by the user on July 29, 2026. D-033, D-034, D-036 through D-039, and D-041 remain active. D-035 was superseded by D-037, and D-040 was superseded by D-041. These decisions cover prospect conversion, active-job stages, contact timing, the three-attempt no-response rule, calling hours, the confirmation-text exception, quote deadlines, the immediate quote-sent notice, and the three-working-day decision follow-up. Later stage-specific next-action rules and minimum fields are not approved yet.

## Exact next action

Review P0-W02 Decision 10 with the user in plain language: decide what reminder should follow if the three-working-day post-quote follow-up does not produce a customer decision.

## Resume instruction

Read this file, Sessions S-004 and S-006 through S-014 in `SESSION_LOG.md`, `../deliverables/P0-W01-current-workflow-and-permission-boundary.md`, `../deliverables/P0-CR01-independent-leads-and-prospecting-scope.md`, and the lifecycle sections of `../deliverables/window-sales-operations-master-plan.md`. Decisions 1 through 9 are approved, with D-035 superseded by D-037 and D-040 superseded by D-041. Resume at Decision 10, the next reminder after an unanswered three-working-day post-quote follow-up, without opening a CRM account, using real customer data, or treating later next-action/field proposals as approved before CP-003.
