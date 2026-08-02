# P1-CR01 - Simplified Personal CRM Scope

**Status:** Approved at CP-010

**Approved:** August 1, 2026

**Recorded:** August 1, 2026

**Triggered after:** P1-W06 and CP-009

## Reason for correction

The CP-004 evaluation method expanded a one-person CRM decision into a broader operational-platform evaluation. It required one product to reproduce Costco/Centah controls, enforce source-specific handoffs, manage installation exceptions, detect every missing job action, and present five action categories in one view. Those controls are useful possible extensions, but they are disproportionate to the immediate need and eliminated otherwise plausible personal CRMs for failures outside the clarified core outcome.

The immediate product outcome is a simple personal CRM that Loryn will consistently use to track independently received leads and prospects from email, text, referrals, and other personal sources. It must become the record of truth for those independent relationships, their history, and their next follow-up. It is not required to replace Centah or become a complete order, installation, or field-service platform.

## Approved system boundary

| Work or information | Authoritative system |
|---|---|
| Independently sourced leads and prospects | Personal CRM |
| Independent contact details, notes, activity history, status, next action, and due date | Personal CRM |
| Independent quote/decision status through `Won` or `Lost / Archived` | Personal CRM |
| Costco-originated lead and job processing, governed identifiers, and Costco-required actions | Centah |
| Optional awareness of a Costco lead in the personal CRM | A minimal manually entered reference or status note only |

- Centah remains the record of truth for Costco-originated work.
- The personal CRM remains the record of truth for independently sourced leads and prospects.
- A Centah integration, automatic synchronization, API, or duplicate-control mechanism is a future convenience, not a selection requirement.
- A manual extract, manual reference, or no cross-system copy is acceptable. If a Costco reference is recorded in the personal CRM, it must not override Centah-governed information.
- Independently sourced business is not required to enter Centah.

## Initial personal-CRM lifecycle

The selected CRM needs a small, understandable pipeline. Exact labels may be adapted to the product, but the initial configuration should represent:

1. `New`.
2. `Contacting`.
3. `Appointment Scheduled`.
4. `Quote / Decision`.
5. `Won`.
6. `Lost / Archived`.

The initial CRM does not need to manage internal order handoff, DocuSign, installation checks, three-month installation exceptions, post-install support, or repair cases. Those previously approved designs remain preserved as possible later expansions, but they are not initial platform-selection or configuration requirements.

Every active independent lead or prospect must have a next action and due date unless it is explicitly closed, archived, or placed in a documented exception state.

## Minimum fit requirements

A personal CRM remains viable when it can satisfy the following right-sized requirements in the production tier being considered:

### S-01 - Quick independent-lead capture

Create an independent lead from an email, text, referral, or other personal source with a name or useful identifier, at least one reachable channel, a short note, source, status, next action, and due date. Routine capture should take about one minute once the user is familiar with the product.

### S-02 - Practical mobile lookup and use

On a phone, Loryn can find a person by last name or phone number, review the record, open today's work, add a note, and update the next action without excessive screens or typing. Directions and appointment confirmation are useful preferences, not elimination gates.

### S-03 - Reliable relationship history

The CRM keeps contact details, notes, manually recorded calls, texts, emails, appointments, status changes, and follow-up history together in an understandable record. Automatic email or text capture is optional.

### S-04 - Today and overdue follow-up

The CRM provides a practical view of today's and overdue next actions. A single five-category dashboard, job-level waiting lists, and automatic discovery of every record missing a next action are not required. The operating rule is maintained through a simple saved view, task practice, visible exception, or routine review.

### S-05 - Simple pipeline and outcomes

The CRM supports the initial independent lifecycle, clear open and closed outcomes, and a reusable contact history. Multiple projects per person are useful when available but are not required for initial adoption if notes and closed history remain understandable.

### S-06 - Human-controlled communication

Calls, texts, and emails remain manually reviewed and sent. The CRM may launch or log a communication, but automatic sequences, purchased-list outreach, and customer-facing automation are not required and remain outside the initial release.

