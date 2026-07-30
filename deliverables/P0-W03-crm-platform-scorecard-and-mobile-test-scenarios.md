# P0-W03 - CRM Platform Scorecard and Synthetic Mobile Test Scenarios

**Status:** Approved - CP-004 signed off July 30, 2026
**Phase:** Phase 0 - Authority, workflow, and evaluation design
**Updated:** July 30, 2026
**Last signed-off checkpoint:** CP-003

## Work-unit outcome

Approve a weighted CRM platform scorecard and a common set of synthetic mobile test scenarios for comparing Zoho CRM Free, HubSpot Free, and the current Centah-only baseline.

## Reconciled collaborator input

The operational collaborator handoff was reconciled by subject because its simplified mobile questions did not preserve the repository question numbering after LQ-003. The accepted input establishes that:

- Daily phone work should prioritize seeing today's work, finding a client or job, confirming appointments, opening directions, and recording a note.
- Routine mobile actions should take about one minute or less while parked and already signed in.
- The opening view should combine today's appointments, people to call, overdue follow-ups, and jobs waiting on someone else.
- Customer lookup should work well by phone number and last name.
- The minimum quick prospect entry is a name and phone number.
- Meeting administration normally happens back at the office and includes notes, quote work, and a manually sent quote notice.
- Sending quotes, returning calls, and following up after quotes are the most common failure points.
- Helpful reminders include quote not sent, client not contacted, and waiting on customer response.
- Profitability is the desired business outcome; it is a later pilot measure rather than a platform capability by itself.
- Loryn will be the primary administrator and daily user. A second administrator will provide occasional setup, troubleshooting, recovery, and other ad hoc administration.

These inputs are accepted for P0-W03 design. They do not sign off this work unit, approve a platform, or authorize an account, integration, real-data action, purchase, or communication.

## Mandatory pass/fail gates

The following gates were explicitly approved for the P0-W03 draft on July 30, 2026. A platform must pass every applicable gate in an acceptable production tier before weighted preferences can determine the preferred option.

### M-01 - Reliable daily action center

A candidate fails if Loryn cannot open one practical view showing today's appointments, people to contact today, overdue actions, jobs waiting on someone else, and active records missing a next action or due date.

### M-02 - Correct source-specific workflow

A candidate fails if it cannot clearly distinguish `Costco/Centah` from `Independent`, require a unique Centah lead number only for Costco/Centah jobs, show the correct source-specific handoff, and preserve the correct installation-check date for each source.

### M-03 - Essential mobile tasks within one minute

While parked and already signed in, Loryn must be able to complete each of the following in about one minute or less:

- Find a customer by phone number or last name.
- Open today's work.
- Confirm an appointment manually.
- Open driving directions.
- Record a note.

The synthetic test will record elapsed time, screens or taps, repeated typing, and mobile limitations.

### M-04 - Reliable reminders and next actions

A candidate fails if it cannot reliably surface a new client who has not been contacted, a quote that is due or overdue, a sent quote awaiting follow-up, an accepted sale with an incomplete handoff, an installation check or three-month exception, and any active prospect or job without a next action and due date. Reminders may prompt Loryn, but customer communications remain manually reviewed and sent.

### M-05 - Administration and access control

An acceptable production tier must support Loryn as primary administrator, one secondary administrator, multifactor authentication, prompt access removal, appropriate permissions, and preserved activity history for important changes. A free prototype may identify a paid-tier dependency, but a platform fails if no acceptable production tier provides these controls at a reasonable cost.

### M-06 - Data portability and lifecycle control

An acceptable production tier must provide usable exports of customers, prospects, jobs, activities, tasks, notes, dates, statuses, and Centah identifiers; preserve or allow reconstruction of customer-to-job relationships; document retention and deletion capabilities; provide a practical subscription-exit path; and avoid an export process based entirely on manual copying. Exact retention periods remain governed by open decision D-013.

### M-07 - Approved record and lifecycle model

A candidate fails if it cannot represent one reusable customer related to multiple jobs, keep prospecting separate from active jobs while preserving conversion history, implement the approved stages and retained outcomes, store the CP-003 minimum fields, and use required fields or visible exception reporting to uphold the next-action rule. Custom application development cannot be used merely to make a candidate pass.

### M-08 - Human-controlled communications

A candidate fails if it cannot keep calls, texts, and emails manually reviewed and sent; record contact method, permission, and opt-outs; suppress or clearly prevent prohibited outreach reminders; and distinguish an internal reminder from an automatically sent message. Purchased-list imports and automated outreach remain blocked pending compliance review.

