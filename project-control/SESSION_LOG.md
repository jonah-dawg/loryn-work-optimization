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

## Session S-052 - Zoho Free, MFA, and organization name confirmed

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 account setup in progress; CP-005 remains pending

**Sign-off status:** Free Edition, MFA, and approved organization name confirmed; secondary-administrator verification remains pending

**Approval evidence:** The user confirmed Free Edition and MFA, then instructed the plan to use the organization name `Hazel Kaine`.

### Accepted decision and operational facts

- **Accepted (D-086):** Use `Hazel Kaine` as the approved trial organization name, replacing only the earlier planned neutral label.
- Confirmed operational fact: Zoho initially placed the account in a 15-day Enterprise promotional trial even though no paid trial was intentionally selected.
- Confirmed operational fact: the account was moved to Free Edition before CRM configuration or test-data entry.
- Confirmed operational fact: Loryn-controlled MFA is enabled.
- Confirmed operational fact: Zoho vendor sample data was loaded during account creation.
- Treat vendor sample records as non-approved synthetic data: do not edit or use them before configuration authorization, and remove them through a verified method or isolate them before evaluator testing.
- Secondary-administrator invitation and verification remain pending.

### Approval boundary

- The organization-name change does not authorize additional employer, Costco, Centah, customer, or production information.
- It does not authorize fields, fixtures, views, imports, integrations, real data, billing, paid trials, purchases, customer communications, scoring, or platform selection.
- Synthetic configuration and testing still require the exact instruction `Begin P1-W01 synthetic configuration` after account readiness is verified.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Invite and verify the technical partner as the secondary administrator, then stop before CRM configuration or testing.

## Session S-053 - Zoho account setup completed

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 account setup complete; CP-005 remains pending

**Sign-off status:** Two-administrator account setup confirmed complete; configuration gate remains closed

**Confirmation evidence:** The user reported, “secondary admin confirmed.”

### Confirmed account state

- `Hazel Kaine` is on Zoho CRM Free Edition.
- Loryn remains the account owner, super administrator, and primary administrator with privately controlled MFA and recovery.
- The technical partner accepted the invitation and is confirmed as the second administrator.
- Zoho vendor sample data remains present but is not an approved fixture set.
- The bounded account-creation procedure is complete.

### Approval boundary

- Do not remove vendor sample data, create fields, enter fixtures, configure views, or run tests until the user gives the exact instruction `Begin P1-W01 synthetic configuration`.
- External integrations, real data, billing, paid trials, purchases, customer communications, scoring, and platform selection remain unapproved.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Wait for the exact synthetic-configuration authorization. Do not modify the Zoho CRM account from readiness alone.

## Session S-054 - P1-W01 synthetic configuration authorized

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 execution in progress; CP-005 remains pending

**Sign-off status:** Synthetic configuration and evaluator testing explicitly authorized within the approved contract

**Approval evidence:** The user stated the required exact instruction, “Begin P1-W01 synthetic configuration.”

### Accepted decision

- **Accepted (D-087):** Open the synthetic-configuration gate for P1-W01.
- Authorize current official-evidence preflight, verified vendor-sample cleanup, approved minimum configuration, fixture entry/reset, evaluator testing, mobile timing, and Zoho result preparation.

### Approval boundary

- Use only approved synthetic data and the bounded P1-W01 configuration.
- Do not connect email, calendar, maps accounts, Centah, or any other external service.
- Real data, billing, paid trials, upgrades, purchases, customer communications, production use, CP-005 sign-off, and platform selection remain unapproved.
- Stop if safe cleanup cannot be verified, a mandatory failure is confirmed with no acceptable path, or execution would require scope expansion.
- CP-004 remains the last signed-off checkpoint.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Run the current official-evidence preflight and verify the vendor-sample cleanup method before modifying Zoho.

## Session S-055 - Zoho Free configuration blocker documented

**Date:** July 30, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 - Zoho synthetic prototype and evaluator screening

**Checkpoint:** P1-W01 incomplete; CP-005 remains pending

**Sign-off status:** Execution evidence recorded; no new approval or platform decision

### Work completed

- Verified current official Zoho evidence for Free users, administrators, MFA, custom fields, list views, workflows, import, export, backup, API capacity, and current USD paid-tier pricing.
- Opened the separately authorized configuration gate and used only the signed-in `Hazel Kaine` tenant without requesting or recording credentials, codes, recovery information, private email addresses, or account identifiers.
- Verified Zoho's dedicated sample-removal dialog, confirmed that it targeted sample data only, executed the already approved vendor-only removal, and observed the scheduled cleanup complete.
- Confirmed no `(Sample)` records remained in the checked Leads, Contacts, Accounts, Deals, Tasks, Meetings, or Calls modules.
- Observed two distinct active Administrator rows without retaining private identity details.
- Observed that Zoho Free disables `Create New Module` and every new Deal field type, while exposing only the standard Deal fields.
- Opened the editable Stage-Probability Mapping screen but saved no partial stage model because the supporting CP-003 fields cannot be created on Free.
- Created the sanitized official-evidence preflight, configuration inventory, synthetic fixture sheet, and incomplete evaluator result under `../evidence/P1-W01/zoho/`.

### Findings and blocker

- Zoho Free cannot faithfully represent the CP-003 job baseline and receives confirmed mandatory failures for the applicable source, reminder, record-model, communication-control, and Centah-identifier gates.
- Zoho Standard's documented 10 custom fields per module is also below the approved Deal/job requirement.
- Zoho Professional is the lowest edition with clearly sufficient documented field capacity. Current official USD evidence gives a two-administrator cost of $46 per month on annual billing or $70 month-to-month, before tax.
- The Professional path is only a paid-tier `Conditional Pass` possibility. No trial, billing, upgrade, purchase, or recommendation was authorized or performed.
- Fixtures, scenarios, mobile timing, cross-device reliability, and weighted scoring remain incomplete because the approved baseline cannot be represented on Free.
- **Open (D-088):** choose explicitly whether to keep Zoho as documentation-only, authorize a separately scoped Professional evaluation, or eliminate Zoho and continue the comparison.

### Approval boundary

