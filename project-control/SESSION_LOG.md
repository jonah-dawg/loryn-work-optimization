# Project Session Log

Append new entries at the end. Signed-off entries are immutable; corrections must be recorded in a later entry that references and supersedes the earlier statement.

## Session S-001 - Guided workflow initialization

**Date:** July 29, 2026  
**Phase:** Phase 0  
**Work unit:** Workflow setup; P0-W01 prepared  
**Checkpoint:** CP-000  
**Sign-off status:** Signed off July 29, 2026

**Approval evidence:** The user explicitly approved beginning execution with: “let's do this shit.”

### Completed

- Defined the interactive work-unit, checkpoint, sign-off, synchronization, and resume protocol.
- Established durable current-state, session-log, and artifact-register controls.
- Set Phase 0 work unit P0-W01, Current workflow and permission boundary, as the next interactive step.
- Added the guided-execution protocol to the master plan.

### Validation

- The workflow distinguishes work-unit sign-off from phase-gate sign-off.
- It requires explicit approval and preserves unsigned work as unapproved.
- It includes reconciliation of the master plan, decisions, state, artifacts, and sensitive-data boundaries.
- The saved state contains an exact next action and resume instruction.

### Decisions and assumptions

- **Accepted (D-018):** Use the guided workflow and checkpoint protocol for all remaining phases.
- **Accepted (D-019):** Use a simple two-person delivery model with no formal role roster.
- **Confirmed:** No project checkpoint broadens permission to use production data, create external accounts, purchase services, or communicate with customers.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `deliverables/window-sales-operations-master-plan.docx`
- `project-control/GUIDED_WORKFLOW.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

P0-W01 is ready. Walk through one sanitized Costco/Centah lead and record the current workflow and permission unknowns; do not begin CRM configuration or copy real customer data yet.

## Session S-002 - Current workflow and permission boundary

**Date:** July 29, 2026  
**Phase:** Phase 0  
**Work unit:** P0-W01 - Current workflow and permission boundary  
**Checkpoint:** CP-001  
**Sign-off status:** Signed off July 29, 2026

**Approval evidence:** The user explicitly said, “Sign off CP-001.”

### Completed

- Mapped the current Costco/Centah workflow from lead receipt through the post-install follow-up rule.
- Identified Centah, iPhone Calendar, text/phone/email, personal Google Sheets, PDF, DocuSign, and internal email handoffs.
- Confirmed duplicate appointment entry, memory-driven quote follow-up, an email-only internal handoff, and missing post-handoff status visibility.
- Confirmed that canceled leads remain in Centah as inactive rather than being permanently deleted.
- Confirmed the synthetic-trial and approved real-data transfer boundary.
- Confirmed that only active and sold leads transfer and that every new order receives a new opportunity-level Centah lead number.
- Defined the six-week post-DocuSign checkpoint and repeating two-to-three-week deferral rule when installation remains incomplete.
- Excluded ongoing support and future repair-case management from the initial CRM scope.

### Validation

- The signed workflow artifact contains no customer names, addresses, phone numbers, email addresses, or other supplied identifying data.
- All P0-W01 acceptance checks passed before sign-off.
- Master Markdown and editable Word content were synchronized at Version 1.4.
- LibreOffice rendered the final Word document to 25 pages; every page was visually inspected at original detail with no clipping, overlap, broken tables, missing glyphs, or footer defects.
- Table-geometry and section audits passed; the document contains one US Letter portrait section with one-inch margins.
- Heading audit found 17 Heading 1 and 42 Heading 2 paragraphs. Numbering warnings apply to intended list items, not missing section-heading styles.
- Accessibility audit reported zero high-severity findings. Nine medium findings are non-data layout/decorative tables without header rows; actual data tables use header rows.

### Decisions

- **Accepted (D-020):** Keep project, repository, test, and trial artifacts synthetic; place approved real fields only in the controlled production CRM.
- **Accepted (D-021):** Transfer only active and sold Centah leads and store the Centah lead number on each opportunity.
- **Accepted (D-022):** Create a six-week post-DocuSign checkpoint, defer by two to three weeks while installation is incomplete, then perform one post-install follow-up.
- **Accepted (D-023):** Exclude ongoing support and future repair-case management from the initial CRM scope.
- **Superseded (D-009):** The earlier blanket synthetic-until-written-authorization rule is replaced by the narrower artifact and production boundary in D-020.

### Deferred or unresolved

- Whether complete quote files should be linked to or stored in the selected CRM.
- Whether the consultant's personal Google account may connect directly to the CRM.
- Centah export/API details, status dictionary, and integration limits.
- Production tenant access, security, retention, export, and recovery controls.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `deliverables/window-sales-operations-master-plan.docx`
- `deliverables/P0-W01-current-workflow-and-permission-boundary.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

CP-001 is complete. P0-W02 is ready to define the target pipeline, stage-specific next-action rules, and minimum CRM fields using only sanitized examples.

## Session S-003 - Independent leads and prospecting scope

**Date:** July 29, 2026  
**Phase:** Phase 0  
**Work unit:** P0-CR01 - Independent leads and prospecting scope change  
**Checkpoint:** CP-002  
**Sign-off status:** Signed off July 29, 2026

**Approval evidence:** The user explicitly said, “Sign off CP-002.”

### Completed

- Defined independent prospecting sources, minimum viable capture, permitted activities, reminder cadence, conversion trigger, retained outcomes, and archive rules.
- Separated the pre-opportunity prospecting lifecycle from the active sales lifecycle while preserving source and activity history at conversion.
- Confirmed that only Costco-originated opportunities use Centah and require an opportunity-level Centah lead number.
- Defined the source-specific sold workflow: Costco/Centah uses DocuSign and the emailed quote to the internal order coordinator in parallel; independent business uses only the emailed quote to the coordinator.
- Anchored the six-week installation check by source and created a visible three-month installation exception with human verification.
- Defined past-customer outreach at 6, 12, 18, and 24 months after post-install follow-up, stopping at two years or immediately after rejection or opt-out.
- Added communication provenance, preferred-channel, permission, and opt-out requirements plus a compliance gate for purchased lists and automated outreach.
- Adopted a hybrid ChatGPT Project workflow: one pinned guided chat per active checkpoint, separate chats for materially different outcomes, and durable Markdown handoffs.
- Made Markdown the live source of truth and deferred Word regeneration until a final release or explicit sharing milestone.

### Validation

- Every CP-002 acceptance check passed before sign-off.
- The signed scope artifact and master plan contain no supplied customer records or credentials.
- Master Markdown Version 1.6, current state, workflow protocol, artifact register, and session log were reconciled.
- The Word distribution copy was intentionally left at Version 1.4 and marked stale under the newly approved milestone-only generation policy.

### Decisions

- **Accepted (D-024):** Use a separate pre-opportunity prospecting lifecycle for independent sources.
- **Accepted (D-025):** Use Centah only for Costco leads; keep independent business solely in the selected CRM.
- **Accepted (D-026):** Require minimum prospect data and next actions; use bounded contact attempts, one 90-day nurture attempt, and retained outcomes.
- **Accepted (D-027):** Branch the sold handoff by source and enforce installation checks through a three-month exception.
- **Accepted (D-028):** Run eligible past-customer outreach at 6, 12, 18, and 24 months, then stop.
- **Accepted (D-029):** Record communication provenance, preferences, permission, and opt-outs, with compliance review before purchased lists or automation.
- **Accepted (D-030):** Use one pinned guided chat for the active checkpoint and separate project chats for materially distinct outcomes.
- **Accepted (D-031):** Maintain Markdown as the live source of truth and generate Word only for a final release or requested sharing copy.