### M-09 - Safe Centah/Costco bridge

Until Centah integration options are confirmed, a candidate must support controlled manual entry or import of approved active and sold Costco/Centah jobs, a unique opportunity-level Centah lead number, duplicate detection or reliable duplicate review, separation of Centah-governed identifiers from local fields, and reconciliation that never places independent jobs in Centah. API, webhook, and automated synchronization capabilities remain unverified until D-012 is resolved.

### M-10 - Reliable saving and synchronization

A candidate fails if ordinary mobile or office use can silently lose or duplicate an update. Testing must verify save confirmation, visible pending or failed updates, safe retry without duplicate activity, and consistent information across phone and desktop. Full offline functionality remains a weighted preference unless testing proves it operationally essential.

### M-11 - Verifiable production cost and limits

A candidate cannot pass until the required production tier for two administrators, paid-feature dependencies, record and platform limits, recurring cost, upgrade triggers, and material uncertainties are documented. No hard budget cutoff is approved; cost will be weighted after the mandatory gates pass.

### M-12 - Sustainable learning and administration

A candidate fails the operational trial if essential daily tasks cannot be learned in one guided session, routine use requires duplicate entry within the CRM, ordinary cleanup and administration consistently exceed about 15 minutes per week, or common configuration changes require ongoing technical support. One-time prototype setup is measured separately.

### M-13 - Common synthetic evidence standard

No platform may pass from a feature list or vendor claim alone. Zoho, HubSpot, and the Centah-only baseline must use the same synthetic scenarios and scoring definitions. Every result must record what was tested, device and tier, observed result, supporting evidence, uncertainty, and free-tier, paid-tier, tenant, or Centah limitations. No real customer data, production connection, or customer communication may be used.

## Mandatory-gate result states

Each platform and gate will use one of these states:

- `Pass` - directly verified in the evaluated tier or supported by sufficient authoritative evidence when direct testing is not yet possible.
- `Conditional Pass` - an acceptable production tier appears to satisfy the gate, but a stated tenant, paid-tier, or external dependency remains to be verified.
- `Fail` - the platform cannot satisfy the gate without prohibited custom development or an unacceptable operating compromise.
- `Unverified` - evidence is insufficient; an unverified mandatory gate cannot be treated as passed.
- `Not Applicable` - allowed only with a recorded explanation approved for that platform baseline.

## Approved weighted categories

The following category weights were explicitly approved on July 30, 2026. Mandatory gates override the weighted total: a platform cannot be preferred if an applicable mandatory gate remains `Fail` or `Unverified`.

| Category | Weight | Intended coverage beyond the mandatory minimum |
|---|---:|---|
| Mobile daily-work usability | 35 | Morning-dashboard quality, phone and last-name search, tap and screen count, repeated typing, navigation, and useful offline behavior. |
| Workflow visibility and configuration | 20 | Clarity and flexibility of views, fields, stages, reminders, source-specific prompts, and exception handling. |
| Governance, security, and administration | 15 | Administration quality, permissions, authentication, activity history, access removal, and manageable configuration. |
| Data portability and reliability | 10 | Export quality, relationship preservation, exit practicality, save confidence, synchronization behavior, and recoverability. |
| Cost and maintenance burden | 10 | Required production tier, recurring cost, upgrade triggers, setup effort, training, cleanup, and ongoing support burden. |
| Centah and integration fit | 10 | Manual-bridge usability, external identifiers, duplicate control, reconciliation, and evidence-backed future integration options. |
| **Total** | **100** | |

These weights are accepted design decisions. The scoring scale and criterion-level allocations are defined below; no platform has been scored.

## Approved scoring scale and calculation

Use the same integer scale for every weighted criterion:

| Score | Meaning |
|---:|---|
| 0 | Cannot perform the criterion. |
| 1 | Major weakness or impractical workaround. |
| 2 | Below expectations with material friction. |
| 3 | Meets normal operational needs. |
| 4 | Strong performance with minor friction. |
| 5 | Excellent performance with a clear practical advantage. |

Calculate each contribution as `criterion weight × score ÷ 5`, then add the contributions for a maximum weighted total of 100.

Scoring controls:

- Evaluate mandatory gates before interpreting the weighted score; gates do not become points.
- Require recorded evidence and a confidence label for every score.
- Leave an unverified criterion unscored and report the candidate's total as incomplete.
- Do not normalize a partial score to hide missing evidence.
- Apply the same definitions and criterion weights to Zoho, HubSpot, and the Centah-only baseline.
- Define criteria so they apply to all three candidates. Any exception requires an approved explanation before scoring.