- CP-004 remains the last signed-off checkpoint; CP-005 is not approved.
- Do not infer authority for a Professional trial, upgrade, purchase, billing action, new candidate account, HubSpot configuration, Loryn testing, real data, integrations, communications, production use, or platform selection.
- The Zoho tenant remains clean of vendor sample data and intentionally contains no partial fixture set.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W01/zoho/configuration-inventory.md`
- `evidence/P1-W01/zoho/evaluator-result.md`
- `evidence/P1-W01/zoho/official-evidence-preflight.md`
- `evidence/P1-W01/zoho/synthetic-fixtures.csv`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Stop at D-088 and request explicit direction. Do not open a paid trial, upgrade, purchase, or start another candidate configuration from the Free blocker alone.

## Session S-056 - D-088 option 1 approved

**Date:** July 31, 2026

**Phase:** Phase 1

**Work unit:** P1-W01 closure and P1-W02 outcome definition

**Checkpoint:** P1-W01 closed incomplete; CP-005 not reached; P1-W02 unapproved

**Sign-off status:** D-088 option 1 explicitly approved; no external account or candidate execution authorized

**Approval evidence:** The user stated, “Approve D-088 option 1.”

### Accepted decision

- **Accepted (D-088 option 1):** Keep Zoho as a documentation-only Professional-tier possibility, do not upgrade or purchase it, close P1-W01 incomplete without CP-005, and proceed only to definition of the next CRM comparison work unit.

### Effect

- Zoho Free remains a confirmed mandatory-field failure; the untested Professional path remains conditional evidence only.
- The `Hazel Kaine` Free tenant remains clean of vendor sample data and intentionally contains no partial fixture set.
- P1-W01 will receive no further fixture entry, scenario testing, mobile timing, or weighted score under the current authority.
- P1-W02 is opened only as an unapproved work-unit outcome and boundary draft in `../deliverables/P1-W02-next-crm-comparison-contract.md`.

### Approval boundary

- CP-004 remains the last signed-off checkpoint. CP-005 was not reached and is not approved.
- This decision does not authorize a HubSpot or other candidate account, account creation, configuration, fixture entry, testing, integration, real data, customer communication, billing, paid trial, purchase, production use, Loryn finalist session, or platform selection.
- The proposed P1-W02 outcome requires a separate explicit approval before detailed contract drafting begins.

### Files changed

- `deliverables/P1-W01-zoho-synthetic-prototype-and-evaluator-screening.md`
- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W01/zoho/configuration-inventory.md`
- `evidence/P1-W01/zoho/evaluator-result.md`
- `evidence/P1-W01/zoho/official-evidence-preflight.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the proposed P1-W02 outcome for explicit approval or revision. Do not create or configure another external account from D-088 option 1 alone.

## Session S-057 - P1-W02 outcome approved

**Date:** July 31, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 - Next CRM comparison contract

**Checkpoint:** CP-004 remains the last signed-off checkpoint; no new checkpoint approved

**Sign-off status:** P1-W02 outcome explicitly approved; detailed contract and external execution remain unapproved

**Approval evidence:** The user stated, “Approve the P1-W02 proposed outcome.”

### Accepted decision

- **Accepted (D-089):** Approve the P1-W02 evidence-first comparison outcome and authorize detailed contract drafting plus current official-evidence research only.

### Effect

- P1-W02 is active in contract design, beginning with the planned HubSpot comparison.
- The lowest plausible production tier will be screened against current official evidence before another account is considered.
- The CP-004 gates, fixtures, scenarios, evidence format, and Loryn burden limit remain the common evaluation method.
- Loryn remains uninvolved until a candidate survives evaluator screening and becomes one of no more than two finalists.

### Approval boundary

- The detailed P1-W02 execution contract and proposed boundaries remain unapproved.
- D-089 does not authorize a HubSpot or other candidate account, trial, configuration, fixture entry, testing, integration, real-data use, communication, billing action, purchase, production use, finalist session, checkpoint sign-off, or platform selection.
- CP-004 remains the last signed-off checkpoint. CP-005 was not reached in P1-W01.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Draft the P1-W02 official-evidence preflight and detailed comparison-contract boundaries, beginning with current official HubSpot tier evidence, then present the next material contract decision. Do not create or configure an external account from D-089.

## Session S-058 - HubSpot preflight and P1-W02 contract draft

**Date:** July 31, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 - Next CRM comparison contract

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-005 was not reached; CP-006 effect is proposed only

**Sign-off status:** No new approval; work performed under D-089 research and drafting authority

### Work completed

- Reviewed current official HubSpot feature, tier, custom-property, required/unique-field, pipeline, view, task, dashboard, mobile, administration, MFA, history, export, deletion, API, cost, and trial evidence.
- Recorded the official-source preflight in `../evidence/P1-W02/hubspot/official-evidence-preflight.md`.
- Drafted the complete P1-W02 candidate/tier boundary, administrator model, minimum configuration, evaluator sequence, stopping rules, account procedure, separate action gates, fixture/evidence handling, acceptance checks, and proposed CP-006 effect.

### Preliminary findings

- HubSpot Free permits only 10 custom properties in total and cannot represent the CP-003 baseline or receive the common fixtures faithfully.
- A Starter-level path remains plausible with 1,000 custom properties per object and a conservative planning cost of $40/month before tax for two Core Seats.
- Starter packaging, exact commitment and renewal terms, and no-billing evaluation access remain unverified because current official pages are not fully consistent.
- The public 14-day trial is Marketing Hub Professional and cannot establish Starter capability.
- M-01 remains a decision-critical risk because multi-source custom reporting is Professional-only; Starter must directly prove a practical single action center or equivalent.

### Approval boundary

- D-089 remains the last approval. The complete P1-W02 execution contract is unapproved.
- No HubSpot account, trial, tier activation, configuration, fixture entry, test, integration, real-data use, communication, billing action, purchase, production use, Loryn finalist session, checkpoint sign-off, or platform selection was authorized or performed.
- Contract approval, if later given, will still leave account creation, qualifying tier activation, and synthetic configuration behind three separate exact instructions.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W02/hubspot/official-evidence-preflight.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the complete P1-W02 execution contract for explicit approval, revision, or rejection. Do not create a HubSpot account from D-089 or from discussion of the draft.

## Session S-059 - Complete P1-W02 execution contract approved

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 - Next CRM comparison contract

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-005 was not reached; CP-006 remains pending execution evidence

**Sign-off status:** Complete P1-W02 execution contract explicitly approved; external action gates remain closed

**Approval evidence:** The user stated, “Approve the complete P1-W02 execution contract.”

### Accepted decision

- **Accepted (D-090):** Approve the complete P1-W02 execution contract, including the candidate and tier boundary, administrator model, minimum configuration, evaluator sequence, stopping rules, separate action gates, fixture and evidence handling, acceptance checks, and CP-006 effect.

### Effect

- The evidence-first HubSpot comparison procedure is approved for execution.
- HubSpot Free remains an account-shell and official-evidence baseline only because its 10-custom-property total cannot represent CP-003 or the common fixtures.
- A Starter-level path remains conditional on exact SKU, two-seat cost, commitment, renewal behavior, no-billing evaluation access, and direct M-01 proof.
- Loryn remains the account owner and primary Super Admin; the technical partner remains the secondary Super Admin for approved ad hoc support.
- Account creation, qualifying tier activation, and synthetic configuration remain behind three separate exact authorization phrases.

### Approval boundary

- D-090 does not authorize a HubSpot or other external account, trial or tier activation, configuration, fixture entry, testing, integration, real-data use, communication, billing action, purchase, production use, Loryn finalist session, checkpoint sign-off, or platform selection.
- CP-004 remains the last signed-off checkpoint. CP-005 was not reached, and CP-006 cannot be signed until the approved HubSpot evaluator result exists.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the separately gated HubSpot Free account-shell decision. Require the exact instruction `Authorize Loryn to create the HubSpot Free evaluation account` before any account is created. Do not activate a trial or tier, enter billing information, connect an external service, or begin configuration from D-090.

## Session S-060 - HubSpot Free account-shell creation authorized

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 - Next CRM comparison contract

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-006 remains pending execution evidence

**Sign-off status:** Bounded HubSpot Free account-shell procedure explicitly authorized; completion not yet confirmed

**Approval evidence:** The user stated, “Authorize Loryn to create the HubSpot Free evaluation account”.

### Accepted decision

- **Accepted (D-091):** Authorize Loryn to create the `Hazel Kaine` HubSpot Free account shell, keep credentials and recovery private, enable MFA, invite the technical partner as secondary Super Admin, inspect only permitted edition and evaluation-offer details, and then stop.

### Authorized procedure

- Loryn creates the account herself using private credentials and recovery under her control.
- Use `Hazel Kaine` as the organization name and select the normal U.S. region if asked.
- Decline imports, connected inboxes, calendars, calling, phone numbers, enrichment, AI agents, and external or credit-consuming setup.
- Enter no billing information, make no purchase, and activate no trial or tier.
- Enable private MFA, invite the technical partner, confirm both Super Admin roles, inspect only the displayed edition and nonprivate offer terms, report the permitted confirmations, and stop before configuration.

### Approval boundary

- D-091 does not authorize trial or tier activation, configuration, fixture entry, testing, integration, real-data use, communication, billing action, purchase, production use, Loryn finalist testing, checkpoint sign-off, or platform selection.
- Credentials, passwords, passkeys, MFA methods or codes, recovery details, private email addresses, account identifiers, session information, and private notifications remain prohibited from project artifacts and chat reporting.
- CP-004 remains the last signed-off checkpoint. CP-006 cannot be signed until an approved HubSpot evaluator result exists.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Guide Loryn through the bounded HubSpot Free account-shell procedure. Stop after she reports the displayed Free edition, private MFA enabled, both Super Admin roles confirmed, and any nonprivate Starter-equivalent evaluation labels and terms. Do not activate a trial or tier, enter billing, connect a service, create CRM fields or records, or begin testing.

## Session S-061 - Synthetic Free MFA exception approved

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 - Next CRM comparison contract

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-006 remains pending execution evidence

**Sign-off status:** Synthetic-Free-only MFA exception explicitly approved; account shell partially confirmed

**Approval evidence:** The user stated, “Revise P1-W02 to make MFA optional during the synthetic Free evaluation.”

### Accepted decision

- **Accepted (D-092):** Make MFA optional only during the synthetic HubSpot Free evaluation, record a deferral as a security limitation, and require MFA before any paid or promotional tier activation, external connection, real-data use, production use, or later security approval.

### Confirmed account-shell facts

- The technical partner created the account as Loryn's proxy and may retain Super Admin control during approved evaluator setup and testing.
- Direct tenant reporting confirms HubSpot Free.
- The organization name is confirmed as `Hazel Kaine`.
- MFA is intentionally deferred under D-092 rather than recorded as enabled or satisfied.
- Loryn's independent Super Admin access and the permitted evaluation-offer inspection remain unconfirmed.

### Approval boundary

- D-092 changes only the MFA requirement during the synthetic HubSpot Free evaluation.
- It does not authorize trial or tier activation, configuration, fixture entry, testing, integration, real-data use, communication, billing action, purchase, production use, Loryn finalist testing, checkpoint sign-off, or platform selection.
- The absence of MFA must remain visible in the security evidence and cannot receive a later production-security pass.
- Credentials, MFA or recovery details, private email addresses, account identifiers, and session information remain prohibited from reporting and project artifacts.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Add Loryn with independent Super Admin access and confirm both administrators without private identifiers. Inspect only nonprivate Starter-equivalent evaluation labels and terms, then stop before tier activation, configuration, fixtures, or testing.

## Session S-062 - Prototype administration moved fully to evaluator

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 - Next CRM comparison contract

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-006 remains pending execution evidence

**Sign-off status:** Technical-partner-only prototype administration explicitly approved; Loryn access deferred

**Approval evidence:** The user stated, “loryns access isn't required for these prototypes, lets just finish the testing so she can get the comparisons to evaluate”.

### Accepted decision

- **Accepted (D-093):** Allow the technical partner to own and control evaluator-only prototype tenants as the sole prototype administrator, defer Loryn's account access until a candidate becomes one of no more than two viable finalists, and require a separate gate before her finalist session.

### Effect

- The HubSpot Free `Hazel Kaine` account shell is complete with the technical partner as the evaluator administrator and MFA intentionally deferred under D-092.
- Loryn receives no prototype account, setup work, configuration work, evidence work, reset work, evaluator testing, or homework.
- Two-administrator and access-removal behavior may remain official-evidence-backed or `Unverified` during evaluator screening, but HubSpot cannot pass M-05 or advance beyond finalist evaluation until the required direct evidence exists.
- If HubSpot becomes a viable finalist, a separate gate will authorize Loryn's limited guided session and appropriate independent access.

### Approval boundary

- D-093 changes prototype ownership and the timing of Loryn's involvement only.
- The user's instruction to finish testing does not bypass the exact tier-activation or synthetic-configuration gates. HubSpot Free remains unable to represent the common fixture baseline.
- Trial or tier activation, configuration, fixture entry, testing, integration, real-data use, communication, billing action, purchase, production use, Loryn finalist testing, checkpoint sign-off, and platform selection remain unapproved.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Inspect only the nonprivate labels and terms of any Starter-equivalent evaluation offer available from the Free tenant, including whether billing or automatic activation is required. Stop before activation, configuration, fixtures, or testing.

## Session S-063 - HubSpot tenant offer inspected; stopping rule reached

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 - Next CRM comparison contract

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-006 remains pending and cannot be signed from the current evidence

**Sign-off status:** No new approval; read-only tenant inspection completed under the D-090 contract and D-091 account-shell authority

### Work completed

- Used the signed-in evaluator tenant to inspect Account & Billing, the Starter upgrade comparison, the one-seat plan configurator, and the checkout terms.
- Recorded the sanitized direct evidence in `../evidence/P1-W02/hubspot/tenant-offer-inspection.md`.
- Exited checkout without entering address or payment information and returned the tenant to the Free plan overview.

### Direct findings

- Account & Billing lists `Free Tools`; no active trial or paid entitlement was displayed.
- The tenant offers `Starter Customer Platform` as a purchase rather than a no-billing evaluation.
- The offer displayed one Core Seat at a limited `$7/mo` promotion against a `$20/mo` base amount.
- Annual billing was selected by default: `$240` base, `$156` annual promotion, and `$84` due immediately before tax.
- A monthly-commit option exists, but its exact immediate total, complete term, renewal price, and tax remain unverified.
- Company address and secure payment details are required to complete checkout.
- No trial path, purchase, tier activation, data entry, external connection, configuration, fixture, test, communication, or production action occurred.

### Stopping-rule result

- HubSpot Free remains unable to represent the approved CP-003 baseline.
- No clean no-billing Starter-equivalent evaluation exists in the inspected tenant.
- P1-W02 execution stops before configuration and synthetic scenario testing.
- HubSpot Starter remains a documentation-backed `Conditional Pass` possibility only; no HubSpot candidate score or platform recommendation exists.

### Approval boundary

- D-093 remains the last approval.
- The inspection does not authorize a trial or tier, paid evaluation, purchase, billing action, configuration, fixture entry, testing, integration, real-data use, communication, production use, Loryn finalist testing, checkpoint sign-off, or platform selection.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W02/hubspot/official-evidence-preflight.md`
- `evidence/P1-W02/hubspot/tenant-offer-inspection.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present three explicit options: retain HubSpot Starter as documentation-only; authorize a separately scoped paid evaluation after exact monthly checkout, renewal, tax, and total-cost review; or close HubSpot incomplete and screen the next CRM candidate. Do not infer approval from discussion.

## Session S-064 - HubSpot closed incomplete; Pipedrive preflight prepared

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W02 closed; P1-W03 proposed

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-005 and CP-006 were not reached

**Sign-off status:** D-094 and D-095 explicitly accepted; complete P1-W03 execution contract remains unapproved

**Approval evidence:** The user answered “let's go with the recommendation, continue” to the recommendation to select P1-W02 stopping-rule option 3, then answered “continue” after the Pipedrive Lite proposed target, tier risk, and no-account boundary were presented.

### Decision recorded

- **Accepted (D-094):** Close P1-W02 incomplete without CP-006, retain HubSpot Starter as documentation-only, and continue to official-evidence screening of the next CRM candidate.
- **Accepted (D-095):** Approve the P1-W03 Pipedrive evidence-first outcome and authorize detailed execution-contract drafting plus additional current official research only.
- D-094 does not authorize a HubSpot purchase, Pipedrive account or trial, configuration, fixture entry, testing, integration, real data, communications, billing, production use, Loryn finalist testing, checkpoint sign-off, or platform selection.
- D-095 preserves the same external-action boundary.

### Work completed

- Closed the P1-W02 contract incomplete and preserved the sanitized HubSpot evidence.
- Reviewed current official Pipedrive pricing, trial, plan-limit, data-model, filter, search, mobile, export, duplicate, and API sources.
- Drafted the P1-W03 proposed outcome in `../deliverables/P1-W03-pipedrive-evidence-first-screening.md`; D-095 subsequently approved that outcome only.
- Recorded the official-source findings in `../evidence/P1-W03/pipedrive/official-evidence-preflight.md`.
- Mapped the CP-003 minimum fields to 22 planned Lite custom fields in `../evidence/P1-W03/pipedrive/field-capacity-preflight.md`.
- Drafted the complete Lite-only execution contract, separate action gates, stopping rules, acceptance checks, and CP-007 effect.

### Preliminary Pipedrive finding

- Pipedrive advertises a 14-day full-access trial with no credit card required.
- Lite is listed at `$14` per seat per month billed annually, or `$168` per seat per year; two paid administrator seats would be `$336` per year before tax if Lite passes.
- Lite allows 30 custom fields per company and includes customizable pipelines, import/export, duplicate merging, and API access.
- The record model supports reusable people with multiple deals and linked activities.
- Official mobile documentation lists Focus, Nearby, pipeline, activity, calendar, contacts, filters, offline mode, audio notes, and notifications on both supported mobile platforms; Nearby can open navigation.
- Search includes person name and phone number.
- Lite is not yet viable: the CP-003 field count, M-01 action center, M-07 exception visibility, trial tier contamination, exact cost terms, administration, mobile speed, save reliability, exports, and Centah bridge remain unverified.
- Hard required-field rules are Premium-only, so Lite must prove visible exception handling instead.
- The documentation field map uses 9 Person and 13 shared Lead/Deal custom fields, leaving eight fields under Lite's limit; activities use standard fields.
- Official import guidance says deals have no native duplicate identifier, so the searchable Centah field and manual duplicate-review procedure must pass M-09 directly.

### Files changed

- `deliverables/P1-W02-next-crm-comparison-contract.md`
- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W03/pipedrive/official-evidence-preflight.md`
- `evidence/P1-W03/pipedrive/field-capacity-preflight.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the complete P1-W03 execution contract for explicit approval. Contract approval would not authorize an account, trial, configuration, testing, billing, purchase, or platform selection.

## Session S-065 - Complete P1-W03 execution contract approved

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W03 - Pipedrive evidence-first screening

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-007 remains pending execution evidence

**Sign-off status:** Complete P1-W03 execution contract explicitly approved as D-096; account creation remains unapproved

**Approval evidence:** The user gave the exact instruction `Approve the complete P1-W03 execution contract`.

### Decision recorded

- **Accepted (D-096):** Approve the complete P1-W03 execution contract, including the Lite-only candidate and tier boundary, technical-partner evaluator ownership, bounded execution sequence, minimum configuration, stopping rules, separate action gates, acceptance checks, and CP-007 effect.

### Approval effect

- P1-W03 may rely on the approved contract for later separately authorized actions.
- CP-007 would approve only a completed Pipedrive evaluator result, configuration inventory, exact tier and cost record, and evidence-backed comparison status.
- D-096 does not authorize account creation, trial activation, configuration, fixture entry, testing, integrations, billing, purchases, real data, customer communications, production use, Loryn participation, checkpoint sign-off, or platform selection.
- Account creation requires the separate exact instruction `Authorize the Pipedrive Lite trial account`.
- Configuration and synthetic testing remain behind the later exact instruction `Begin P1-W03 synthetic configuration`.

### Files changed

- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the separate Pipedrive Lite account-creation gate. Do not create or activate the trial until the explicit authorization is received.

## Session S-066 - Pipedrive evaluator account and trial authorized

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W03 - Pipedrive evidence-first screening

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-007 remains pending execution evidence

**Sign-off status:** Bounded evaluator account and no-credit-card trial explicitly authorized as D-097; setup pending

**Approval evidence:** The user gave the instruction `authorize the pipedrive lite trial account`.

### Decision recorded

- **Accepted (D-097):** Authorize the technical partner to create the bounded `Hazel Kaine` Pipedrive evaluator account and no-credit-card trial, then inspect only nonprivate edition, expiry, and feature-boundary labels before stopping.

### Authorized account procedure

- The technical partner creates and controls the evaluator account using private credentials.
- Use `Hazel Kaine` as the organization name.
- Do not enter billing information, invite Loryn, connect another service, or use real data. If vendor sample data appears, report it and leave it untouched until configuration is separately authorized.
- Keep passwords, MFA methods or codes, recovery details, private email addresses, account identifiers, and session details outside project artifacts and chat.
- After first sign-in, report only nonprivate plan, trial-expiry, and feature-boundary labels, then stop.

### Continuing boundary

- D-097 does not authorize configuration, fixture entry, synthetic testing, integrations, billing, purchases, real data, customer communications, production use, Loryn participation, CP-007 sign-off, or platform selection.
- Configuration and testing still require the exact instruction `Begin P1-W03 synthetic configuration` after the account shell and Lite-equivalent boundary are confirmed.

### Files changed

- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Guide the technical partner through private Pipedrive signup. Stop after the account shell, plan, expiry, and Lite-equivalent feature boundary are confirmed.

## Session S-067 - Pipedrive tenant inspected; Premium stopping boundary reached

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W03 - Pipedrive evidence-first screening

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-007 remains pending execution evidence

**Sign-off status:** No new approval; bounded read-only account-shell and plan inspection completed under D-097

### Work completed

- Confirmed the `Hazel Kaine` evaluator account shell and inspected only the setup surface, Billing overview, and read-only plan comparison.
- Recorded sanitized direct evidence in `../evidence/P1-W03/pipedrive/tenant-shell-inspection.md`.
- Returned to Billing overview without saving a plan change or entering billing information.

### Direct tenant findings

- Billing overview displays a `14-day free trial`, Premium as the current plan, monthly billing, one seat in use, and `$0` during the trial.
- No exact calendar expiration date was displayed.
- Premium includes LeadBooster, Smart Docs, and Projects, confirming higher-tier and add-on contamination.
- Lite appeared in the plan comparison at `$24` per seat per month on monthly billing or `$14` per seat per month billed annually. It was not selected.
- The Lite comparison displayed 2,500 leads and deals per seat, 30 custom fields per company, 15 reports per seat, and 30,000 API tokens per seat, subject to displayed caps.
- The setup surface showed three preloaded activity indicators before evaluator data entry. Their contents and origin were not inspected, and they remain untouched.

### Stopping boundary

- The current Premium trial cannot serve as clean Lite evidence. The approved stopping rule blocks configuration until a separate no-billing Premium-to-Lite switch is explicitly authorized and verified.
- No plan change, billing action, purchase, configuration, record inspection, fixture entry, synthetic test, integration, customer communication, real-data action, invitation, or production action occurred.
- D-097 remains the last approval. CP-007 was not reached, and no platform was scored or selected.

### Files changed

- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W03/pipedrive/official-evidence-preflight.md`
- `evidence/P1-W03/pipedrive/tenant-shell-inspection.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the proposed authorization to switch only the existing no-billing Pipedrive trial from Premium to Lite, then verify the plan and remaining-trial labels. Do not select Lite without explicit approval. If the switch requires billing, a paid commitment, or an unexpected loss of trial access, stop. Configuration and synthetic testing remain separately unapproved.

## Session S-068 - Pipedrive Lite-only trial boundary authorized and verified

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W03 - Pipedrive evidence-first screening

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-007 remains pending execution evidence

**Sign-off status:** No-billing Premium-to-Lite trial transition explicitly approved and completed as D-098; configuration remains unapproved

**Approval evidence:** The user gave the exact instruction `Authorize switching the Pipedrive trial from Premium to Lite with no billing information`.

### Decision recorded

- **Accepted (D-098):** Switch only the existing no-billing Pipedrive trial from Premium to Lite, remove carried-over trial add-ons, verify the resulting plan and remaining-trial labels, and stop before configuration.

### Authorized action completed

- Opened the existing plan-management flow and selected Lite on monthly billing.
- The first order summary retained LeadBooster, Projects, and Smart Docs and showed a `$110` estimated post-trial total. Disabled all three before confirmation.
- Confirmed the plan change only after the summary showed `$24` for one Lite seat and no selected add-ons.
- Returned to Billing overview and verified Lite, one seat, `$24`, `$0` during the trial, no active add-ons, no billing details, and the preserved `14-day free trial` label.
- The former add-ons now appear only as optional trial offers.

### Evidence and boundary

- Updated `../evidence/P1-W03/pipedrive/tenant-shell-inspection.md` with the sanitized before-and-after readback.
- The exact calendar expiration date remains unverified because the tenant displays only the duration label.
- The Activities count changed from three to four during the vendor plan transition. No record was opened or inspected, and all preloaded content remains untouched.
- No configuration, fixture entry, synthetic testing, integration, billing-detail entry, purchase, real-data action, customer communication, invitation, production action, checkpoint sign-off, or platform selection occurred.
- D-098 resolves the Premium-contamination blocker only. CP-007 was not reached, and Pipedrive remains unscored.

### Files changed

- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W03/pipedrive/official-evidence-preflight.md`
- `evidence/P1-W03/pipedrive/tenant-shell-inspection.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the separate `Begin P1-W03 synthetic configuration` gate. Until that exact authorization is received, do not inspect or clean preloaded records, configure the approved model, enter synthetic fixtures, or run tests.

## Session S-069 - Pipedrive synthetic configuration authorized and begun

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W03 - Pipedrive evidence-first screening

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-007 remains pending execution evidence

**Sign-off status:** Synthetic configuration and evaluator testing explicitly authorized as D-099; execution in progress

**Approval evidence:** The user gave the exact instruction `Begin P1-W03 synthetic configuration`.

### Decision recorded

- **Accepted (D-099):** Begin P1-W03 synthetic configuration, including verified vendor-sample cleanup, the approved minimum Lite configuration, synthetic fixture handling, evaluator testing, and result preparation.

### Authorized action completed

- Inspected the preloaded records and verified that the visible activities and linked records were labeled `[Sample]`.
- Used Pipedrive's global-administrator sample-data removal control and verified the successful-removal state.
- Directly confirmed the Lite custom-field limit and configured 25 of 30 fields: 9 Person fields and 16 shared Lead/Deal fields.
- Corrected the documentation map because last-contact date and time require separate fields and standard acquisition metadata does not represent the approved Costco/independent operational source branch.
- Configured the nine-stage `Window Sales Jobs` pipeline, four workflow-specific activity types, six lost reasons, and disabled the conflicting generic post-won three-month task prompt.
- Prepared the seven-record synthetic preload in `../evidence/P1-W03/pipedrive/synthetic-fixtures.csv`; `SYN-PROSPECT-A` remains reserved for TS-01.

### Incomplete execution and boundary

- The fixture file has not yet been loaded. Practical views, TS-01 through TS-07, mobile timing, duplicate review, export, save/recovery evidence, cleanup, and the evaluator result remain incomplete.
- Browser control could list the signed-in Chrome tab but could not take control of it after the upload page reset. Chrome, the extension, and the native connection all passed read-only diagnostics; no fixture file was transmitted.
- No billing detail, purchase, add-on, higher tier, external connection, real data, customer communication, production action, Loryn participation, checkpoint sign-off, or platform selection occurred.
- Mobile-only criteria remain unverified until actually tested and must not be inferred from desktop or responsive-web behavior.

### Files changed

- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W03/pipedrive/configuration-inventory.md`
- `evidence/P1-W03/pipedrive/field-capacity-preflight.md`
- `evidence/P1-W03/pipedrive/synthetic-fixtures.csv`
- `evidence/P1-W03/pipedrive/tenant-shell-inspection.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Resume at the seven-record fixture upload, then create the practical action-center and exception views and execute the directly verifiable desktop scenarios. Keep native-mobile-only items unverified unless actually tested. The external-action boundary remains unchanged.

## Session S-070 - Pipedrive evaluator result prepared at mandatory stopping rule

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W03 - Pipedrive evidence-first screening

**Checkpoint:** CP-004 remains the last signed-off checkpoint; CP-007 is pending explicit review

**Sign-off status:** D-099 evaluator execution completed to the stopping rule; proposed Lite elimination remains unapproved

### Authorized work completed

- Imported the seven-row approved preload as seven People and seven linked Deals. The import added 14 items with no updates, merges, or skips and placed every Deal in `Window Sales Jobs`.
- Added six baseline activities and kept `SYN-QUEUE-H` without an activity for the negative test.
- Created private `Missing Next Action` and `Waiting on Others` Deal filters and verified native Today and Overdue activity states.
- Executed the directly verifiable desktop portions of TS-01 through TS-07 using synthetic data only.
- Verified customer search by synthetic phone number and last name, quote-note/value/date history, overdue visibility, explicit handoff and installation tasks, and installation-exception visibility.
- Generated server-side entity exports. Chrome blocked the vendor-hosted download with `ERR_BLOCKED_BY_CLIENT`, so export contents and relationship reconstruction remain unverified.

### Mandatory stopping result

- TS-03 accepted a second Deal with the existing `SYN-CENTAH-1001` value without blocking it or visibly routing it for duplicate review. The prepared result records M-09 as `Fail`.
- TS-06 showed that Lite exposes the same handoff fields on both sources and cannot conditionally require the approved source-specific set, prevent premature completion, or produce the source-specific installation anchor. The prepared result records M-02 as `Fail`.
- These direct mandatory failures make Pipedrive Lite nonviable under the CP-004 rules. Further mobile, save/recovery, administration, and export testing stopped rather than creating a misleading weighted score.
- `../evidence/P1-W03/pipedrive/evaluator-result.md` proposes `Eliminated`; that outcome is unapproved until CP-007 is explicitly signed.

### Cleanup and retained synthetic state

- Deleted the temporary TS-01 Lead and Person and the duplicate Deal and Person. The active People list returned to the seven baseline synthetic records.
- Pipedrive retains deleted records for 30 days, and the TS-01 activity may remain unlinked.
- Retained the baseline fixtures, scenario activities, synthetic quote note/value, saved filters, and generated server-side exports as evaluation evidence. Reset them before any rerun or tenant closeout.

### Approval boundary

- No checkpoint, platform selection, next candidate, finalist session, billing, purchase, paid commitment, production use, external connection, real data, or customer communication is approved.
- Loryn remains uninvolved in evaluator testing.
- CP-007 would approve only the prepared evaluator result, configuration inventory, tier/cost record, and evidence-backed comparison status.

### Files changed

- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W03/pipedrive/configuration-inventory.md`
- `evidence/P1-W03/pipedrive/evaluator-result.md`
- `evidence/P1-W03/pipedrive/official-evidence-preflight.md`
- `evidence/P1-W03/pipedrive/tenant-shell-inspection.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Review the prepared P1-W03 evaluator result. If the proposed Lite elimination is accepted, explicitly sign CP-007. Do not infer that sign-off, a next-candidate authorization, or a platform selection from this execution record.

## Session S-071 - P1-W03 signed off at CP-007

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W03 - Pipedrive evidence-first screening

**Checkpoint:** CP-007

**Sign-off status:** Signed off August 1, 2026; Pipedrive Lite eliminated

**Approval evidence:** The user explicitly said, `Sign off CP-007.`

### Approved result

- Approved `../evidence/P1-W03/pipedrive/evaluator-result.md`, the linked configuration inventory, the Lite tier/cost record, and the evidence-backed comparison status.
- Approved Pipedrive Lite as `Eliminated` because M-02 source-specific workflow and M-09 safe Centah/Costco bridge fail directly.
- Confirmed that the weighted score remains intentionally incomplete under the approved stopping rule and that the unverified mobile, reliability, export, and administration items do not reverse the two mandatory failures.
- Closed P1-W03 at CP-007.

### Validation

- The evaluator result contains all thirteen mandatory-gate rows and all seven scenario rows.
- The configuration inventory records the 25-field map, seven-person/seven-deal import, practical filters, direct scenario observations, export limitation, and cleanup state.
- Privacy and secret checks found no credentials, private email addresses, account identifiers, real customer data, or private integration payloads.
- Markdown and Git diff checks passed before commit.

### Approval boundary

- CP-007 approves the Pipedrive Lite evaluator result only.
- It does not select another CRM, authorize a next candidate or account, start a Loryn finalist session, permit billing or production use, connect Centah or another service, import real data, or send customer communications.
- Pipedrive Lite can be reopened only through a later explicitly approved work unit.

### Files changed

- `deliverables/P1-W03-pipedrive-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W03/pipedrive/configuration-inventory.md`
- `evidence/P1-W03/pipedrive/evaluator-result.md`
- `evidence/P1-W03/pipedrive/official-evidence-preflight.md`
- `evidence/P1-W03/pipedrive/tenant-shell-inspection.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Define and approve the next Phase 1 CRM comparison work unit using official evidence before authorizing another account, trial, configuration, or external action.

