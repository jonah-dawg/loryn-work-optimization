# P1-W06 Less Annoying CRM Official-Evidence Preflight

**Status:** Current under D-111; complete contract approved; no demo, account, or tenant action authorized

**Candidate:** Less Annoying CRM (LACRM)

**Proposed evaluated product:** Single all-features tier

**Reviewed:** August 1, 2026

## Preflight result

LACRM is a proportionate next evidence-first candidate, not a viable or preferred result. Its single `$15` per-user monthly tier, full 30-day no-credit-card trial, public no-signup demo, unlimited pipelines and custom fields, two-factor authentication, user permissions, mobile-browser access, exports, automations, and open API reduce cost and tier ambiguity.

The record model has one decision-critical uncertainty. LACRM supports multiple pipeline items for separate orders on one reusable contact, but its task documentation and API link a task to a Contact rather than a Pipeline Item. The documented missing-follow-up filter likewise identifies contacts in a pipeline with no pending task or event. One task may therefore conceal a second active job with no next action. That M-01/M-04/M-07 risk must be tested before broad configuration or scoring.

## Official-evidence summary

| Area | Current official evidence | P1-W06 effect |
|---|---|---|
| Price and trial | One tier at `$15` per user per month plus tax; 30-day full-access trial; no credit card; no annual contract or feature tiers | Clear preliminary M-11 boundary; two-admin baseline `$30` monthly or `$360` yearly before tax |
| Public access | The official product tour links to a live demo without signup | Allows a later bounded record-model inspection before an account, but interaction requires separate approval |
| Customer and jobs | Contacts/companies are primary records; multiple pipeline items can represent multiple orders or projects for one contact | Plausible reusable customer-to-multiple-job model |
| Tasks | Tasks have due dates, remain open until completed, and may attach to a Contact; timed work uses Events; the API exposes `ContactId` but no `PipelineItemId` | Critical job-specific next-action risk; direct two-job negative test must run first |
| Missing follow-up | A pipeline report can filter for contacts without an associated pending task or event | Promising visibility, but apparently contact-scoped rather than job-scoped |
| Pipelines and fields | Unlimited pipelines, custom contact fields, and custom pipeline fields; pipeline list/board reports and saved filters | Ample apparent field capacity; exact CP-003 map and view behavior remain unverified |
| Automations | Manual or status-triggered automations can assign a user, attach a note/task/group, or attach a pipeline | Plausible reminders; source conditions, working-day timing, and job-specific task scope remain unverified |
| Duplicate and source controls | Bulk actions can create duplicate pipeline items; no current official evidence found for unique pipeline fields or conditional required fields | M-02/M-09 remain unverified; do not infer uniqueness from internal record IDs |
| Mobile | Product is available in a mobile browser; contacts, tasks, events, pipelines, and notes are marketed for mobile use | M-03/M-10 require direct timing and weak-signal tests; no offline guarantee found |
| Search | Product tour states search by name, keyword, or stored detail | Phone-number and last-name behavior require direct proof |
| Reporting and export | Task, activity, contact, and pipeline reports plus admin bulk export and an open API are documented | Plausible M-06 path; full relationship reconstruction remains unverified |
| Security and access | Two-factor authentication, admin/user roles, export/delete permissions, contact/calendar sharing, lockout, reassignment, and user deletion are documented | Preliminary M-05 support; two-admin ownership and preserved history require direct evidence |
| Retention and backup | Encryption, real-time/offsite backups, one-year post-cancellation archive, and immediate deletion on request are documented | Preliminary governance evidence; exact production policy remains a later decision |
| Communications | Email/calendar integrations and automations exist but are optional | Preserve manual/no-send testing with all external communication connections disabled |

## Mandatory-gate preflight