The scale and calculation are accepted design decisions. Criterion-level weights and scenario scripts are defined below; no platform has been scored.

## Approved criterion-level allocation

### Mobile daily-work usability - 35 points

| Criterion | Weight | Scored comparison beyond the mandatory minimum |
|---|---:|---|
| Daily action-center clarity and usefulness | 10 | How quickly Loryn can understand today's appointments, contacts due, overdue work, waiting jobs, and exceptions. |
| Essential mobile-task efficiency | 10 | Relative speed, taps, screens, repeated typing, and clarity after the M-03 one-minute gate is passed. |
| Customer and job search quality | 5 | Phone-number and last-name search speed, tolerance, result clarity, and navigation to the right record. |
| Appointment confirmation and directions workflow | 5 | Ease of reaching the correct contact action and opening the service address in navigation while keeping communication manual. |
| Mobile note capture and weak-signal behavior | 5 | Ease of capturing a note plus useful offline, pending-sync, retry, and weak-connection behavior beyond M-10. |
| **Category total** | **35** | |

This allocation is accepted.

### Workflow visibility and configuration - 20 points

| Criterion | Weight | Scored comparison beyond the mandatory minimum |
|---|---:|---|
| Lifecycle, fields, and customer-to-jobs configuration | 5 | Ease and clarity of implementing the approved records, relationships, stages, fields, conversion history, and retained outcomes. |
| Next-action, reminder, and overdue-work visibility | 5 | Quality and flexibility of tasks, due dates, reminders, missing-next-action detection, and overdue presentation. |
| Source-specific handoff and installation-exception clarity | 5 | Usability of Costco/Centah versus independent prompts, handoff completion, installation anchors, and the three-month exception. |
| Office workflow, activity history, and practical reporting | 5 | Ease of completing notes and quote-related administration, reviewing history, and using reports or views that support daily decisions. |
| **Category total** | **20** | |

This allocation is accepted.

### Governance, security, and administration - 15 points

| Criterion | Weight | Scored comparison beyond the mandatory minimum |
|---|---:|---|
| Secure sign-in, MFA, and account recovery | 4 | Practical account protection and recovery for Loryn without adding unnecessary daily friction. |
| Administrator usability, permissions, and access removal | 4 | Ease of Loryn's full administration and occasional secondary-admin support, including prompt access removal. |
| Activity history, auditability, and accountability | 4 | A usable record of important changes and completed work sufficient to understand what happened. |
| Retention, deletion, and governance documentation | 3 | Clear, usable controls and explanations for retaining, deleting, and administering production data. |
| **Category total** | **15** | |

Apply a proportionality rule to this category: evaluate practical controls for a one-person operation with occasional secondary-admin help. Do not award extra points merely for enterprise role matrices, compliance suites, or elaborate audit tooling that adds no operational value here.

This allocation and proportionality rule are accepted.

### Data portability and reliability - 10 points

| Criterion | Weight | Scored comparison beyond the mandatory minimum |
|---|---:|---|
| Getting all important data out in usable files | 4 | Completeness, clarity, and practical usability of exported records, activities, notes, dates, statuses, and identifiers. |
| Keeping customer-to-job relationships understandable after export | 3 | How well one customer's multiple jobs and their related work remain connected or can be reconstructed. |
| Reliable saving, syncing, retrying, and recovery | 3 | Confidence and ease when saving across phone and desktop, handling failures, retrying safely, and recovering usable information. |
| **Category total** | **10** | |

This allocation is accepted.

### Cost and maintenance burden - 10 points

| Criterion | Weight | Scored comparison beyond the mandatory minimum |
|---|---:|---|
| Actual recurring cost for two administrators and required features | 5 | Expected production subscription cost for the approved access model and every capability needed to pass mandatory gates. |
| Ongoing training, cleanup, and support effort | 3 | Recurring time needed for learning, routine administration, cleanup, troubleshooting, and ordinary configuration changes. |
| Pricing clarity and risk of forced upgrades | 2 | Transparency of tier limits, upgrade triggers, and likely cost changes as normal use grows. |
| **Category total** | **10** | |

This allocation is accepted.

### Centah and integration fit - 10 points