## Session S-072 - P1-W04 Bigin outcome proposed

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W04 - Bigin Premier evidence-first screening

**Checkpoint:** CP-007 remains the last signed-off checkpoint; CP-008 effect is proposed only

**Sign-off status:** Proposed outcome unapproved; no Bigin account or external action authorized

### Orientation

- Current phase: Phase 1 CRM candidate comparison.
- Active work unit: P1-W04 definition and official-evidence preflight.
- Last approval: CP-007, which eliminated Pipedrive Lite only.
- Open blocker: identify a right-sized CRM tier that can enforce source-specific handoffs and opportunity-level Centah duplicate control while preserving mobile usability and reasonable cost.
- Proposed outcome: evaluate Bigin Premier through a separately approved evidence-first contract and no-credit-card trial.

### Work completed

- Reviewed current official Bigin pricing, edition limits, Team Pipelines, custom and unique fields, Stage Transition Rules, workflows, mobile dashboards/calendar/contacts, user management, export, backup, and API positioning.
- Confirmed Premier at `$15` per user monthly or `$12` per user per month billed annually; two administrators therefore baseline at `$30` monthly or `$288` annually before applicable tax or add-ons.
- Confirmed the no-credit-card 15-day trial does not autocharge and falls back to the one-user Free plan.
- Identified Premier as the lowest plausible tier: Express has 10 custom fields per module, while Premier has 25 plus Stage Transition Rules, five Team Pipelines, advanced date automation, and duplicate cleanup.
- Compared Freshsales Pro as the strongest documentation-only fallback. Its unique fields, field dependencies, and mobile offline behavior are promising, but the current annual-billing price is `$39` per user per month and is less proportionate to the one-person operation.
- Drafted `../deliverables/P1-W04-bigin-evidence-first-screening.md` and recorded the official evidence in `../evidence/P1-W04/bigin/official-evidence-preflight.md`.

