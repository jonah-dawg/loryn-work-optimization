# P1-W04 Bigin Premier Evaluator Result

**Status:** Proposed - unapproved pending CP-008 review

**Candidate:** Bigin by Zoho CRM

**Directly evaluated tier:** Premier in a no-billing 15-day trial

**Evaluation date:** August 1, 2026

**Evaluator:** Technical-partner session with Codex-assisted Chrome control

**Device and application:** Windows desktop and Chrome; native mobile timing not reached

## Proposed outcome

Propose `Eliminated` for Bigin Premier. The candidate directly passed manual Centah uniqueness and provided useful source-specific Stage Transition Rules, reusable Contacts, search, tasks, events, and exception fields. However, direct TS-02 inspection confirmed that it cannot produce the approved reliable daily action center in the evaluated Premier configuration:

- source-specific sub-pipelines place Independent and Costco/Centah record lists on separate tabs;
- dashboards offer aggregate KPI, chart, and target components rather than actionable record lists; and
- Pipeline views cannot filter an active opportunity by the absence of a linked next Task.

`SYN-QUEUE-H` therefore cannot appear reliably with the named appointment, contact-due, overdue, and waiting-on-others records on one practical screen. This directly fails M-01 and also leaves the M-04 and M-07 next-action rule unsupported. The D-101 stopping rule ended the remaining mobile, export, administration, import-duplicate, and later scenario tests. No weighted score is calculated.

This result is not approved. CP-007 remains the last signed checkpoint; CP-008 requires a later explicit sign-off.

## Scenario result summary

| Scenario | Result | Direct observation | Remaining uncertainty |
|---|---|---|---|
| TS-01 quick prospect | `Unverified` | Contact prospect fields were configured, but the phone creation run was not reached. | Mobile timing, conversion history, and quick capture. |
| TS-02 morning action center | `Fail` | All five synthetic conditions existed, phone and last-name search found the Beta Contact, and the Tasks dashboard showed one overdue item. Source-tab separation, aggregate-only dashboard components, and no missing-linked-task view prevented one practical record queue. | None material to the direct M-01 stopping result. |
| TS-03 Costco/Centah lead | Desktop `Partial Pass` | Costco source and Centah field were visible; a manual duplicate using `SYN-CENTAH-1001` was blocked; a dated first-contact Task was saved. | Import duplicate handling and true due-time export were not tested. |
| TS-04 appointment | Desktop `Partial`; mobile `Unverified` | Saved an Event linked to the Beta job with synthetic location, 6:00-7:00 p.m. time, and 15-minute reminder. | Manual confirmation composer, directions, context reachability, and phone timing. |
| TS-05 visit and quote | Desktop `Partial` | Quote-sent date and visibly overdue decision-follow-up task were saved. | Visit note, quoted amount, manual-notice history, completion timestamp, and mobile entry were not completed. |
| TS-06 accepted-sale handoff | Desktop `Partial Pass` | Costco transition required Centah, DocuSign, and coordinator dates; Independent required coordinator date only; the next Costco transition required installation confirmation. | Six-week and three-month calculated anchors, completion after filled fields, and premature closure from other stages. |
| TS-07 installation exception | Desktop `Partial` | The synthetic three-month exception, still-unconfirmed status, retained reason, and same-day coordinator task were saved without automatic installation completion. | Unified morning visibility and customer-contact prompting failed or were not reached. |

## Mandatory-gate record

| ID | Result | Evidence | Limitation or uncertainty | Confidence |
|---|---|---|---|---|
| M-01 | `Fail` | Direct dashboard, source-tab, and Pipeline-view inspection; TS-02 | No one-screen actionable record queue and no reliable missing-linked-task detection. | High |
| M-02 | `Partial / Unverified` | Two source routes and direct Stage Transition Rule prompts | Handoff requirements were correct, but calculated source-specific installation-check dates were not completed. | Medium |
| M-03 | `Unverified` | Desktop search only | No parked-phone one-minute run. | High |
| M-04 | `Fail` | `SYN-QUEUE-H`, Tasks dashboard, Pipeline view criteria | Missing next actions on active Pipeline records cannot be surfaced reliably from linked Tasks. | High |
| M-05 | `Conditional Pass` | Premier shell and official preflight | One Super Admin was observed; production two-admin roles, MFA, removal, permissions, and history were not directly tested. | Low |
| M-06 | `Unverified` | Official preflight only | Export contents and customer-to-job reconstruction were not tested. | High |
| M-07 | `Fail` | Reusable Contacts, linked jobs, stages, fields, and view criteria | Core model fits, but neither required fields nor visible exception reporting upheld the active-record next-action invariant. | High |
| M-08 | `Unverified` | Manual-only configuration; no communication sent | Opt-out suppression and composer behavior were not tested. | Medium |
| M-09 | `Partial / Unverified` | Unique Pipeline field and blocked manual duplicate | Manual entry passed; import duplicate behavior and reconciliation export were not tested. | Medium |
| M-10 | `Unverified` | Desktop saves only | No cross-device, weak-signal, retry, pending-state, or duplicate-activity test. | High |
| M-11 | `Conditional Pass` | Official `$15` monthly / `$12` annual per-user pricing and Premier shell | Exact two-administrator checkout, renewal, tax, and commitment terms remain unverified. | Medium |
| M-12 | `Unverified` | Evaluator desktop setup only | No guided Loryn session or representative weekly-administration measurement occurred. | High |
| M-13 | `Pass` | Synthetic-only configuration and fixtures | No real record, message, integration, billing detail, or production action was used. | High |

## Direct configuration strengths

- Direct model fit: 10 Contact custom fields and 14 Pipeline custom fields plus standard Lead Source, within Premier's separate 25-field allowances.
- One Team Pipeline preserved reusable Contacts while two source routes allowed distinct transition rules.
- Costco handoff prompted for Centah, DocuSign, and coordinator dates; Independent prompted only for the coordinator date.
- The unique Centah field blocked a manual duplicate Opportunity.
- Global phone-number and last-name search both returned the intended synthetic Contact.
- Standard Events retained appointment time; Tasks provided reminders and visible overdue status.

## Direct limitations and stopping state

- The system label `Window Sales Work Standard` remained on the Independent route despite a rename attempt.
- Task Due Date is date-only. Reminder time exists separately and must be future.
- Saturday appeared outside configured working days despite the approved Saturday schedule.
- The correct native loss stage is labeled `Closed Lost`, not the approved display label `Lost / Canceled`.
- Closure Restriction was not configured because a broad rule could block legitimate early loss exits.
- Import duplicate handling, mobile timing, directions, note entry, cross-device reliability, export reconstruction, administrator removal, and exact production checkout were not reached after the mandatory failure.

## Tenant evidence left in place

Seven synthetic Contacts, seven synthetic Opportunities, three Tasks, one Event, the saved fields, stages, source routes, and transition rules remain in the evaluator tenant. Vendor samples and one blank malformed synthetic Contact remain recoverable in the recycle bin. The duplicate Opportunity was never saved. No final KPI or custom-view draft was saved.

## Approval boundary

A future CP-008 may approve this evaluator result, linked configuration inventory, tier/cost evidence, and evidence-backed `Eliminated` status only. It would not select another CRM, authorize another account or work unit, purchase Bigin, connect Centah or another service, use real data, permit customer communications, or begin a Loryn finalist session.