| Criterion | Weight | Scored comparison beyond the mandatory minimum |
|---|---:|---|
| Practical handling of Costco/Centah jobs and lead numbers | 4 | Ease and clarity of working with Costco/Centah records, opportunity-level identifiers, governed-field boundaries, and the approved manual-first approach. |
| Duplicate checking and clear reconciliation | 3 | Quality of duplicate prevention or review and the practical ability to identify and resolve record differences. |
| Evidence-backed future import, export, or API options | 3 | Verified options, limits, support, and upgrade dependencies for a later approved connection; unknown Centah capabilities remain unverified rather than receiving assumed points. |
| **Category total** | **10** | |

This allocation is accepted. All six categories are now allocated across specific criteria totaling 100.

## Approved synthetic scenario areas

Use the same fictional records, starting conditions, and task sequence for Zoho, HubSpot, and the Centah-only baseline.

| ID | Scenario area | Required test coverage |
|---|---|---|
| TS-01 | Quick prospect capture | Add a fictional prospect with name, phone, source, and next action. |
| TS-02 | Morning action center | Find today's appointments, calls, overdue work, waiting jobs, and an active record missing its next action. |
| TS-03 | Costco/Centah lead | Identify the source, handle the opportunity-level Centah number, check for a duplicate, and set the next action. |
| TS-04 | Appointment workflow | Find the client, review the needed details, manually confirm the appointment, and open directions. |
| TS-05 | Visit and quote follow-up | Add notes, track the quote, record the manual quote-sent notice, and schedule the next follow-up. |
| TS-06 | Accepted-sale handoff | Test both Costco/Centah and independent handoff requirements and their source-specific installation anchors. |
| TS-07 | Installation exception | Surface a three-month overdue installation, create or find the same-day coordinator task, and record the result without automatic installation completion. |

These seven scenario areas are accepted. Their synthetic fixtures and exact scripts are defined below.

## Approved synthetic fixture set

Use `T0` as the evaluation day and reset every fixture to its stated starting condition before testing each candidate. All names, phone numbers, email addresses, identifiers, and addresses are fictional test values.

| Fixture | Synthetic identity and starting condition |
|---|---|
| `SYN-PROSPECT-A` | Input card for `Synthetic Prospect Alpha`, phone `+1 202-555-0101`, source `Referral`; the record does not exist before TS-01. |
| `SYN-APPT-B` | `Synthetic Customer Beta`, phone `+1 202-555-0102`, email `beta@example.invalid`, source `Independent`, preferred channel `Text`, appointment on T0, and service address `100 Example Way, Exampleville, NY 00000`. |
| `SYN-COSTCO-C` | `Synthetic Customer Gamma`, source `Costco/Centah`, Centah lead number `SYN-CENTAH-1001`, and first-contact task due on T0; the duplicate-check step attempts the same Centah number on `SYN-COSTCO-C-DUP`. |
| `SYN-QUOTE-D` | `Synthetic Customer Delta`, source `Independent`, quote sent three working days before T0, manual quote-sent notice recorded, and decision follow-up due at 9:00 a.m. on T0. |
| `SYN-HANDOFF-COS-E` | `Synthetic Customer Epsilon`, source `Costco/Centah`, Centah lead number `SYN-CENTAH-1002`, accepted on T0, with DocuSign and coordinator email both incomplete. |
| `SYN-HANDOFF-IND-F` | `Synthetic Customer Zeta`, source `Independent`, accepted on T0, with coordinator email incomplete and no Centah lead number. |
| `SYN-INSTALL-G` | `Synthetic Customer Eta`, source `Costco/Centah`, Centah lead number `SYN-CENTAH-1003`, handoff complete, installation unconfirmed, and coordinator-email date exactly three months before T0. |
| `SYN-QUEUE-H` | `Synthetic Customer Theta`, source `Independent`, active at `Quote Sent - Awaiting Decision`, intentionally missing its next action and due date as a negative test. |

Run TS-02 after 9:00 a.m. on T0 so `SYN-QUOTE-D` is visibly overdue. Use `SYN-APPT-B` for today's appointment, `SYN-COSTCO-C` for today's contact, `SYN-INSTALL-G` for work waiting on another person, and `SYN-QUEUE-H` for missing-next-action detection.

This fixture set is accepted. The step-by-step scripts, timing procedure, and expected results are defined below.

## Approved common execution rules