### Decision-critical uncertainties

- Complete CP-003 field mapping within Premier's 25-field-per-module limits.
- Separate Team Pipelines versus sub-pipelines for Costco/Centah and Independent work without fragmenting the morning action center or reusable customer history.
- Direct stage-transition, unique-field, duplicate-import, date-anchor, mobile, search, directions, save/retry, export-relationship, administration, MFA, retention, API-limit, and exact cost behavior.
- Exact trial edition and isolation from any Bigin 360-only capability.

### Approval boundary

- No decision number is assigned because the proposed outcome is unapproved.
- No account, trial, tenant inspection, configuration, fixture entry, test, billing detail, purchase, external connection, real data, customer communication, production use, Loryn participation, checkpoint, or platform selection is authorized.
- Explicit outcome approval would authorize detailed contract drafting, the field-capacity map, and further current official research only.

### Files changed

- `deliverables/P1-W04-bigin-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W04/bigin/official-evidence-preflight.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`
- `project-control/ARTIFACT_REGISTER.md`

### Saved ending point

Present the P1-W04 proposed outcome for explicit approval. Do not draft the execution contract or field map until the outcome is approved, and do not create a Bigin account without a later separate authorization.

## Session S-073 - P1-W04 outcome approved and contract proposed

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W04 - Bigin Premier evidence-first screening

