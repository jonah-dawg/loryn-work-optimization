# P1-W06 - Less Annoying CRM Evidence-First Definition

**Status:** Signed off at CP-009; Less Annoying CRM eliminated by direct M-01 failure; P1-W06 closed

**Phase:** Phase 1 - CRM candidate comparison

**Updated:** August 1, 2026

**Last signed-off checkpoint:** CP-009

## Definition authority

- **Accepted (D-109):** Begin the P1-W06 Less Annoying CRM evidence-first definition and current official research only.
- **Accepted (D-110):** Approve the P1-W06 proposed outcome and authorize the CP-003 field-model preflight, complete-contract drafting, additional current official research, and project-control synchronization only.
- **Accepted (D-111):** Approve the complete P1-W06 execution contract, including its product boundary, evaluator ownership, action sequence, minimum configuration, first stopping test, remaining stopping rules, evidence controls, and checkpoint boundary.
- **Accepted (D-112):** Authorize the bounded P1-W06 LACRM public-demo inspection under the approved contract and stop before account creation or any broader action.
- D-112 authorizes only the no-signup public-demo inspection. It does not authorize an account, trial, persistent tenant, configuration, fixture entry beyond temporary demo observation, billing, purchase, external connection, real data, customer communication, production use, Loryn participation, checkpoint sign-off, or platform selection.

## Approved work-unit outcome

Evaluate the single-tier Less Annoying CRM product as the next independent-work CRM candidate through an evidence-first, evaluator-only process. Begin with current official evidence and, only after later separate approvals, a bounded public-demo inspection before deciding whether an account is justified. If the record model remains plausible, prepare a CP-003 field map and a complete execution contract before any signup or configuration.

## Current recommendation

Continue to complete-contract review, but keep LACRM unapproved as a viable or preferred platform. It is the most proportionate next candidate because:

- One current tier includes all features for `$15` per user per month, or `$30` per month plus tax for two administrators.
- The 30-day trial is described as full access with no credit card, and a public live demo is available without signup.
- Official material lists unlimited contacts, pipelines, custom fields, task management, user permissions, mobile access, two-factor authentication, exports, automations, and an open API.
- One reusable contact may have multiple pipeline items representing separate orders or projects.
- Its single tier avoids the edition contamination, field-count, and forced-upgrade ambiguity encountered in prior candidates.

The first stopping risk is material: official task documentation exposes a Contact link but no Pipeline Item link, and the documented missing-follow-up filter finds contacts in a pipeline without a task. With multiple active jobs on one customer, a task for one job may therefore make another job appear covered. P1-W06 must test this before any broad configuration.

## Current documented boundary

- One production tier at `$15` per user per month plus tax; indicative two-administrator cost is `$30` per month or `$360` per year before tax.
- The free trial is 30 days, includes the full product, and requires no credit card according to current official pricing.
- The public product tour links to a live demo that does not require signup. Demo interaction remains a separately authorized action.
- LACRM is browser-based on mobile rather than relying on a required native app. Current material does not establish offline editing, pending-sync visibility, conflict handling, or retry behavior.
- No account, trial, demo interaction, or external service is authorized by D-110.

## Decision-critical risks

### 1. Job-specific next actions

Pipeline items can represent multiple orders for one contact, but tasks are documented as attached to a Contact or left unattached. The API task model has `ContactId` and no documented `PipelineItemId`. The public demo must prove whether each active job can own a distinct next action and due date and whether a missing action on one job remains visible when the same customer has another task.

### 2. One-screen morning action center

Official evidence supports a Workspace task list, daily agenda email, task reports, pipeline reports, and a filter for pipeline contacts without pending tasks or events. It does not establish one practical view containing today's appointments, contacts due today, overdue actions, waiting-on-others jobs, and every active job missing its own next action. M-01 remains `Unverified`.

### 3. Source-specific integrity

Unlimited pipeline fields and status automations are documented. Current official material does not establish conditional required fields, a unique pipeline-level Centah identifier, or a duplicate-review path that distinguishes two legitimate jobs for one customer from an accidental duplicate. M-02 and M-09 remain `Unverified`.

### 4. Mobile and time precision

LACRM supports mobile-browser access. Tasks carry dates but not times; timed work uses Events. The later evaluator must test phone-number and last-name search, today's work, manual confirmation, directions, note capture, the one-minute limit, 7:45 a.m. confirmation reminders, and save/retry behavior.