- Reset every fixture to its approved starting state before testing each candidate.
- Use the same phone and test order for Zoho, HubSpot, and the Centah-only baseline; record the device, operating system, application or browser, candidate tier, and test date.
- Begin each timed mobile action while already signed in. Start timing when the tester begins the stated action and stop when the result is visibly saved or the requested destination is open.
- Record elapsed time, taps, screens, repeated typing, workaround steps, save or error feedback, and any uncertainty.
- Open a manual message composer when the script calls for customer contact, but do not send a message. Open directions when required, but do not begin travel.
- Do not connect email, calendar, maps accounts, Centah, or any other external system. Use only the candidate's unconnected behavior and fictional fixtures.
- Record any deviation from the common steps. Missing or incomparable evidence remains `Unverified`; do not invent a result or normalize an incomplete score.

## Approved participant-burden and staging rule

The seven scenarios are evaluation coverage, not seven separate assignments for Loryn.

### Stage A - Evaluator screening

- The project owner or evaluator screens Zoho, HubSpot, and the Centah-only baseline for mandatory gates, configuration feasibility, quick prospect capture, Costco handling, duplicate behavior, handoff branches, installation exceptions, exports, security, pricing, and integration evidence.
- Stop testing a candidate when a confirmed mandatory failure makes it nonviable, unless a short additional check is needed to document the failure or compare a useful fallback.
- Eliminate nonviable candidates before asking Loryn to test them.

### Stage B - Loryn finalist sessions

- Loryn tests no more than two viable finalists.
- Use one guided session per finalist, capped at about 20 minutes.
- Combine the morning action center, customer search, appointment confirmation, directions, note capture, and quote-follow-up experience in that session.
- The evaluator prepares fixtures, guides the session, records evidence, and handles all technical or administrative checks.
- Loryn receives no independent homework or follow-up test tasks.

The maximum planned burden is two guided sessions, about 40 minutes total, and may be only one session if other candidates fail screening.

## Approved scenario scripts

### TS-01 - Quick prospect capture

1. On the phone, start from the candidate's normal opening screen.
2. Create `SYN-PROSPECT-A` using the approved name, phone number, `Referral` source, next action, and due date.
3. Save the record and confirm that it can be found again.

**Expected result:** The minimum prospect is visibly saved with its source and dated next action, is searchable, and does not require an opportunity or Centah number. Record total time, taps, screens, repeated typing, and any unavailable required field.

### TS-02 - Morning action center

1. Run after 9:00 a.m. on T0 and open the candidate's normal morning or task view.
2. Identify today's appointment from `SYN-APPT-B`, today's contact from `SYN-COSTCO-C`, overdue follow-up from `SYN-QUOTE-D`, work waiting on another person from `SYN-INSTALL-G`, and missing next action on `SYN-QUEUE-H`.
3. Find `SYN-APPT-B` once by phone number and once by last name.

**Expected result:** All five work conditions are available from one practical action center or its approved equivalent, and both searches find the correct record. Record time to understand the queue and each search, plus taps, screens, ambiguity, and missing states.

### TS-03 - Costco/Centah lead handling

1. Open `SYN-COSTCO-C` and identify its source and `SYN-CENTAH-1001` without searching through notes.
2. Attempt to create or import `SYN-COSTCO-C-DUP` with the same Centah lead number.
3. Record the first-contact task and due time.

**Expected result:** The source and opportunity-level identifier are clear, the duplicate is blocked or visibly routed to review, and the dated next action is saved. The identifier must not appear as a reusable customer-level requirement.

### TS-04 - Appointment workflow

1. Find `SYN-APPT-B` and open the appointment.
2. Review the customer name, appointment time, preferred channel, phone number, recent context, and service address without a separate search.
3. Open the manual confirmation composer but send nothing; record the synthetic confirmation result.
4. Open directions to the synthetic service address but do not begin travel.

**Expected result:** The appointment context is easy to reach, customer communication remains manual, the confirmation result is saved, and directions open from the stored address. Time the find, confirmation, and directions actions separately.

### TS-05 - Visit and quote follow-up

1. Using the normal office workflow, add a visit note to `SYN-QUOTE-D`.
2. Record the quoted amount and quote-sent date without attaching or sending a real quote.
3. Record that the fictional manual quote-sent notice was completed; send nothing.
4. Confirm or create the decision follow-up due three working days after quote send.

**Expected result:** The note, quote facts, manual notice, and dated follow-up are visible in the job history. A missed due time becomes visibly overdue and does not disappear or silently reschedule.

### TS-06 - Accepted-sale handoff