**Checkpoint:** CP-007 remains the last signed-off checkpoint

**Sign-off status:** Outcome approved as D-100; proposed complete execution contract unapproved; no Bigin account or external action authorized

### Orientation

- Current phase: Phase 1 CRM candidate comparison.
- Active work unit: P1-W04 Bigin Premier evidence-first screening.
- Last signed checkpoint: CP-007, which eliminated Pipedrive Lite only.
- Open blockers: complete contract approval, exact trial edition, Premier isolation, source-specific transition-rule behavior, unique Centah handling, unified action-center behavior, task timestamps, mobile behavior, administration, portability, and exact production cost.
- Proposed outcome: bounded Premier-only evaluator screening with separate contract, account, edition-change, configuration, paid-action, external-connection, finalist, checkpoint, and selection gates.

### Approval recorded

- **Accepted (D-100):** Approve the P1-W04 Bigin Premier evidence-first outcome and authorize detailed execution-contract drafting, the CP-003 field-capacity map, and additional current official research only.
- D-100 does not approve the proposed contract or authorize an account, trial, tenant inspection, configuration, fixtures, testing, billing, purchase, connection, real data, communication, production use, Loryn participation, checkpoint, or platform selection.

### Work completed under D-100

- Revalidated current official Bigin pricing, field types and limits, default module fields, Team Pipelines, Stage Transition Rules, unique fields, pipeline records, activity relationships, and import behavior.
- Completed the conservative CP-003 field map at 10 Contact custom fields, 15 Pipeline custom fields, and at most 2 Task custom fields, each within Premier's documented separate 25-field-per-module limit without add-ons.
- Reserved one of the Pipeline module's two documented custom unique fields for the opportunity-level Centah lead number.
- Proposed one reusable Contact with multiple linked Pipeline records, Contact-plus-Activity prospecting before conversion, and one `Window Sales Work` Team Pipeline with source sub-pipelines only if direct evidence preserves a unified action center and distinct transition controls.
- Drafted the complete Premier-only execution contract with technical-partner-only ownership, minimum configuration, stopping rules, acceptance checks, synthetic-only controls, and separate exact action gates.