### Deferred or unresolved

- Current communications-compliance review for purchased lists and automated outreach.
- Production CRM tenant controls, final platform selection, and CRM configuration.
- Centah export/API details, status dictionary, integration access, and limits.
- Whether complete quote files enter the CRM and whether the personal Google account may connect directly.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `deliverables/P0-CR01-independent-leads-and-prospecting-scope.md`
- `project-control/GUIDED_WORKFLOW.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

CP-002 is complete. P0-W02 is ready to define the connected prospecting and active-opportunity lifecycles, stage-specific next-action rules, and minimum CRM fields using sanitized examples. The next guided session starts with prospect conversion into a new active opportunity.

## Session S-004 - P0-W02 lifecycle design started

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Paused without sign-off

### Work in progress

- Reconciled the signed CP-001 and CP-002 baselines before beginning P0-W02.
- Presented Decision 1: the proposed prospect-to-opportunity conversion behavior.
- Proposed preserving one reusable customer identity and prospecting history, closing the prospect sequence as `Converted`, and creating one opportunity per project at `Consultation Scheduled`.
- Proposed setting the morning-of confirmation as the new opportunity's next action and allowing direct current-project inquiries to bypass prospecting.

### Approval status

Decision 1 was not accepted or rejected before the user paused the session. No P0-W02 lifecycle stages, next-action rules, or fields are authoritative yet.

### Files changed

- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Resume by asking the user to accept or revise Decision 1. Do not advance to the remaining active-opportunity stages until that decision is resolved.

## Session S-005 - GitHub backup established

**Date:** July 29, 2026  
**Phase:** Project infrastructure  
**Work unit:** Repository backup setup  
**Checkpoint:** No product checkpoint  
**Sign-off status:** Operational task requested by the user; CP-002 remains the last product approval

### Completed

- Selected `jonah-dawg/loryn-work-optimization` as the durable GitHub backup.
- Defined the local checkout, tracked Markdown scope, checkpoint synchronization procedure, exclusions, and recovery process.
- Kept the app-managed project folder as the interactive working copy until the repository folder is attached or opened as the primary Codex project.
- Excluded the stale Word copy, rendering intermediates, synced project sources, credentials, and real customer data from routine checkpoint backups.
- Replaced the internal coordinator's personal name with a role label before the initial repository snapshot.
- Preserved the P0-W02 pause point; Decision 1 remains unapproved.

### Decisions

- **Accepted (D-032):** Back up authoritative Markdown and project-control files to `jonah-dawg/loryn-work-optimization`.

### Files included in the repository snapshot

- `README.md`
- `AGENTS.md`
- `.gitignore`
- `deliverables/*.md`
- `project-control/*.md`

### Saved ending point

Repository backup is established without changing the P0-W02 product decision state. Resume P0-W02 at the unapproved prospect-conversion proposal.

## Session S-006 - P0-W02 Decision 1 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 1 explicitly approved

**Approval evidence:** After reviewing the prospect-to-opportunity conversion rule in plain language, the user said, “approved.”

### Accepted decision

- **Accepted (D-033):** A prospect converts when a real project is confirmed and the initial consultation is scheduled.
- Close the prospecting sequence as `Converted`, preserve the reusable customer record and prospecting history, and create one opportunity for that project at `Consultation Scheduled`.
- Set the morning-of appointment confirmation as the opportunity's first required next action.
- Allow a direct inquiry about an immediate project to enter at `Consultation Scheduled` without first passing through prospecting.

### Approval boundary

- This approval covers only P0-W02 Decision 1.
- The complete active-opportunity stage sequence, stage-specific next-action rules, and minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decision 1 is complete. Present Decision 2 in plain language: approve or revise the proposed active-opportunity stage sequence before defining the required next action for each stage.

## Session S-007 - P0-W02 Decision 2 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 2 explicitly approved

**Approval evidence:** After reviewing the recommended job-status list in plain language, the user said, “approved.”

### Accepted decision

- **Accepted (D-034):** Use ten plain-language active-opportunity stages: `New Customer Request`, `Trying to Contact`, `Appointment Scheduled`, `Appointment Completed`, `Preparing Quote`, `Quote Sent - Awaiting Decision`, `Customer Accepted - Handoff Due`, `Handoff Complete - Installation Pending`, `Installed - Customer Follow-Up Due`, and `Finished`.
- Allow `Lost / Canceled` as an exit from any applicable stage.
- Show an installation that remains unconfirmed at three months as a visible overdue-installation exception.
- Do not use normal stages that claim an order was placed or installation was scheduled unless the consultant receives reliable confirmation.

### Approval boundary

- This approval covers the active-opportunity stage sequence only.
- Stage-specific next-action rules and due timing remain unapproved.
- The minimum CRM field set remains unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 and 2 are complete. Present Decision 3 in plain language, beginning with how quickly a `New Customer Request` must receive its first contact attempt.

## Session S-008 - P0-W02 Decision 3 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 3 explicitly approved

**Approval evidence:** The user approved the proposed first-contact timing and specified, “m-f 10am-6pm Saturday 10am-2pm.”

### Accepted decision

- **Accepted (D-035):** Working hours are Monday through Friday, 10:00 a.m. to 6:00 p.m., and Saturday, 10:00 a.m. to 2:00 p.m.
- A `New Customer Request` received during working hours requires a manual first-contact attempt by closing time that day.
- A request received outside working hours requires the first contact attempt at 10:00 a.m. on the next working day; a Sunday request is due Monday at 10:00 a.m.
- The CRM creates a reminder for the consultant and does not contact the customer automatically.

### Approval boundary

- This approval covers the first-contact deadline and standard working hours.
- Holiday, vacation, and other unavailable-day handling may be configured later if the chosen CRM supports a practical business-calendar rule.
- Retry timing after an unanswered attempt remains unapproved.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 3 are complete. Present Decision 4 in plain language: decide the timing for the second and third contact attempts and the outcome after a third unsuccessful attempt.

## Session S-009 - P0-W02 Decision 4 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 4 explicitly approved

**Approval evidence:** The user answered “yes” to the proposed retry timing and no-response outcome.

### Accepted decision

- **Accepted (D-036):** After the first unanswered attempt on an active customer request, make the second attempt on the next working day.
- If the second attempt receives no answer, make the third and final attempt two working days later.
- After a third nonresponse, close the opportunity as `Lost / Canceled - No Response`, retain the record and attempt notes, and stop creating active-job reminders.
- For Costco/Centah leads, also follow the already approved current process of canceling the related Centah lead so it remains retained there as inactive.
- Keep this active-request rule separate from the approved long-term prospecting nurture sequence.

### Approval boundary

- This approval covers retry timing and the outcome after three unanswered attempts on an active request.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 4 are complete. Present Decision 5 in plain language: confirm whether the approximately 7:45 a.m. morning-of appointment confirmation remains an intentional exception to the 10:00 a.m. working-hours start.

## Session S-010 - P0-W02 Decision 5 approved and calling hours revised

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 5 explicitly approved

**Approval evidence:** The user clarified that confirmation texts remain at 7:45 a.m. and then directed, “lets do call hours 9am.”

### Accepted decision

- **Accepted (D-037):** Calling hours are Monday through Friday, 9:00 a.m. to 6:00 p.m., and Saturday, 9:00 a.m. to 2:00 p.m.
- New-lead and lead-follow-up calls must not be scheduled before 9:00 a.m.
- A request received outside calling hours is due for its first manual contact attempt at 9:00 a.m. on the next working day.
- Keep approximately 7:45 a.m. as a limited exception for a manual confirmation text for appointments happening that day.
- A confirmation phone call must wait until calling hours begin at 9:00 a.m.
- **Superseded (D-035):** Replace the previously approved 10:00 a.m. start with D-037's 9:00 a.m. calling-hours start.

### Approval boundary

- This approval covers calling hours and the existing morning-of appointment-confirmation rule.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 5 are complete. Present Decision 6 in plain language: decide the quote-preparation deadline after an appointment is completed.

## Session S-011 - P0-W02 Decision 6 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 6 explicitly approved

**Approval evidence:** The user specified, “first goal to send quote is by end of working day as appt, same day.”

### Accepted decision

- **Accepted (D-038):** After an appointment is completed and a quote is needed, the primary goal is to finish and manually send the quote by the end of that same working day.
- Move the opportunity to `Preparing Quote` with the same-day closing time as its due time.
- If the quote is not sent by closing time, keep the task visibly overdue until the consultant records a new due date or sends the quote; do not silently clear or reschedule it.

### Approval boundary

- This approval establishes the primary quote target only.
- The default fallback deadline after missing the same-day target remains unapproved.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 6 are complete. Present Decision 7 in plain language: decide the fallback deadline when a quote cannot be sent by the same-day target.

## Session S-012 - P0-W02 Decision 7 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 7 explicitly approved

**Approval evidence:** The user answered “yes” to the proposed next-working-day fallback and delay-reason requirement.

### Accepted decision

- **Accepted (D-039):** If the primary same-day quote target is missed, require a short reason for the delay.
- Set the fallback quote deadline to the end of the next working day.
- Keep the quote visibly overdue until the fallback date is entered.
- If the fallback is also missed, keep the task overdue and require another deliberate due date and reason rather than silently rescheduling it.

### Approval boundary

- This approval covers recovery from a missed same-day quote target.
- Follow-up timing after a quote is sent remains unapproved.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 7 are complete. Present Decision 8 in plain language: decide when the first customer follow-up is due after a quote is sent.

## Session S-013 - P0-W02 Decision 8 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 8 explicitly approved

**Approval evidence:** The user answered “yes” to the proposed first post-quote follow-up timing and handling.

### Accepted decision

- **Accepted (D-040):** When a quote is sent, create the first manual customer follow-up task for two working days later.
- Use the customer's preferred and permitted channel.
- If the customer responds before the reminder is due, cancel the reminder and record the answer and resulting next action or outcome.
- Do not send the follow-up automatically.

### Approval boundary

- This approval covers only the first follow-up after a quote is sent.
- Timing and limits for later unanswered quote follow-ups remain unapproved.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 8 are complete. Present Decision 9 in plain language: decide when the next follow-up is due after an unanswered first post-quote follow-up.

## Session S-014 - P0-W02 Decision 9 approved and quote follow-up revised

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 9 explicitly approved

**Approval evidence:** The user approved the three-working-day follow-up and clarified, “after i send quote i should send follow up immediatgely so they can check their emails and then check back up 3 days later.”

### Accepted decision

- **Accepted (D-041):** Immediately after emailing a quote, send a manual message through the customer's preferred and permitted channel telling them the quote was sent and asking them to check their email.
- Create the next manual decision-follow-up task for three working days later.
- Keep the opportunity at `Quote Sent - Awaiting Decision` until the customer decides or another explicit outcome is recorded.
- If the customer responds before the task is due, cancel the reminder and record the response and resulting next action.
- Do not send either message automatically.
- **Superseded (D-040):** Replace the earlier two-working-day first-follow-up rule with D-041.

### Approval boundary

- This approval covers the immediate quote-sent notice and the next follow-up three working days later.
- The later reminder sequence and stopping rule after no customer decision remain unapproved.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 9 are complete. Present Decision 10 in plain language: decide what reminder follows if the three-working-day post-quote follow-up does not produce a customer decision.

## Session S-015 - P0-W02 Decision 10 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 10 explicitly approved

**Approval evidence:** The user answered “yes” to the proposed one-week follow-up after an unanswered three-working-day quote follow-up.

### Accepted decision

- **Accepted (D-042):** If the three-working-day post-quote follow-up receives no response, create another manual follow-up for one week later.
- Schedule the contact during normal calling hours.
- Keep the opportunity at `Quote Sent - Awaiting Decision` until the customer decides or another explicit outcome is recorded.
- Do not send the follow-up automatically.

### Approval boundary

- This approval covers the next follow-up interval only.
- The number of later weekly follow-ups and the closure rule for an unresponsive quote remain unapproved.
- Later stage-specific next-action rules and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 10 are complete. Present Decision 11 in plain language: decide how long weekly quote follow-ups continue and what closes an unresponsive quote.

## Session S-016 - P0-W02 Decision 11 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 11 explicitly approved

**Approval evidence:** The user answered “si” to the proposed three-week quote-follow-up limit and `No Decision` outcome.

### Accepted decision

- **Accepted (D-043):** After the three-working-day decision follow-up receives no response, follow up manually once a week for up to three weeks.
- If the customer still does not respond after the third weekly follow-up, close the opportunity as `Lost / Canceled - No Decision`.
- Retain the quote and communication history and stop active reminders.
- If the customer asks for more time, use the date they request instead of continuing the weekly schedule.
- Do not send any follow-up automatically.

### Approval boundary

- This approval completes the normal unanswered-quote follow-up sequence and stopping rule.
- Accepted-sale handoff timing, later post-sale rules, and the minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 11 are complete. Present Decision 12 in plain language: decide the deadline for the source-specific paperwork and internal handoff after the customer accepts.

## Session S-017 - P0-W02 Decision 12 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 12 explicitly approved

**Approval evidence:** The user answered “yasss queen” to the proposed accepted-sale handoff deadline and source-specific checklist.

### Accepted decision

- **Accepted (D-044):** Complete the required accepted-sale handoff by the end of the same working day.
- If the customer accepts outside calling hours, complete the handoff by 9:00 a.m. on the next working day.
- For Costco/Centah work, send DocuSign and email the quote to the internal order coordinator; both are required.
- For independent work, skip DocuSign and email the quote to the internal order coordinator.
- Move to `Handoff Complete - Installation Pending` only after all source-required items have actually been sent.

### Approval boundary

- This approval covers the accepted-sale handoff deadline and completion rule.
- Installation tracking, post-install closure, and the minimum CRM field set remain unapproved within P0-W02.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 12 are complete. Present Decision 13 in plain language: confirm the installation-check tasks, deferral, three-month exception, and transition into post-install follow-up.

## Session S-018 - P0-W02 Decision 13 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 13 explicitly approved

**Approval evidence:** The user answered “fuck ya bruh” to the proposed installation-check, deferral, exception, and human-verification rules.

### Accepted decision

- **Accepted (D-045):** After handoff, create the first installation check for six weeks after DocuSign was sent on Costco/Centah work or six weeks after the coordinator email on independent work.
- If installation is not confirmed, add a note and schedule another check in two to three weeks.
- At three months after the sold quote was emailed to the internal order coordinator, stop routine deferral and show an urgent overdue-installation exception.
- Create a same-day task to contact the coordinator, record the result, and contact the customer if the coordinator cannot confirm installation.
- Never mark installation complete without human confirmation.
- After confirmation, move to `Installed - Customer Follow-Up Due`.

### Approval boundary

- This approval covers installation tracking through the three-month exception and the transition after confirmed installation.
- The post-install customer follow-up timing, final closure rule, and minimum CRM field set remain unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 13 are complete. Present Decision 14 in plain language: decide the post-install customer follow-up timing, recorded result, and transition to `Finished`.

## Session S-019 - P0-W02 Decision 14 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 14 explicitly approved

**Approval evidence:** The user answered “yesss sis” to the proposed post-install customer follow-up and closure rule.

### Accepted decision

- **Accepted (D-046):** After installation is confirmed, create one manual customer follow-up due by the end of the next working day.
- Record the customer's result.
- If everything is satisfactory, move the opportunity to `Finished` and schedule the approved six-month past-customer reminder.
- If the customer reports a problem, do not mark the opportunity finished; flag the unresolved problem and require a next action.
- Keep detailed repair-case management outside the initial CRM scope.

### Approval boundary

- This approval covers satisfactory and problem-reported outcomes from the post-install follow-up.
- The outcome when the customer does not answer the one follow-up attempt remains unapproved.
- The minimum CRM field set remains unapproved.
- CP-003 remains pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 14 are complete. Present Decision 15 in plain language: decide how to close a confirmed-installed job when the customer does not answer the one post-install follow-up attempt.

## Session S-020 - P0-W02 Decision 15 approved

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 pending

**Sign-off status:** Work unit in progress; Decision 15 explicitly approved

**Approval evidence:** The user answered “yasss i love itttt” to the proposed post-install no-response closure rule.

### Accepted decision

- **Accepted (D-047):** If the customer does not answer the one post-install follow-up on a confirmed-installed job, record `Post-Install Follow-Up Attempted - No Response`.
- Mark the opportunity `Finished` and stop post-install reminders.
- Schedule the six-month past-customer reminder only if the customer has not opted out and there is no known unresolved problem.
- Preserve the follow-up result and job history.

### Approval boundary

- This approval completes the normal post-install closure outcomes.
- The minimum CRM field set remains unapproved.
- The sanitized end-to-end validation and CP-003 sign-off remain pending.

### Files changed

- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Decisions 1 through 15 are complete. Present Decision 16 in plain language: approve or revise the minimum information stored on customer, opportunity, and task/activity records.

## Session S-021 - P0-W02 Decision 16 approved and CP-003 prepared

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003 awaiting sign-off

**Sign-off status:** Decision 16 approved; checkpoint packet prepared but not signed off

**Approval evidence:** The user answered “clock it biotch” to the proposed minimum customer, job, and task/activity field set.

### Accepted decision

- **Accepted (D-048):** Use the minimum field set consolidated in `deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`.
- Store the Centah lead number only on Costco/Centah jobs, where it is required and unique; prohibit it on independent jobs.
- Keep detailed quote-file storage deferred while requiring the quoted amount and quote-sent date.
- Require next action and due date on every active prospect and job unless an approved exception is recorded.

### Validation

- Consolidated the sixteen approved P0-W02 decisions into one checkpoint artifact.
- Walked a sanitized independent prospect from capture through conversion, handoff, installation, closure, and eligible past-customer reminder.
- Walked a sanitized Costco/Centah job through its required identifier, DocuSign-plus-email handoff, source-specific installation anchor, three-month exception, and post-install outcome.
- Confirmed that every active stage has a dated next action or an explicit exception.
- Confirmed that the Centah lead number is required and unique only for Costco/Centah jobs.
- Confirmed that all examples use synthetic identifiers, `.invalid` email addresses, and no real customer data.
- Confirmed that no CRM account, external integration, automated communication, or production-data action occurred.

### Files changed

- `deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the CP-003 checkpoint packet. CP-003 remains unsigned until the user explicitly signs it off.

## Session S-022 - P0-W02 signed off at CP-003

**Date:** July 29, 2026

**Phase:** Phase 0

**Work unit:** P0-W02 - Target lifecycle, next-action rules, and minimum CRM fields

**Checkpoint:** CP-003

**Sign-off status:** Signed off July 29, 2026

**Approval evidence:** The user explicitly said, “Sign off CP-003.”

### Approved result

- Approved `deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md` as the connected prospecting and active-job lifecycle specification.
- Approved the stage-specific next-action rules, calling and communication timing, quote sequence, source-specific handoff, installation exception, post-install outcomes, and minimum CRM field set.
- Approved the sanitized independent and Costco/Centah validation walkthroughs.
- Confirmed that every active prospect and job requires a dated next action or an approved exception.
- Confirmed that the Centah lead number is required and unique only for Costco/Centah jobs and prohibited for independent jobs.

### Validation

- All seven P0-W02 acceptance checks passed.
- Markdown table structure, required-stage coverage, synthetic path coverage, and checkpoint-status consistency passed.
- Privacy scans found no real customer records, personal contact patterns, credentials, or private integration payloads.
- No CRM account was created, no integration was connected, no communication was sent, and no production data was used.

### Deferred or unresolved

- Production CRM tenant administration, security, retention, and export controls.
- Centah API/export/sandbox details and Costco program restrictions.
- Final platform selection and whether a Centah adapter is justified.
- Detailed quote-file storage, personal Google connection, and communications-compliance review.

### Files changed

- `deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

CP-003 is complete. P0-W03 is ready to define mandatory platform gates, weighted scorecard criteria, evidence rules, and common synthetic mobile test scenarios before any CRM account is created.

## Session S-023 - GitHub collaborator handoff clarified

**Date:** July 29, 2026

**Phase:** Project infrastructure

**Work unit:** Collaborator onboarding and durable handoff

**Checkpoint:** No new product checkpoint

**Sign-off status:** Operational save requested by the user; CP-003 remains the last product approval

### Completed

- Confirmed that CP-003 was already signed, committed, and pushed before this operational clarification.
- Corrected the stale current-position summary in `README.md` from CP-002/P0-W02 to CP-003/P0-W03.
- Added explicit instructions for another GitHub collaborator to clone or open the repository, start a new Codex task, read `AGENTS.md`, and resume from `CURRENT_STATE.md`.
- Clarified that the repository transfers durable project context, not the original Codex or ChatGPT transcript, personal memories, credentials, connected apps, or uncommitted changes.
- Recommended separate branches or worktrees for concurrent collaboration.

### Files changed

- `README.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

The GitHub repository is ready to serve as the handoff packet for a new collaborator. P0-W03 remains ready to begin with mandatory platform pass/fail requirements.

## Session S-024 - Shared Project mobile collaboration packet added

**Date:** July 30, 2026

**Phase:** Project infrastructure

**Work unit:** Collaborator onboarding and asynchronous guided input

**Checkpoint:** No new product checkpoint

**Sign-off status:** Operational setup requested by the user; CP-003 remains the last product approval

### Completed

- Added `COLLABORATOR_PACKET.md` as the mobile-ready setup and handoff guide for a shared ChatGPT Project.
- Added copy-ready Project instructions and a launch prompt that enforce one-question-at-a-time intake, `unknown` as a valid answer, explicit approval boundaries, and synthetic-only content.
- Added twelve P0-W03 operational questions covering essential phone actions, unacceptable friction, daily queues, prospect capture, reminders, Costco/Centah clarity, appointment and quote context, installation exceptions, weak connectivity, maintenance burden, access, and final must-have requirements.
- Added a structured collaborator handoff format and repository reconciliation checklist.
- Linked the packet from `README.md` and registered it in the project-control files.

### Approval boundary

- The packet changes the collaboration process only; it does not approve any P0-W03 platform requirement, score, weight, account, integration, or vendor selection.
- Answers collected through the shared Project remain unapproved input until reconciled through the guided workflow and explicitly signed off.
- CP-003 remains the last signed-off checkpoint, and P0-W03 remains ready to begin with mandatory pass/fail requirements.

### Files changed

- `README.md`
- `project-control/COLLABORATOR_PACKET.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Create and share the cloud ChatGPT Project using `COLLABORATOR_PACKET.md`, then begin the collaborator's mobile intake at LQ-001. Reconcile the resulting handoff before drafting or approving the P0-W03 mandatory platform requirements.

## Session S-025 - P0-W03 collaborator input reconciled and mandatory gates approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Mandatory gates M-01 through M-13 explicitly approved; work unit remains unapproved

**Approval evidence:** The user approved each proposed mandatory gate individually in the guided sequence.

### Reconciled operational input

- Preserved the collaborator's simplified mobile answers by subject rather than forcing the post-LQ-003 answers into mismatched repository question IDs.
- Confirmed the daily mobile priorities, one-minute friction threshold, combined morning action view, phone-number and last-name search, name-and-phone quick prospect capture, office-based meeting administration, common missed-work risks, and profitability as the desired later business outcome.
- Confirmed Loryn as primary administrator and daily user, with one secondary administrator providing occasional setup, troubleshooting, recovery, and other ad hoc administration.
- Found no conflict with CP-003 or the signed source-specific, next-action, communication, privacy, or CRM-first boundaries.

### Accepted decisions

- **Accepted (D-049 / M-01):** Require one reliable daily action center covering today's appointments, contacts due, overdue work, jobs waiting on others, and active records missing a next action or due date.
- **Accepted (D-050 / M-02):** Require correct Costco/Centah versus independent identification, fields, handoff actions, and installation anchors.
- **Accepted (D-051 / M-03):** Require each essential parked mobile task to be completable in about one minute or less while already signed in.
- **Accepted (D-052 / M-04):** Require reliable reminders for uncontacted clients, quotes, quote follow-up, incomplete handoffs, installation work, and missing next actions while keeping customer communications manual.
- **Accepted (D-053 / M-05):** Require an acceptable production tier with two administrators, multifactor authentication, prompt access removal, permissions, and preserved important activity history.
- **Accepted (D-054 / M-06):** Require usable relationship-preserving exports and documented retention, deletion, and subscription-exit controls; exact retention periods remain open under D-013.
- **Accepted (D-055 / M-07):** Require the approved CP-003 record and lifecycle model through CRM configuration without custom application development merely to pass.
- **Accepted (D-056 / M-08):** Require human-controlled communications, permission and opt-out records, and separation of internal reminders from automatic sends.
- **Accepted (D-057 / M-09):** Require a safe manual Centah bridge while API, webhook, and automated synchronization details remain unverified under D-012.
- **Accepted (D-058 / M-10):** Reject silent loss or duplication and require visible save, failure, retry, and cross-device behavior; full offline support remains weighted.
- **Accepted (D-059 / M-11):** Require documented production cost, tier dependencies, limits, upgrade triggers, and material uncertainties before a candidate may pass.
- **Accepted (D-060 / M-12):** Require learnable daily tasks and sustainable administration using the approved guided-session and fifteen-minute weekly thresholds.
- **Accepted (D-061 / M-13):** Require the same synthetic scenarios and recorded evidence standard for Zoho, HubSpot, and the Centah-only baseline.

### Approval boundary

- This approval covers the P0-W03 mandatory gates only.
- Weighted categories, weights, scoring definitions, synthetic scenarios, evidence records, platform scores, account creation, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Mandatory gates M-01 through M-13 are approved for the P0-W03 draft. Next define and approve weighted preference categories and weights totaling 100 before defining scores or synthetic scenarios.

## Session S-026 - P0-W03 weighted categories approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Weighted categories and weights explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “approve” to the recommended category weights.

### Accepted decision

- **Accepted (D-062):** Use category weights totaling 100: mobile daily-work usability 35, workflow visibility and configuration 20, governance/security/administration 15, data portability and reliability 10, cost and maintenance burden 10, and Centah/integration fit 10.
- Mandatory gates remain separate and override the weighted total; a platform with an applicable `Fail` or `Unverified` gate cannot be preferred from its score.

### Approval boundary

- This approval covers the six category weights only.
- The scoring scale, criterion-level allocation, synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the common scoring scale and weighted-score calculation rule before allocating category weights across specific scored criteria.

## Session S-027 - P0-W03 scoring scale and calculation approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Scoring scale and calculation explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “yes” to the proposed scoring scale and calculation rule.

### Accepted decision

- **Accepted (D-063):** Score each weighted criterion from 0 to 5, where 0 means the criterion cannot be performed, 3 meets normal operational needs, and 5 provides a clear practical advantage.
- Calculate each contribution as `criterion weight × score ÷ 5` and sum the contributions for a maximum of 100.
- Evaluate mandatory gates separately before interpreting points.
- Require evidence and a confidence label for every score; leave a candidate's total incomplete and do not normalize it when evidence is missing.
- Apply the same scale and weights to Zoho, HubSpot, and the Centah-only baseline.

### Approval boundary

- This approval covers the scoring scale and calculation only.
- Criterion-level allocation, synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Allocate the approved category weights across specific scored criteria, beginning with the 35-point mobile daily-work usability category.

## Session S-028 - P0-W03 mobile criterion allocation approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Mobile category criteria and weights explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “approved” to the recommended 35-point mobile allocation.

### Accepted decision

- **Accepted (D-064):** Allocate mobile daily-work usability as daily action-center clarity and usefulness 10, essential mobile-task efficiency 10, customer and job search quality 5, appointment confirmation and directions workflow 5, and mobile note capture and weak-signal behavior 5.
- Related mandatory gates remain prerequisites; these points compare performance beyond the minimum pass threshold.

### Approval boundary

- This approval covers the 35-point mobile criterion allocation only.
- The other five category allocations, synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Allocate the 20 workflow visibility and configuration points across specific scored criteria.

## Session S-029 - P0-W03 workflow criterion allocation approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Workflow category criteria and weights explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “yes” to the recommended 20-point workflow allocation.

### Accepted decision

- **Accepted (D-065):** Allocate five points each to lifecycle/record configuration, next-action/reminder/overdue visibility, source-specific handoff/installation-exception clarity, and office workflow/activity history/practical reporting.
- Related mandatory gates remain prerequisites; these points compare performance beyond the minimum pass threshold.

### Approval boundary

- This approval covers the 20-point workflow criterion allocation only.
- The other four category allocations, synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Allocate the 15 governance, security, and administration points across specific scored criteria.

## Session S-030 - P0-W03 right-sized governance allocation approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Governance category criteria, weights, and proportionality rule explicitly approved; work unit remains unapproved

**Approval evidence:** The user approved the recommended 15-point allocation while noting that some controls felt too detailed for a one-person operation.

### Accepted decision

- **Accepted (D-066):** Allocate governance, security, and administration as secure sign-in/MFA/recovery 4, administrator usability/permissions/access removal 4, activity history/auditability/accountability 4, and retention/deletion/governance documentation 3.
- Apply a proportionality rule: evaluate practical controls for Loryn's one-person operation with occasional secondary-admin help, and do not award extra points for unused enterprise complexity.

### Approval boundary

- This approval covers the 15-point governance allocation and its proportionality rule only.
- The other three category allocations, synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Allocate the 10 data portability and reliability points across specific scored criteria.

## Session S-031 - P0-W03 portability and reliability allocation approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Data portability and reliability criteria and weights explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “yes” to the recommended 10-point portability and reliability allocation.

### Accepted decision

- **Accepted (D-067):** Allocate data portability and reliability as usable export of important data 4, understandable customer-to-job relationships after export 3, and reliable saving/synchronization/retry/recovery 3.
- Related mandatory gates remain prerequisites; these points compare performance beyond the minimum pass threshold.

### Approval boundary

- This approval covers the 10-point portability and reliability allocation only.
- The cost and integration allocations, synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Allocate the 10 cost and maintenance burden points across specific scored criteria.

## Session S-032 - P0-W03 cost and maintenance allocation approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Cost and maintenance criteria and weights explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “yes” to the recommended 10-point cost and maintenance allocation.

### Accepted decision

- **Accepted (D-068):** Allocate cost and maintenance burden as actual recurring cost for two administrators and required features 5, ongoing training/cleanup/support effort 3, and pricing clarity/forced-upgrade risk 2.
- Compare the required production operating cost rather than relying on a free prototype label.

### Approval boundary

- This approval covers the 10-point cost and maintenance allocation only.
- The Centah/integration allocation, synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Allocate the 10 Centah and integration-fit points across specific scored criteria.

## Session S-033 - P0-W03 Centah allocation and complete criterion set approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Centah/integration criteria and all criterion-level weights explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “approved” to the recommended final 10-point category allocation.

### Accepted decision

- **Accepted (D-069):** Allocate Centah and integration fit as practical Costco/Centah job and lead-number handling 4, duplicate checking and reconciliation 3, and evidence-backed future import/export/API options 3.
- Keep unknown Centah capabilities unverified instead of awarding assumed points.
- All six categories are now allocated across specific criteria totaling 100.

### Approval boundary

- This approval completes the criterion-level 100-point scorecard allocation.
- Synthetic scenarios, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the common synthetic fixture set and mobile scenario scripts.

## Session S-034 - P0-W03 synthetic scenario areas approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Seven common synthetic scenario areas explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “yes” to the recommended seven scenario areas.

### Accepted decision

- **Accepted (D-070):** Use TS-01 quick prospect capture, TS-02 morning action center, TS-03 Costco/Centah lead handling, TS-04 appointment workflow, TS-05 visit and quote follow-up, TS-06 both accepted-sale handoff branches, and TS-07 the three-month installation exception.
- Use the same fictional records, starting conditions, and task sequence for Zoho, HubSpot, and the Centah-only baseline.

### Approval boundary

- This approval covers the seven scenario areas only.
- Exact fixtures, starting states, step-by-step scripts, timing rules, expected results, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the exact synthetic fixture set, starting states, scenario steps, timing rules, and expected results for TS-01 through TS-07.

## Session S-035 - P0-W03 synthetic fixture set approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Eight-fixture synthetic dataset explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “yes” to the recommended fixture set.

### Accepted decision

- **Accepted (D-071):** Use eight fixed synthetic fixtures covering new prospect capture, today's appointment, Costco/Centah identification and duplicate review, quote follow-up, both accepted-sale handoff branches, the three-month installation exception, and an intentional missing-next-action negative test.
- Use relative T0 dates, clearly fictional names and identifiers, reserved 555 phone numbers, `.invalid` email addresses, and a plainly synthetic address.
- Reset fixtures to the approved starting state before each candidate test.

### Approval boundary

- This approval covers the synthetic fixture set and starting states only.
- Exact script steps, timing rules, expected results, evidence records, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the exact steps, timing rules, and expected results for TS-01 through TS-07 using the approved fixtures.

## Session S-036 - P0-W03 exact scenario scripts approved

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Common execution rules and exact TS-01 through TS-07 scripts explicitly approved; work unit remains unapproved

**Approval evidence:** The user answered “yes” to the proposed common rules, steps, timing boundaries, and expected results.

### Accepted decision

- **Accepted (D-072):** Reset the same fixtures, use the same phone and order, time actions while already signed in, record friction and uncertainty, and enforce no-send, no-travel, and no-external-connection controls.
- Run the exact approved steps and expected-results checks for quick capture, daily queue, Costco handling, appointment work, quote follow-up, both handoff branches, and the installation exception.
- Leave missing or incomparable evidence `Unverified`; do not invent or normalize a result.

### Approval boundary

- This approval covers the exact scenario scripts and common execution rules only.
- The evidence-record format, completed acceptance review, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the evidence-record format used for every mandatory gate, scored criterion, and scenario result.

## Session S-037 - P0-W03 participant testing burden limited

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** P0-W03 checkpoint pending

**Sign-off status:** Staged testing and Loryn's participant-burden cap explicitly approved; work unit remains unapproved

**Approval evidence:** The user approved the recommendation after asking not to inundate Loryn with tests or follow-up tasks.

### Accepted decision

- **Accepted (D-073):** The evaluator screens all three candidates first and stops nonviable candidates after a confirmed mandatory failure unless a short check is needed to document the result.
- Loryn tests no more than two viable finalists in one guided session of about 20 minutes per finalist.
- Her guided session combines the morning action center, customer search, appointment confirmation, directions, note capture, and quote-follow-up experience.
- The evaluator prepares fixtures, guides the session, records evidence, and completes all technical and administrative checks. Loryn receives no homework or follow-up test tasks.

### Approval boundary

- This approval changes test staging and participant burden, not the seven required areas of evaluation coverage.
- The evidence-record format, completed acceptance review, platform scores, trial accounts, external connections, and platform selection remain unapproved.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the evidence-record format used by the evaluator for every mandatory gate, scored criterion, and scenario result while preserving Loryn's approved burden cap.

## Session S-038 - P0-W03 evidence format approved and CP-004 prepared

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** CP-004 awaiting sign-off

**Sign-off status:** Evidence format approved and checkpoint packet prepared; CP-004 remains unsigned

**Approval evidence:** The user answered “yes” to the evaluator-only compact evidence format.

### Accepted decision

- **Accepted (D-074):** Record candidate/tier/device details once per run and use one compact evaluator-completed row per gate or criterion containing result or score, time or friction, evidence reference, limitation or uncertainty, and confidence.
- Loryn performs no evidence-recording work.
- Low-confidence totals remain provisional, and `Unverified` results receive no score.

### Validation

- Mandatory gates remain separate from weighted preferences.
- Six categories and twenty-two criteria total 100.
- All three candidates use the same gates, scale, fixtures, scripts, and evidence standard.
- TS-01 through TS-07 cover every required P0-W03 scenario area.
- Evidence records require observed results, confidence, uncertainty, and tier or tenant limitations.
- Synthetic-only, no-send, no-travel, no-external-connection, and participant-burden boundaries are explicit.
- Loryn is limited to no more than two guided finalist sessions of about 20 minutes each and receives no homework.

### Approval boundary

- The P0-W03 artifact is complete but remains unapproved until explicit CP-004 sign-off.
- CP-004 would approve the evaluation method only; it would not approve platform scores, account creation, external connections, real data, customer communication, or final platform selection.
- CP-003 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the CP-004 checkpoint packet and request explicit sign-off on the complete P0-W03 evaluation method.

## Session S-039 - P0-W03 signed off at CP-004

**Date:** July 30, 2026

**Phase:** Phase 0

**Work unit:** P0-W03 - CRM platform scorecard and synthetic mobile test scenarios

**Checkpoint:** CP-004

**Sign-off status:** Signed off July 30, 2026

**Approval evidence:** The user explicitly said, “sign off cp-004”.

### Approved result

- Approved `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md` as the common CRM platform-evaluation method.
- Approved mandatory gates M-01 through M-13, the twenty-two weighted criteria totaling 100, and the common 0-5 scoring calculation.
- Approved TS-01 through TS-07, the eight synthetic fixtures, exact execution steps, timing boundaries, expected results, and no-send/no-travel/no-external-connection controls.
- Approved the compact evaluator-only evidence format and the rule that missing evidence remains `Unverified` and is never normalized away.
- Approved evaluator screening before Loryn tests no more than two viable finalists in one guided session of about 20 minutes per finalist, with no homework.

### Validation

- All P0-W03 acceptance checks passed.
- Thirteen mandatory gates, six categories, twenty-two criteria totaling 100, seven scenario scripts, and eight fixtures passed structural and arithmetic checks.
- Decision IDs D-001 through D-074 and session IDs S-001 through S-039 are sequential and unique.
- Markdown tables and Git diff checks passed.
- Privacy checks found only clearly synthetic identities, reserved 555 phone numbers, `.invalid` email addresses, and no credentials or private payloads.

### Approval boundary

- CP-004 approves the evaluation method only.
- It does not authorize a CRM account, external connection, real-data use, customer communication, platform score, purchase, production tenant, or final platform selection.
- Phase 1 requires a separate work-unit contract and explicit authorization before any account action.

### Files changed

- `deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Phase 0 is complete at CP-004. Define and review the first Phase 1 work-unit contract before creating any CRM trial account or beginning platform testing.

## Session S-040 - P1-W01 account ownership rule approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Account ownership rule explicitly approved; work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed account ownership and administration rule.

### Accepted decision

- **Accepted (D-075):** Loryn will own the Zoho account and remain its primary administrator.
- The technical partner will be invited as secondary administrator for approved setup, troubleshooting, recovery support, and ad hoc administration.
- Account recovery information remains under Loryn's control.
- Passwords, recovery codes, MFA secrets, and other credentials are prohibited from Codex and repository artifacts.

### Approval boundary

- This approval covers ownership and administration only.
- The P1-W01 contract, account creation, configuration, testing, external connections, real-data use, customer communications, purchases, scoring, and selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the P1-W01 prototype configuration scope without creating an account.

## Session S-041 - P1-W01 prototype configuration scope approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Minimum configuration scope explicitly approved; work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed prototype configuration scope.

### Accepted decision

- **Accepted (D-076):** Attempt only the standard customer/prospect/job/task records, CP-003 minimum fields, approved stages and source rules, manual next actions, five practical views, eight synthetic fixtures, and manual communications needed for the CP-004 evaluation.
- Exclude real data, external connections, automatic messages, custom code, purchases, paid upgrades, detailed quote attachments, HubSpot configuration, and final platform scoring.
- Record a Zoho Free limitation instead of expanding scope or purchasing an upgrade.

### Approval boundary

- This approval covers the P1-W01 configuration scope only.
- The complete contract, account creation, configuration execution, testing, integrations, real data, customer communications, purchases, scoring, and selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the eight-fixture entry and reset procedure without creating an account.

## Session S-042 - P1-W01 fixture entry and reset approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Synthetic fixture procedure explicitly approved; work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed fixture-entry and reset procedure.

### Accepted decision

- **Accepted (D-077):** Maintain one repository fixture sheet, preload seven existing-record fixtures, and keep `SYN-PROSPECT-A` absent until TS-01 creates it.
- Reset relative T0 dates, stages, tasks, and the intentional missing-next-action state before each candidate run.
- The evaluator completes all entry and reset work outside Loryn's session.
- Remove only the test-created prospect and duplicate attempt and restore changed synthetic fixtures; do not bulk-delete unrelated records.

### Approval boundary

- This approval covers fixture entry and reset only.
- The complete contract, account creation, configuration execution, testing, integrations, real data, customer communications, purchases, scoring, and selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the evaluator screening sequence and early-stop rule without creating an account.

## Session S-043 - P1-W01 evaluator sequence and stopping rule approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Evaluator sequence and early-stop rule explicitly approved; work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed evaluator sequence and early-stop rule.

### Accepted decision

- **Accepted (D-078):** Screen Zoho through official evidence, configuration viability, synthetic scenarios, evaluator mobile timing, and a result summary.
- Stop after a confirmed mandatory failure with no acceptable production tier or in-scope configuration path.
- Require exact feature and cost evidence before marking a paid-tier possibility `Conditional Pass`; do not purchase or activate it.
- Keep missing evidence `Unverified` and exclude Loryn from P1-W01 testing.

### Approval boundary

- This approval covers evaluator sequencing and stopping only.
- The complete contract, account creation, configuration execution, testing, integrations, real data, customer communications, purchases, scoring, and selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the evidence and screenshot storage boundary without creating an account.

## Session S-044 - P1-W01 evidence storage boundary approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Evidence and screenshot storage boundary explicitly approved; work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed evidence and screenshot-storage boundary.

### Accepted decision

- **Accepted (D-079):** Keep raw trial screenshots in ignored local `.trial-evidence/` and commit only reviewed sanitized evidence under `evidence/P1-W01/zoho/`.
- Exclude credentials, MFA/recovery material, cookies, tokens, account identifiers, billing details, personal notifications, browser context, and unrelated private information.
- Permit committed evidence to show only approved synthetic fixtures and use candidate plus gate, criterion, or scenario IDs in filenames.
- Run privacy and secret scans before every commit and do not externally upload or share P1-W01 trial evidence.

### Approval boundary

- This approval covers evidence storage and sanitization only.
- The complete contract, account creation, configuration execution, testing, integrations, real data, customer communications, purchases, scoring, and selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `.gitignore`
- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve free-tier versus paid-tier handling without creating an account or purchasing anything.

## Session S-045 - P1-W01 free-tier and paid-tier rule approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Free-tier and paid-tier handling explicitly approved; work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed free-tier versus paid-tier rule.

### Accepted decision

- **Accepted (D-080):** Evaluate Zoho Free without billing information, paid trials, upgrades, activation, or purchase.
- Do not count a temporary promotional-trial feature as a Free capability.
- Assign `Conditional Pass` for a paid-tier possibility only with exact official evidence for the tier, feature, current cost, user limit, and relevant restriction.
- Keep Free and paid evidence separate and limit P1-W01 to documenting upgrade options rather than recommending or authorizing a purchase.

### Approval boundary

- This approval covers tier handling only.
- The complete contract, account creation, configuration execution, testing, integrations, real data, customer communications, purchases, scoring, and selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the trial-account creation procedure and exact authorization boundary without creating an account.

## Session S-046 - P1-W01 account procedure and action gates approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Trial-account procedure and two action gates explicitly approved; work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed account-creation and authorization procedure.

### Accepted decision

- **Accepted (D-081):** After contract approval, require the exact instruction `Authorize Loryn to create the Zoho Free trial account` before account creation.
- Loryn creates the account herself using private credentials, recovery, and MFA, with the neutral label `Synthetic Window Workflow Trial`, the normal U.S. region when offered, no employer or customer information, no billing, and no paid trial or upgrade.
- Invite and verify the technical partner as secondary administrator, then stop.
- Require the separate exact instruction `Begin P1-W01 synthetic configuration` before configuring fields, entering fixtures, creating views, or running tests.

### Approval boundary

- This approval covers the procedure and authorization wording only; neither action is currently authorized.
- The complete contract, account creation, configuration execution, testing, integrations, real data, customer communications, purchases, scoring, and selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the P1-W01 acceptance checks and CP-005 effect without creating an account.

## Session S-047 - P1-W01 acceptance checks and CP-005 effect approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 contract pending

**Sign-off status:** Acceptance checks and limited CP-005 effect explicitly approved; whole work-unit contract remains unapproved

**Approval evidence:** The user answered “yes” to the proposed acceptance checks and CP-005 effect.

### Accepted decision

- **Accepted (D-082):** Require official tier, administrator, MFA, export, limit, and cost evidence; verified administrator roles; the minimum configuration or documented limitations; resettable synthetic fixtures; evaluator screening; evidence-backed results; privacy review; and a clear viability outcome before P1-W01 can complete.
- Keep totals incomplete while required evidence is `Unverified`, and assign no P1-W01 testing, setup, reset, evidence capture, or homework to Loryn.
- Limit CP-005 to approval of the completed Zoho evaluator result and configuration inventory.

### Approval boundary

- This approval completes the contract design but does not approve the complete work-unit contract.
- CP-005 will not select a platform or authorize HubSpot setup, Loryn finalist testing, production use, real data, integrations, purchases, customer communications, or automation.
- Account creation and synthetic configuration remain separately gated and unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the complete P1-W01 execution contract for explicit whole-contract approval without creating an account.

## Session S-048 - P1-W01 execution contract approved

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 approved for execution; CP-005 remains pending

**Sign-off status:** Complete execution contract explicitly approved; both account action gates remain closed

**Approval evidence:** The user stated, “Approve the P1-W01 execution contract.”

### Accepted decision

- **Accepted (D-083):** Approve the complete P1-W01 execution contract recorded in `../deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`.
- Preserve the separate exact account-creation and configuration authorization gates.

### Approval boundary

- Contract approval does not authorize account creation, synthetic configuration, or platform testing.
- Account creation requires the exact instruction `Authorize Loryn to create the Zoho Free trial account`.
- Configuration and testing require the later exact instruction `Begin P1-W01 synthetic configuration`.
- Real data, external connections, purchases, customer communications, production use, platform scoring, and platform selection remain unapproved.
- CP-004 remains the last signed-off checkpoint; CP-005 occurs only after the approved P1-W01 acceptance checks pass.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Wait for the exact account-creation authorization. Do not create an account or begin synthetic configuration from contract approval alone.

## Session S-049 - P1-W01 account creation authorized

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 execution in progress; CP-005 remains pending

**Sign-off status:** Account-creation gate explicitly opened for Loryn; configuration gate remains closed

**Approval evidence:** The user stated the required exact instruction, “Authorize Loryn to create the Zoho Free trial account.”

### Accepted decision

- **Accepted (D-084):** Authorize Loryn to create the neutral-label Zoho Free account under the approved trial-account procedure.
- Loryn may use private credentials and recovery, enable MFA, invite and verify the technical partner as secondary administrator, and then stop.
- Report only non-sensitive readiness; never provide credentials, codes, recovery information, private email addresses, or account identifiers to Codex or the repository.

### Approval boundary

- This authorization covers account and administrator setup only.
- It does not authorize fields, fixtures, views, imports, tests, integrations, real data, billing, paid trials, purchases, customer communications, scoring, or platform selection.
- Synthetic configuration and testing still require the exact instruction `Begin P1-W01 synthetic configuration` after account readiness is verified.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Await Loryn's non-sensitive report that the neutral-label Free account, MFA, and both administrator roles are ready. Do not begin configuration or testing.

## Session S-050 - Paused for Loryn account-setup handoff

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 execution paused; CP-005 remains pending

**Sign-off status:** Session closed at the approved account-creation handoff; no new product decision or checkpoint approval

**Closure evidence:** The user asked to end the session and stated that Loryn will complete the process interactively with Codex.

### Handoff state

- The P1-W01 execution contract remains approved.
- D-084 authorizes Loryn to complete only the neutral-label Free account, private MFA/recovery, and two-administrator setup.
- Guide Loryn interactively without requesting or recording credentials, codes, recovery information, private email addresses, or account identifiers.
- Stop after Loryn reports only that the Free account, MFA, and both administrator roles are ready.

### Approval boundary

- Synthetic configuration and testing remain unapproved and require the later exact instruction `Begin P1-W01 synthetic configuration` from the user.
- Fields, fixtures, views, imports, integrations, real data, billing, paid trials, purchases, customer communications, scoring, and platform selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Resume with Loryn's interactive account setup under D-084. Do not begin synthetic configuration or testing.

## Session S-051 - Final-platform CRM boundary clarified

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 execution paused; CP-005 remains pending

**Sign-off status:** Platform-selection boundary explicitly accepted; account-setup handoff and configuration gate are unchanged

**Approval evidence:** The user instructed that Centah is not the desired final system and that CRM candidates must support independent work outside Costco/Centah while allowing integration.

### Accepted decision

- **Accepted (D-085):** Centah is not eligible as the final standalone system.
- Evaluate and select only among CRMs that can manage independent prospects and jobs outside Costco/Centah.
- Require the selected CRM to support an evidence-backed manual bridge, import/export path, API, webhook, or other approved integration approach for Costco/Centah work.
- Retain Centah-only only as the current-state reference baseline and governed Costco-side system.

### Approval boundary

- This clarification does not select Zoho, HubSpot, or another CRM.
- It does not authorize synthetic configuration, another CRM account, real data, external integrations, purchases, customer communications, or production use.
- The approved P1-W01 account-setup handoff remains unchanged, and configuration still requires the exact instruction `Begin P1-W01 synthetic configuration`.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Resume with Loryn's authorized account setup. Evaluate Centah only as a nonselectable baseline and integration constraint.
