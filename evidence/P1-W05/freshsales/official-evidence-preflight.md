# P1-W05 Freshsales Pro Official-Evidence Preflight

**Status:** Closed documentation-only under D-108; signup blocked before account creation; no direct tenant evidence

**Candidate:** Freshsales

**Proposed evaluated tier:** Pro

**Reviewed:** August 1, 2026

## Preliminary disposition

Freshsales Pro is the approved P1-W05 evidence-first candidate, but it is not yet viable or preferred. It is the lowest documented Freshsales tier that combines 250 custom fields per module, up to 10 deal pipelines, and field dependencies. Its unique Deal fields, Activities dashboard, workflow-created tasks, mobile offline behavior, full export, and API surface make it a credible response to failures observed in prior candidates.

The largest unresolved issue is M-01. Official documentation shows actionable daily and overdue activity lists, but not one practical view that also detects waiting-on-others Deals and active Deals with no next action or due date. Trial contamination, field-dependency import bypass, Pro-versus-Enterprise administration history, exact checkout, and direct mobile behavior also remain unresolved.

## Evidence summary

| Area | Current official evidence | P1-W05 effect |
|---|---|---|
| Pricing | Pro is `$39` per user per month billed annually. Enterprise is `$59`. A Freshworks published price list identifies `$47` monthly-billed Pro. | Two-admin Pro baseline: `$936` annually or an indicative `$94` monthly-billed total. Exact checkout, tax, renewal, and add-ons remain unverified. |
| Trial | Freshsales describes a 21-day, fully loaded trial; support pages state no credit card is required. At expiry, continued use requires selecting and paying for a plan, otherwise the account is suspended. | No account is authorized. A future contract must isolate Pro-equivalent evidence before configuration. |
| Tier boundary | Growth has 150 custom fields, one pipeline, and no active field dependencies after downgrade. Pro has 250 custom fields, up to 10 pipelines, and up to 100 dependencies per entity. Enterprise adds audit logs, field-level permissions, sandbox, and custom modules. | Pro is the lowest plausible source-specific tier. Enterprise features remain documentation-only unless a mandatory gate proves them necessary. |
| Record model | Contacts, Accounts, Deals, Tasks, Appointments, Sales Activities, and Notes are documented, including APIs for related records. | Plausible reusable Contact-to-multiple-Deal model; direct relationship and conversion-history checks remain required. |
| Conditional requirements | A controlling dropdown/checkbox/radio can reveal a dependent field and make it required for only the applicable choice. | Plausible Costco/Centah-only field prompts without imposing them on Independent work. |
| Dependency limitation | Imports and bulk updates can save controlling/dependent values without dependency validation; mismatched dependent values may be stored but hidden from the form. | Decision-critical M-02/M-09 integrity risk. Direct negative import and reconciliation tests are mandatory. |
| Unique values | Deal custom fields can be marked unique. Freshsales says uniqueness is validated on manual save, bulk update, API, and CSV import. | Strong preliminary evidence for a unique opportunity-level Centah identifier; exact Deal-field behavior must be tested. |
| Pipelines | Growth supports 1 pipeline, Pro 10, Enterprise 25; each pipeline has at least 3 stages and no documented upper stage limit. | The approved lifecycle fits. Prefer testing one unified pipeline plus source control first to avoid the split-view failure seen in Bigin. |
| Daily action visibility | The Activities dashboard shows tasks, meetings, and custom activities by due date for today/tomorrow/week and provides Open, Overdue, and Completed tabs. The mobile home shows a weekly calendar, tasks, appointments, and overdue tasks. | Promising, actionable evidence, but M-01 remains `Unverified` because waiting-on-others and missing-next-action records are not shown in the same documented view. |
| Workflows and reminders | Workflows can create tasks with due dates relative to execution or record date fields and can operate on contacts, deals, appointments, and tasks. | Plausible quote, follow-up, handoff, and installation reminders; working-day timing and three-month exception behavior require direct tests. |
| Search and mobile | Web global search documents record names and activity titles. Mobile supports quick-add records/activities, calendar, tasks, appointments, voice notes, cached views, offline creation, and later sync. | Phone/last-name lookup, directions, tap/time limits, save conflicts, and recovery behavior remain direct-test items. |
| Import/export | CRM import supports Contacts, Accounts, and Deals with mappings, mandatory fields, duplicate options, histories, and error downloads. Full account export can include contacts, deals, activities, sales activities, users, and email logs; full export is limited to once in the selected range and exports are limited to five daily. | Plausible manual Centah bridge and exit path. Notes, task links, customer-to-job reconstruction, and exact retention still need direct evidence. |
| API | Official CRM APIs cover Contacts, Accounts, Deals, Notes, Tasks, Appointments, Sales Activities, search, upserts, and deletes; the documented account limit is 1,000 requests per hour. | Plausible future thin-adapter path only. No API token, connection, or integration is authorized. |
| Administration | Freshsales documents account/admin roles, custom role scopes, user reassignment/deletion, account exports, and 90-day configuration audit logs. Current pricing lists audit logs and field-level permissions under Enterprise. | Two-admin Pro ownership is plausible, but MFA, recovery, access removal, Pro-level activity history, and any Enterprise dependency remain unverified. |

