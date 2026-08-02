# P1-W06 - Less Annoying CRM Evidence-First Definition

**Status:** Proposed work-unit outcome - Unapproved; definition and current official research authorized under D-109

**Phase:** Phase 1 - CRM candidate comparison

**Updated:** August 1, 2026

**Last signed-off checkpoint:** CP-008

## Definition authority

- **Accepted (D-109):** Begin the P1-W06 Less Annoying CRM evidence-first definition and current official research only.
- D-109 authorizes this proposed-outcome record, the official-evidence preflight, and project-control synchronization.
- D-109 does not approve the proposed outcome or an execution contract and does not authorize public-demo interaction, an account, trial, tenant inspection, configuration, fixture entry, testing, billing, purchase, external connection, real data, customer communication, production use, Loryn participation, checkpoint sign-off, or platform selection.

## Proposed work-unit outcome - Unapproved

Evaluate the single-tier Less Annoying CRM product as the next independent-work CRM candidate through an evidence-first, evaluator-only process. Begin with current official evidence and, only after later separate approvals, a bounded public-demo inspection before deciding whether an account is justified. If the record model remains plausible, prepare a CP-003 field map and a complete execution contract before any signup or configuration.

## Recommendation

Approve the proposed work-unit outcome, but keep LACRM unapproved as a viable or preferred platform. It is the most proportionate next candidate because:

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
- No account, trial, demo interaction, or external service is authorized by D-109.

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

## Proposed definition boundary - Unapproved

- The single current LACRM tier is the only proposed evaluated product. Do not add custom code or an external automation service to make it pass.
- The technical partner remains the sole evaluator under D-093. Loryn remains deferred until a separately approved viable-finalist session.
- Start with official evidence. If the outcome and later contract are approved, inspect the public no-signup demo before authorizing an account.
- Test the job-specific next-action invariant first using one synthetic contact with two active pipeline items and distinct action states.
- Use only the signed CP-004 fixtures and manual/no-send communication controls if later execution is authorized.
- Keep credentials, private emails, identifiers, billing information, and browser/session data outside all project artifacts.

## Proposed approval sequence - Unapproved

1. Begin definition and official research. Completed as D-109.
2. Explicitly approve or reject the proposed outcome.
3. If approved, prepare the CP-003 field map and complete execution contract.
4. Explicitly approve or reject the complete contract.
5. Separately authorize a bounded public-demo inspection focused on task-to-job linkage and the unified action center.
6. If the demo remains plausible, separately authorize a no-credit-card evaluator account and nonprivate tenant inspection.
7. Separately authorize synthetic configuration and evaluator testing.
8. Present the evidence-backed viable, eliminated, or incomplete result for a later checkpoint decision.

## Current action

Review and explicitly approve or reject the proposed P1-W06 work-unit outcome. No demo interaction, account, trial, tenant inspection, configuration, or external action is authorized by D-109.