### Proposed action gates

- Contract: `Approve the complete P1-W04 execution contract`.
- Account: `Authorize the Bigin Premier trial account`.
- Any no-billing move from a higher trial edition to Premier: separate exact authorization after tenant inspection.
- Configuration and synthetic testing: `Begin P1-W04 synthetic configuration`.
- Payment, production, real data, external connections, Loryn finalist testing, CP-008, and platform selection remain separate later approvals.

### Files changed

- `deliverables/P1-W04-bigin-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W04/bigin/field-capacity-preflight.md`
- `evidence/P1-W04/bigin/official-evidence-preflight.md`
- `project-control/ARTIFACT_REGISTER.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`

### Saved ending point

Present the complete P1-W04 execution contract for explicit approval. Contract approval does not authorize account creation, trial activation, tenant inspection, configuration, or any other external action.

## Session S-074 - P1-W04 execution contract approved

**Date:** August 1, 2026

**Phase:** Phase 1

**Work unit:** P1-W04 - Bigin Premier evidence-first screening

**Checkpoint:** CP-007 remains the last signed-off checkpoint

**Sign-off status:** Complete execution contract approved as D-101; no Bigin account, trial, or tenant action authorized

### Orientation

- Current phase: Phase 1 CRM candidate comparison.
- Active work unit: P1-W04 Bigin Premier evidence-first screening.
- Last signed checkpoint: CP-007, which eliminated Pipedrive Lite only.
- Prior approval: D-100 approved the P1-W04 outcome for contract drafting, field mapping, and official research only.
- Open blockers: separate account authorization, exact trial edition, Premier isolation, and the direct evidence items defined by the contract.
- Approved outcome: bounded Premier-only evaluator screening with technical-partner-only administration and separate action gates.