## Mandatory-gate preflight

| Gate | Official-evidence state | Required direct proof if the outcome and contract are later approved |
|---|---|---|
| M-01 Reliable daily action center | `Unverified` | One practical desktop and mobile action center showing all five required categories, including a Deal missing its next action/due date. |
| M-02 Correct source-specific workflow | `Conditional Pass` | One-pipeline source branch, conditional Costco fields, correct handoff, source-specific installation anchor, and negative import cases. |
| M-03 Essential mobile tasks within one minute | `Unverified` | Phone and last-name search, today's work, manual confirmation, directions, and note timing while parked. |
| M-04 Reliable reminders and next actions | `Conditional Pass` | Quote, call-back, handoff, installation, exception, and missing-next-action reminders under actual working-day rules. |
| M-05 Administration and access control | `Unverified` | Two administrators, MFA, role boundary, prompt removal, recovery ownership, and sufficient important-change history in Pro. |
| M-06 Data portability and lifecycle control | `Conditional Pass` | Full synthetic export and reconstruction of Contacts, Deals, Tasks, Activities, Notes, dates, outcomes, and identifiers; retention/exit record. |
| M-07 Approved record and lifecycle model | `Conditional Pass` | Reusable Contact with multiple Deals, separate prospecting history, complete stages/fields, and visible next-action exception handling. |
| M-08 Human-controlled communications | `Conditional Pass` | All email/SMS/phone/sequence sending remains disconnected or disabled; manual action prompts do not send. |
| M-09 Safe Centah/Costco bridge | `Conditional Pass` | Unique Deal identifier in manual/API/import paths plus an explicit review route for source/dependency mismatches. |
| M-10 Reliable save and synchronization | `Unverified` | Desktop/mobile/offline save, later sync, conflict behavior, duplicate avoidance, and visible recovery from failure. |
| M-11 Evidence-backed cost and tier | `Conditional Pass` | Exact tenant edition, Pro feature isolation, checkout for two admins, billing cadence, renewal, tax/add-ons, and suspension/downgrade effects. |
| M-12 Sustainable learning and administration | `Unverified` | Guided evaluator use, routine cleanup, configuration inventory, and weekly administration estimate. |
| M-13 Common synthetic evidence standard | `Conditional Pass` | Same CP-004 fixtures, TS-01 through TS-07, result rows, device/tier record, sanitized evidence, and stopping rules. |

These states are research preflight labels, not evaluation results. D-105 approved the outcome and field-map/contract drafting only; no Freshsales gate has passed.

## Observed signup blocker and closure