1. Open `SYN-HANDOFF-COS-E`; verify that DocuSign and coordinator email are both required and that handoff cannot be marked complete after only one item.
2. Record both fictional items as completed and confirm that the six-week installation anchor uses the DocuSign-sent date.
3. Open `SYN-HANDOFF-IND-F`; verify that coordinator email is required, DocuSign is not required, and no Centah lead number is requested.
4. Record the fictional coordinator email as completed and confirm that the six-week anchor uses the coordinator-email date.
5. Confirm that both branches retain the coordinator-email date for the three-month boundary.

**Expected result:** Each source shows only its approved handoff requirements, prevents premature completion, and produces the correct installation dates without false Centah fields on the independent job.

### TS-07 - Installation exception

1. Open the morning action center and locate the three-month exception for `SYN-INSTALL-G`.
2. Open or create the same-day task to contact the coordinator.
3. Record the fictional result `Installation still unconfirmed`.
4. Verify that customer contact is prompted and that the job remains unconfirmed until a person records installation confirmation.

**Expected result:** The exception is difficult to miss without repetitive automatic customer messages, the coordinator result is retained, the next action is explicit, and the system never marks installation complete from elapsed time alone.

These execution rules, scripts, and participant-burden limits are accepted. The evidence-record format and completed acceptance review follow.

## Approved evaluator evidence record

The evaluator, not Loryn, completes the evidence record.

### Test-run header

Record once for each candidate and run:

- Candidate and evaluated tier.
- Test date and evaluator.
- Phone or desktop, operating-system version, and application or browser version.
- Confirmation that the approved fixtures were reset before the run.

### Result row

Use one compact row for each mandatory gate or scored criterion:

| ID | Result or score | Time or friction | Evidence reference | Limitation or uncertainty | Confidence |
|---|---|---|---|---|---|
| Gate or criterion ID | Mandatory result state or score `0`-`5` | Relevant elapsed time, taps/screens, repeated typing, or workaround | Synthetic screenshot, export, observed setting, or official exact-tier documentation | Free/paid-tier or tenant limit, deviation, unresolved dependency, or uncertainty | `High`, `Medium`, or `Low` |

Confidence definitions:

- `High` - directly observed and repeatable.
- `Medium` - observed once or supported by exact-tier official documentation with a stated caveat.
- `Low` - indirect or incomplete evidence; any total remains provisional.
- `Unverified` is a result state, not a confidence level; assign no score.

Evidence controls:

- Keep candidate and device details in the header rather than repeating them in every row.
- Use mandatory result states for gates and the approved 0-5 scale for weighted criteria.
- Reference evidence rather than embedding sensitive or verbose material in the row.
- Record every free-tier, paid-tier, tenant, Centah, device, or test-condition limitation that could change the result.
- Use only synthetic fixture values in screenshots and exports. Exclude or redact credentials, account identifiers, personal notifications, and unrelated private information.
- A low-confidence or incomplete result cannot support final platform selection until the stated uncertainty is resolved.

This evaluator-only evidence format is accepted.

## Acceptance review

- [x] Mandatory pass/fail requirements are separate from weighted preferences.
- [x] Six category weights and twenty-two criterion weights total 100 and cover mobile daily-work value, workflow configuration, governance, portability, cost, and integration fit.
- [x] Zoho, HubSpot, and the Centah-only baseline use the same gates, criteria, scoring definitions, fixtures, scripts, and evidence standard.
- [x] TS-01 through TS-07 cover prospect capture, Costco lead handling, appointment confirmation, quote follow-up, accepted-sale handoff, installation exception, and daily queue use.
- [x] Every gate and score requires evidence, confidence, limitations, and uncertainty; missing evidence remains `Unverified` and is never normalized away.
- [x] Fixtures and scripts use fictional data and prohibit credentials, private payloads, real customer records, external connections, actual messages, and travel actions.
- [x] Evaluator screening occurs before no more than two guided Loryn finalist sessions of about 20 minutes each, with no homework.

## CP-004 approval effect

CP-004 approves the P0-W03 evaluation method: mandatory gates, weights, scoring rules, synthetic fixtures and scripts, evidence format, and participant-burden limit. Phase 1 may rely on this method when a separate work-unit contract and any required trial-account authorization are approved. CP-004 does not select a platform, approve a production tenant, authorize a trial account, connect an external system, permit real data, or authorize customer communication.

## Approval boundary

M-01 through M-13, the complete 100-point scorecard, common scoring rule, TS-01 through TS-07, the eight-fixture synthetic dataset, exact scripts, evaluator evidence format, and staged participant-burden limit are approved at CP-004. Platform scores, trial accounts, external connections, production-data use, and final platform selection remain unapproved.