### S-07 - Dependable access, saving, and exit

The production setup supports Loryn as the primary user/administrator and Jonah as a secondary user or administrator during evaluation and approved support. Ordinary saves must be dependable, and contacts, notes, tasks, and pipeline information must have a usable export or practical exit path. Prototype MFA may remain optional; production security must be reviewed before real data is entered.

### S-08 - Proportionate cost and administration

The product must be understandable for a one-person operation, require little routine administration, disclose the likely two-user cost and meaningful limits, and avoid forcing enterprise-level configuration for ordinary use.

## Simplified comparison method

The finalist decision will use five practical dimensions instead of the CP-004 thirteen-gate operating-platform scorecard:

| Dimension | Weight |
|---|---:|
| Everyday mobile and desktop usability | 35 |
| Follow-up and next-action reliability | 25 |
| Contact history, search, and simple pipeline | 20 |
| Cost and administration burden | 10 |
| Access, export, and basic production readiness | 10 |

- A candidate is screened first against S-01 through S-08 using existing signed evidence and current official information where possible.
- A limitation is disqualifying only when it prevents the clarified personal-CRM outcome, creates unacceptable data loss or access risk, or makes routine use disproportionate.
- Integration depth, workflow automation, installation management, conditional source enforcement, elaborate reporting, and enterprise controls earn no extra credit unless they directly improve the initial personal workflow.
- No more than two viable finalists will be placed in front of Loryn.
- Loryn will receive one guided practical session of approximately 15 to 20 minutes per finalist, with no evidence-recording work, homework, or follow-up test burden.
- The practical session covers only capture, lookup, note/history review, next-action update, today's/overdue work, and pipeline status.
- The selected CRM must be the simplest acceptable product Loryn is willing to maintain, not the product with the largest feature set.

## Effect on previous checkpoints and candidates

- CP-004 remains an immutable record of the evaluation method approved on July 30, 2026, but its M-01 through M-13 gates, weights, fixtures, and TS-01 through TS-07 are superseded for all future platform selection by CP-010 and this artifact.
- CP-007, CP-008, and CP-009 remain valid evidence-backed results against the CP-004 method. Their historical findings are not deleted or rewritten.
- Pipedrive Lite, Bigin Premier, and Less Annoying CRM are no longer automatically excluded from the simplified personal-CRM comparison solely because they failed a superseded CP-004 gate.
- Reconsideration should reuse existing signed evidence first and requires a later approved work unit before any new account, tenant action, configuration, or testing.
- Zoho, HubSpot, and Freshsales limitations remain useful evidence but do not require further evaluation unless one becomes a finalist under the simplified screen.
- OnePageCRM, Less Annoying CRM, Capsule, and the already-inspected Bigin configuration may be considered during paper screening. This shortlist is not a selection or an account authorization.

## CP-010 acceptance review

- [x] The personal CRM is the record of truth for independently sourced leads and prospects.
- [x] Centah remains authoritative for Costco-originated work.
- [x] Centah integration is optional, and a manual reference or extract is acceptable.
- [x] The initial CRM lifecycle ends at a clear won or lost/archive outcome rather than requiring complete installation operations.
- [x] The next-action and due-date rule remains in force for active independent records.
- [x] Eight right-sized minimum fit requirements replace the thirteen mandatory operating-platform gates.
- [x] The comparison emphasizes usability, follow-up reliability, simple history, cost, and portability.
- [x] Prior evidence and signed eliminations remain historically intact but do not bind the new scope.
- [x] At most two finalists will reach Loryn, with no homework or evidence burden.
- [x] No platform is selected and no account, trial, billing, integration, real-data, or communication action is authorized.

## Effect on current work

CP-010 approves this scope correction, supersedes the CP-004 evaluation method for future candidate selection, and closes the current chat's scope-reset outcome. Phase 1 remains active with no selected CRM and no active candidate work unit. The next chat should begin P1-W07 as a simplified finalist-screening definition, reuse existing evidence, and seek explicit approval before any new external platform action.