- On August 1, 2026, the user reported that Freshsales rejected the available Gmail evaluator address and required a business email during the authorized D-107 signup attempt.
- No Freshsales account, trial, or tenant was created or inspected, and no billing information, configuration, fixture, test, integration, real data, or customer communication was used.
- The report is a direct evaluator observation supplied by the user; no screenshot or private account information is stored in the repository.
- D-108 closes P1-W05 incomplete without CP-009 rather than obtaining, purchasing, or fabricating a business-domain identity solely for the evaluation.
- Freshsales Pro remains documentation-only and unscored. Its official-evidence gate labels are not direct evaluation results.

## Proposed pre-account stopping checks

- Map every CP-003 field to Freshsales defaults or Pro custom fields without hiding required facts in Notes.
- Define a one-pipeline source model first; use multiple pipelines only if direct evidence proves that one action center remains unified.
- Prove from current official material which workflow, dependency, unique-field, view, export, API, administrator, and mobile features belong to Pro.
- Define a trial-contamination check that records only nonprivate edition, expiry, sample-data, and feature-boundary labels.
- Stop before account creation if official evidence establishes an M-01 failure, an unavoidable Enterprise dependency at unreasonable cost, or a field/source model that cannot remain correct during import.
- Keep all external connections, communications, billing, real data, production use, Loryn participation, and platform selection prohibited.

## Official sources reviewed

- [Freshsales pricing](https://www.freshworks.com/crm/pricing/)
- [Freshworks published price list](https://dam.freshworks.com/m/4bf615e1eea87a7/original/Freshworks-Price-List.pdf)
- [Freshsales custom fields and plan limits](https://crmsupport.freshworks.com/support/solutions/articles/50000002389-how-to-create-custom-fields-for-contacts-accounts-and-deals-)
- [Freshsales field dependencies](https://crmsupport.freshworks.com/support/solutions/articles/50000002573-how-to-configure-field-dependency-)
- [Freshsales unique fields](https://crmsupport.freshworks.com/support/solutions/articles/50000002578-what-are-unique-fields-why-are-few-fields-marked-as-unique-by-default-)
- [Freshsales multiple deal pipelines](https://crmsupport.freshworks.com/support/solutions/articles/50000002957-how-to-configure-multiple-deal-pipelines-)
- [Freshsales Activities dashboard](https://crmsupport.freshworks.com/support/solutions/articles/50000003054-how-to-use-the-activities-dashboard-)
- [Freshsales mobile home](https://crmsupport.freshworks.com/support/solutions/articles/50000002487-how-to-use-the-home-screen-on-the-mobile-app-)
- [Freshsales mobile offline behavior](https://crmsupport.freshworks.com/support/solutions/articles/50000002950-how-to-use-the-mobile-app-offline-)
- [Freshsales global search and filtering](https://crmsupport.freshworks.com/support/solutions/articles/50000008798-how-to-search-and-filter-records-)
- [Freshsales workflow-created tasks](https://crmsupport.freshworks.com/support/solutions/articles/50000003925-how-to-create-tasks-using-workflows-)
- [Freshsales workflow examples and limitations](https://crmsupport.freshworks.com/support/solutions/articles/50000002142-common-use-cases-for-workflows)
- [Freshsales CSV/XLSX import](https://crmsupport.freshworks.com/support/solutions/articles/50000002586-how-to-import-records-contacts-accounts-deals-from-a-csv-xlsx-file-)
- [Freshsales full account export](https://crmsupport.freshworks.com/support/solutions/articles/50000004927-how-do-i-export-all-required-data-from-the-crm-)
- [Freshsales roles and permissions](https://crmsupport.freshworks.com/support/solutions/articles/50000002412-how-to-configure-roles-and-manage-user-permissions-in-freshworks-crm-)
- [Freshsales user deletion](https://crmsupport.freshworks.com/support/solutions/articles/50000002410-how-to-delete-a-user-in-freshworks-crm-)
- [Freshsales audit logs](https://crmsupport.freshworks.com/support/solutions/articles/50000002682-how-to-track-changes-using-audit-logs-)
- [Freshsales REST API](https://developers.freshworks.com/crm/api/)