### 5. Export and history reconstruction

Admin bulk export, pipeline export, activity reports, notes, and API resources are documented. Direct evidence must prove that customers, multiple jobs, job-specific notes, tasks, events, statuses, dates, close outcomes, and Centah identifiers can be reconstructed without manual copying.

### 6. Right-sized administration

Two-factor authentication, admin/user permissions, immediate lockout, user deletion/reassignment, encrypted backups, and one-year post-cancellation retention are documented. Direct evidence must confirm that two administrators can maintain the approved model within the roughly 15-minute weekly administration limit.

## Approved evaluator boundary

- The single current LACRM tier is the only proposed evaluated product. Do not add custom code or an external automation service to make it pass.
- The technical partner remains the sole evaluator under D-093. Loryn remains deferred until a separately approved viable-finalist session.
- Start with official evidence. If the complete contract is later approved, inspect the public no-signup demo under a separate authorization before considering an account.
- Test the job-specific next-action invariant first using one synthetic contact with two active pipeline items and distinct action states.
- Use only the signed CP-004 fixtures and manual/no-send communication controls if later execution is authorized.
- Keep credentials, private emails, identifiers, billing information, and browser/session data outside all project artifacts.

## Approval sequence

1. Begin definition and official research. Completed as D-109.
2. Approve the proposed outcome and authorize field-map and contract drafting only. Completed as D-110.
3. Prepare the CP-003 field map and complete execution contract. Completed as an unapproved draft under D-110.
4. Approve the complete execution contract. Completed as D-111.
5. Authorize and run the bounded public-demo inspection focused on task-to-job linkage and the unified action center. Completed as D-112; M-01 failed directly.
6. If the demo remains plausible, separately authorize a no-credit-card evaluator account and nonprivate tenant inspection. Not reached because the stopping rule fired.
7. Separately authorize synthetic configuration and evaluator testing. Not reached.
8. Present the evidence-backed `Eliminated` result for a later checkpoint decision. Current action.

## CP-003 field-model result

The proposed minimum model uses 8 Contact custom fields, 7 Prospecting pipeline fields, and 20 Window Sales Work pipeline fields. LACRM documents unlimited custom fields, so field quantity is not the concern. The critical issue is relationship integrity: Tasks and Events are Contact-scoped, while the next-action invariant applies separately to each active Prospecting or Window Sales Work pipeline item.

The draft therefore keeps `Next action` and `Next action due` as canonical pipeline-item fields and treats any Contact-linked Task as a reminder whose title must include the pipeline-item label. A direct evaluator run must prove that empty next-action fields can be found per pipeline item and that reminder creation, completion, and rescheduling do not require unsustainable duplicate entry. The complete mapping is in `../evidence/P1-W06/lacrm/field-model-preflight.md`.

## Approved complete execution contract

### Product and ownership boundary

- Evaluate only LACRM's single all-features tier. Do not add custom code, paid services, external automations, or integrations to make the candidate pass.
- The technical partner remains the sole evaluator under D-093. Loryn remains deferred until a separately approved viable-finalist session.
- Keep all records synthetic and all customer-facing communications manual and unsent.

### Execution sequence

1. Approve this complete contract. Completed as D-111.
2. If approved, separately authorize a bounded public-demo inspection that requires no signup.
3. In the public demo, inspect task-to-job linkage, blank pipeline-field filtering, the unified action center, field controls, and mobile-browser behavior before considering an account.
4. Stop if the demo requires signup, exposes nonpublic personal information, cannot preserve a synthetic-only boundary, or directly establishes a mandatory failure.
5. If the candidate remains plausible, separately authorize a no-credit-card evaluator account and nonprivate tenant-shell inspection.
6. Stop after recording the product, trial-expiry, sample-data, user-role, and feature-boundary labels.
7. Separately authorize synthetic configuration and evaluator testing before changing the tenant or entering CP-004 fixtures.
8. Run mandatory stopping tests first, then only the minimum remaining CP-004 scenarios needed for a comparable result.
9. Present the evidence-backed `Viable`, `Eliminated`, or `Incomplete` result for a later checkpoint decision.

### Minimum configuration if later authorized