| Gate | Official-evidence state | Required direct proof if later approved |
|---|---|---|
| M-01 Reliable daily action center | `Unverified` | One practical view with all five categories and a second job missing its own next action while the shared contact has another task |
| M-02 Correct source-specific workflow | `Unverified` | Costco/Centah versus Independent branches, source-specific handoff and dates, conditional prompts, and retained exceptions |
| M-03 Essential mobile tasks within one minute | `Unverified` | Mobile-browser phone/last-name search, today's work, confirmation, directions, and note timing |
| M-04 Reliable reminders and next actions | `Unverified` | Job-specific tasks, overdue behavior, working-day schedules, quote/handoff/installation reminders, and missing-action detection |
| M-05 Administration and access control | `Conditional Pass` | Two admins, 2FA, ownership, lockout/removal, permissions, recovery, and preserved activity history |
| M-06 Data portability and lifecycle control | `Conditional Pass` | Bulk export and reconstruction of Contacts, pipeline items, tasks, events, notes, dates, outcomes, and identifiers |
| M-07 Approved record and lifecycle model | `Unverified` | Reusable Contact with multiple independent job records, conversion history, complete fields/stages, and per-job next actions |
| M-08 Human-controlled communications | `Conditional Pass` | Keep email/calendar connections and automated external sending disabled while internal tasks remain usable |
| M-09 Safe Centah/Costco bridge | `Unverified` | Unique/reviewable job-level Centah identifier and reliable manual/import duplicate reconciliation |
| M-10 Reliable save and synchronization | `Unverified` | Browser save confirmation, weak-signal behavior, retry, duplicate avoidance, and desktop/mobile consistency |
| M-11 Evidence-backed cost and tier | `Conditional Pass` | Confirm exact checkout, two users, tax, renewal, trial expiry, limits, and absence of paid extras |
| M-12 Sustainable learning and administration | `Conditional Pass` | One guided session, no routine duplicate entry, setup effort, and weekly administration estimate |
| M-13 Common synthetic evidence standard | `Conditional Pass` | Same CP-004 fixtures, scripts, timing, evidence rows, sanitation, and stopping rules |

These are research preflight labels, not evaluation results. D-111 approves the complete execution contract but authorizes no public-demo interaction, account, trial, tenant action, or direct test; no LACRM gate has passed.

## Proposed pre-demo stopping checks

- Map the CP-003 Contact, job, and activity fields without hiding required facts in Notes.
- Treat task-to-job linkage as the first public-demo stopping test using one Contact with two active job pipeline items.
- Require one job to have a task and the other to lack one; verify whether the missing-action report identifies only the uncovered job.
- Check whether pipeline fields can be required conditionally and whether Centah identifiers can be unique or reliably reviewed.
- Confirm that a public demo cannot expose private third-party data and that no signup or persistent external change is required.
- Keep accounts, trials, connections, communications, billing, real data, production use, Loryn participation, and platform selection prohibited.

## Official sources reviewed

- [LACRM pricing and trial](https://www.lessannoyingcrm.com/pricing)
- [LACRM product tour and public demo](https://www.lessannoyingcrm.com/tour)
- [Using pipelines for multiple orders](https://www.lessannoyingcrm.com/help/use-pipelines-to-track-multiple-orders)
- [Pipeline reports and configuration](https://www.lessannoyingcrm.com/help-topics/pipelines)
- [Filter pipeline contacts with no task](https://www.lessannoyingcrm.com/help/filter-pipeline-by-no-follow-up-scheduled)
- [Task API and Contact-scoped linkage](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks)
- [Pipeline Item API](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items)
- [Creating status-triggered automations](https://www.lessannoyingcrm.com/help/creating-automations)
- [Custom field types](https://www.lessannoyingcrm.com/help/custom-field-types)
- [Bulk data export](https://www.lessannoyingcrm.com/help/exporting-all-of-your-data-out-of-lacrm)
- [User permissions](https://www.lessannoyingcrm.com/help/managing-sharing-permissions-for-other-users)
- [Two-factor authentication](https://www.lessannoyingcrm.com/help/how-to-turn-off-two-factor-authentication)
- [User lockout, reassignment, and deletion](https://www.lessannoyingcrm.com/help/removing-an-existing-user-from-your-account)
- [Security and backups](https://www.lessannoyingcrm.com/help/data-security-and-backups)
- [Privacy and retention](https://www.lessannoyingcrm.com/help/privacy)