### Approval recorded

- **Accepted (D-101):** Approve the complete P1-W04 Premier-only execution contract, including the tier boundary, prototype ownership, sequence, minimum configuration, stopping rules, separate action gates, acceptance checks, and CP-008 effect.
- D-101 approves the contract only. It does not authorize an account, trial, tenant inspection, edition change, configuration, fixture entry, testing, billing, purchase, external connection, real data, communication, production use, Loryn participation, checkpoint, or platform selection.

### Approved contract boundary

- Bigin Premier is the only directly evaluated tier; Free, Express, Bigin 360, add-ons, and connected Zoho services remain documentation-only.
- The technical partner is the sole evaluator administrator under D-093; Loryn remains deferred until a separately approved viable-finalist session.
- The conservative documentation map remains 10 Contact, 15 Pipeline, and at most 2 Task custom fields.
- Account creation, any no-billing edition change, synthetic configuration, paid action, external connection, finalist testing, CP-008, and platform selection remain separate approvals.
- Synthetic data, manual communications, no billing details, no production use, and all privacy prohibitions remain mandatory.

### Exact next action

Obtain the separate instruction `Authorize the Bigin Premier trial account`. That later authorization would permit only creation of the bounded evaluator account shell and inspection of nonprivate tier, trial-expiry, feature-boundary, sample-data, and administrator labels, followed by a stop before any edition change, configuration, fixture entry, or testing.

### Files changed

- `deliverables/P1-W04-bigin-evidence-first-screening.md`
- `deliverables/window-sales-operations-master-plan.md`
- `evidence/P1-W04/bigin/field-capacity-preflight.md`
- `evidence/P1-W04/bigin/official-evidence-preflight.md`
- `project-control/ARTIFACT_REGISTER.md`
- `project-control/CURRENT_STATE.md`
- `project-control/SESSION_LOG.md`

### Saved ending point

Present the separate Bigin Premier account-creation gate. Do not create an account or begin a trial without the exact authorization.