- Two pipelines: `Prospecting` and `Window Sales Work`.
- The field model in `../evidence/P1-W06/lacrm/field-model-preflight.md`, with no speculative extras.
- One reusable Contact may hold multiple distinct pipeline items; the job label must be visible on each badge.
- Pipeline-item `Next action` and `Next action due` fields remain canonical until direct evidence proves a simpler reliable method.
- Any Contact-linked Task or Event title must begin with the relevant synthetic pipeline-item label so two jobs for one Contact remain distinguishable.
- Keep email, calendar, maps, Centah, API, webhooks, and every other external connection disabled.

### First stopping test

Use one synthetic Contact with two active Window Sales Work pipeline items. Give the first item a distinct next action and reminder; leave the second item's next-action fields blank. The candidate fails if one practical action-center route cannot reveal the uncovered second job without opening records individually, or if the first job's Contact-linked task makes the second job appear covered.

### Remaining mandatory stopping rules

- Stop on any direct M-01 through M-13 failure; do not continue merely to collect a numeric score.
- Stop if Costco/Centah-only fields cannot be visibly separated or exceptions cannot be reported reliably.
- Stop if a duplicate Centah identifier cannot be blocked or routed to a practical visible review without custom code.
- Stop if routine next-action handling requires repeated manual entry across pipeline fields and Tasks beyond the roughly 15-minute weekly administration target.
- Stop if the trial requires billing, an annual commitment, a disallowed identity, or a higher-priced product.
- Stop before external connections, real data, outbound communications, production use, Loryn participation, checkpoint sign-off, or platform selection.

### Evidence and cleanup

- Use only CP-004 synthetic fixtures and its accepted evidence-row format.
- Sanitize screenshots and exports; exclude credentials, private email addresses, account identifiers, session data, and unrelated records.
- Record official claims separately from direct observations and label every unrun gate `Unverified`.
- Do not permanently delete recoverable vendor sample data without separate necessity and scope confirmation.
- If a later run stops, record the exact stopping evidence and the remaining synthetic tenant state before any cleanup.

### Checkpoint boundary

A later P1-W06 checkpoint may approve only the evidence set, configuration inventory, cost/tier record, and `Viable`, `Eliminated`, or `Incomplete` result. It will not by itself select LACRM, authorize payment or production use, permit real data, connect Centah or another service, send customer communications, or begin Loryn finalist testing.

## Public-demo inspection result

The official no-signup demo opened as a temporary vendor demo account after selecting only the generic industry profile and the `2-5` user range. No identity, credentials, billing information, account, trial, real data, connection, or customer communication was supplied.

Direct inspection established:

- Workspace combines a due-task widget, pipeline-report widget, activity report, and calendar preview.
- The task widget can show due or overdue Tasks by calendar but Tasks expose an `Attached contact`, not a pipeline item.
- The pipeline widget can select user scope and pipelines, but it presents pipeline/status summaries rather than the actionable records from a saved or filtered view.
- A Contact page presents an upcoming Task and a Lead pipeline item as separate attached-item sections, reinforcing that the Task is Contact-scoped.
- Pipeline customization supports multiple statuses, custom fields, a global required-field checkbox, pipeline-report display, and pipeline-badge display. The inspected field dialog exposed no conditional-requirement or unique-value option.

M-01 fails directly. One Workspace cannot show all five required categories as actionable records because `waiting on someone else` jobs and active jobs missing their own next action cannot appear as record-level items beside today's appointments, contacts due today, and overdue actions. The pipeline widget exposes only aggregate status counts, and its settings offer pipeline/user scope rather than a saved filtered record view.

The approved mandatory stopping rule ended the run immediately. No account, tenant, custom field, record, task, filter, view, widget setting, or configuration was saved. The temporary demo tab was closed. All other gates remain `Unverified`; they were not run merely to collect a score. Detailed sanitized evidence is in `../evidence/P1-W06/lacrm/public-demo-inspection.md`.

## Approved evaluator result

**Signed off (CP-009):** `Eliminated` because LACRM directly fails M-01. CP-009 approves the sanitized public-demo evidence, the direct gate result, and closure of P1-W06. It does not select another CRM, authorize an account or next candidate, or change any production boundary.

## Current action

Define and present the next evidence-first Phase 1 CRM candidate and proposed outcome for explicit approval. No next candidate, account, trial, configuration, external action, Loryn session, or platform selection is authorized by CP-009.
