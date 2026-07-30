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
