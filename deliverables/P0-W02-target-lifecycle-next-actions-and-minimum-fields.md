# P0-W02 - Target Lifecycle, Next Actions, and Minimum CRM Fields

**Status:** Awaiting CP-003 sign-off

**Phase:** Phase 0 - Authority, workflow, and evaluation design

**Updated:** July 29, 2026

## Work-unit outcome

Approve the connected prospecting and active-job lifecycles, the next action required at every active stage, and the minimum CRM information needed to operate the workflow without relying on memory, email searches, or text history.

## Plain-language record model

- A **customer record** represents one reusable person or business.
- A **prospect** represents possible future work that has not reached an active project.
- An **opportunity or job** represents one specific window-covering project or order. One customer may have several jobs over time.
- A **task or activity** records what must happen or what already happened.
- A Centah lead number belongs to a Costco/Centah job, never to the reusable customer record.

## Prospect-to-job conversion

A prospect becomes an active job only when a real project is confirmed and the initial appointment is scheduled. Close the prospecting sequence as `Converted`, retain the customer and prospecting history, create one job for that project at `Appointment Scheduled`, and make the morning-of confirmation its next action. A direct inquiry about an immediate project may enter the active-job workflow without first using prospecting.

## Approved active-job stages and next actions

| Stage | What it means | Required next action or exit |
|---|---|---|
| `New Customer Request` | A current-project request has arrived. | Make the first manual contact attempt by closing time if received during calling hours, or at 9:00 a.m. on the next working day if received outside them. |
| `Trying to Contact` | The first attempt received no answer. | Retry on the next working day, then make a third and final attempt two working days later. After a third nonresponse, close as `Lost / Canceled - No Response`. |
| `Appointment Scheduled` | The initial appointment is booked. | At approximately 7:45 a.m. on the appointment day, manually send the confirmation text. A requested phone confirmation must wait until 9:00 a.m. |
| `Appointment Completed` | The visit occurred and its result must be recorded. | If a quote is needed, move to `Preparing Quote` and make the quote due by the end of the same working day. Otherwise record an explicit next action or close with a retained outcome. |
| `Preparing Quote` | The quote is being prepared. | Send it by the same-day target. If missed, record a short reason and set the fallback deadline to the end of the next working day. Missed fallbacks remain overdue and require a deliberate new date and reason. |
| `Quote Sent - Awaiting Decision` | The quote was emailed and the customer has not decided. | Immediately send a manual message asking the customer to check their email. Follow up three working days later, then weekly for up to three weeks. Use a customer-requested date instead when supplied. After the third weekly nonresponse, close as `Lost / Canceled - No Decision`. |
| `Customer Accepted - Handoff Due` | The customer said yes but the internal handoff is incomplete. | Finish the source-specific handoff by the end of that working day, or by 9:00 a.m. the next working day after an outside-hours acceptance. |
| `Handoff Complete - Installation Pending` | Every required handoff item was sent. | Check installation six weeks after the source-specific anchor. If unconfirmed, record a note and check again in two to three weeks. At three months, create the approved urgent exception and same-day escalation. |
| `Installed - Customer Follow-Up Due` | A person confirmed installation. | Perform one manual customer follow-up by the end of the next working day and record `Satisfactory`, `Problem Reported`, or `No Response`. |
| `Finished` | Installation and the one post-install follow-up requirement are complete. | No active-job task is required. Create the six-month past-customer prospecting reminder only when the customer is eligible. |
| `Lost / Canceled` | The active job ended without a sale or was canceled. | Require a retained outcome such as `No Response`, `No Decision`, `Declined`, `Customer Canceled`, `Invalid Information`, or `Duplicate`; no active-job task is required. |

## Calling and communication rules

- Calling hours are Monday through Friday, 9:00 a.m. to 6:00 p.m., and Saturday, 9:00 a.m. to 2:00 p.m.
- Sunday work rolls to Monday at 9:00 a.m. unless that day is configured as unavailable.
- Approximately 7:45 a.m. is a limited exception for manual same-day appointment-confirmation texts.
- All customer communications remain human-reviewed and manually sent.
- Use the customer's preferred and permitted channel and honor overall and channel-specific opt-outs.

## Source-specific accepted-sale handoff

| Source | Items required before handoff is complete | Installation-check anchor |
|---|---|---|
| Costco/Centah | Send DocuSign and email the quote to the internal order coordinator. | DocuSign-sent date |
| Outside Costco/Centah | Skip DocuSign and email the quote to the internal order coordinator. | Coordinator-email date |

The three-month overdue-installation boundary is measured from the date the sold quote was emailed to the internal order coordinator for both sources.

## Installation and post-install outcomes

- Never mark installation complete without human confirmation.
- At three months without confirmation, show an urgent exception, contact the coordinator that day, record the result, and contact the customer if the coordinator cannot confirm installation.
- `Satisfactory`: mark `Finished` and schedule the six-month past-customer reminder when eligible.
- `Problem Reported`: keep the job at `Installed - Customer Follow-Up Due`, flag the unresolved problem, and require a next action. Detailed repair-case management remains outside the first release.
- `No Response`: record `Post-Install Follow-Up Attempted - No Response`, mark the confirmed-installed job `Finished`, and schedule the six-month reminder only when there is no opt-out or known unresolved problem.

## Minimum CRM field set

### Customer or contact

| Field | Requirement |
|---|---|
| Display name | Required; may be a person, business, or social identity. |
| Reachable channel or location | At least one of phone, email, social handle, or address is required for an active prospect. |
| Prospect state | Required when used in prospecting: `Active`, `Long-Term Nurture`, `Converted`, `Archived`, or `Do Not Contact`. |
| Preferred contact method | Required before routine follow-up. |
| Acquisition source and date | Required; records how and when the information was obtained. |
| Contact-permission status | Required: `Unknown`, `Directly Provided`, `Existing Relationship`, or `Opted Out`. |
| Overall do-not-contact status, date, and reason | Required when applicable. |
| Channel-specific opt-outs | Required when applicable. |
| Unresolved-problem indicator | Required when a known problem blocks promotional follow-up. |

### Opportunity or job

| Field | Requirement |
|---|---|
| Linked customer | Required. |
| Service address | Required for an active job. |
| Lead source and source detail | Source required; detail required when needed to identify the referral, builder, event, campaign, social platform, list, business, or Costco context. |
| Centah lead number | Required and unique only for Costco/Centah jobs; prohibited for independent jobs. |
| Current stage | Required. |
| Last-contact date and time | Required after the first contact activity. |
| Next action and due date/time | Required for every active stage unless an approved exception is recorded. |
| Appointment date and time | Required once scheduled. |
| Quoted amount and quote-sent date | Required once the quote is sent. Detailed quote-file storage remains deferred. |
| Acceptance date | Required when accepted. |
| DocuSign-sent date | Required only for accepted Costco/Centah jobs. |
| Coordinator-email date | Required for every accepted job. |
| Installation status and confirmed date | Required after handoff; confirmed date requires human verification. |
| Post-install follow-up date and result | Required after confirmed installation. |
| Close outcome or reason | Required for `Finished` and `Lost / Canceled`. |
| Exception or stall reason | Required whenever the normal next-action rule is overridden or the job is visibly stalled. |

### Task or activity

| Field | Requirement |
|---|---|
| Linked customer and job | Customer required; job also required when the task or activity concerns an active job. |
| Activity or task type | Required. |
| Due date/time and status | Required for a task. |
| Completed date/time | Required when completed. |
| Result or note | Required when an activity is completed. |

## Sanitized validation walkthroughs

### A. Independent prospect converts into a job

1. Create `SYN-PROSPECT-001` for `Synthetic Customer Alpha`, source `Referral`, reachable at `alpha@example.invalid`, with a next action and date.
2. Record a real-project confirmation and schedule the initial appointment.
3. Close the prospect sequence as `Converted`; preserve the referral source and activities.
4. Create `SYN-OPP-IND-001` at `Appointment Scheduled` with no Centah lead number and a 7:45 a.m. confirmation-text task.
5. Complete the appointment, set the same-day quote deadline, email the quote, and send the immediate manual check-your-email notice.
6. Record customer acceptance. Skip DocuSign, email the quote to the internal order coordinator, and move to `Handoff Complete - Installation Pending`.
7. Create the six-week installation check from the coordinator-email date.
8. Record human-confirmed installation, perform the next-working-day customer follow-up, mark `Finished`, and create the eligible six-month past-customer reminder.

**Result:** The independent path traverses prospect conversion through closure without a Centah identifier and always has a next action while active.

### B. Costco/Centah job follows the governed source branch

1. Create `SYN-OPP-COS-001` for `Synthetic Customer Beta`, source `Costco/Centah`, with unique external reference `SYN-CENTAH-001`.
2. Start at `New Customer Request` with a dated first-contact task.
3. Schedule and confirm the appointment, complete it, and send the quote using the approved same-day target and follow-up sequence.
4. Record customer acceptance. Send DocuSign and email the quote to the internal order coordinator; do not mark handoff complete until both are recorded.
5. Create the six-week installation check from the DocuSign-sent date and retain the coordinator-email date for the three-month boundary.
6. If installation is still unconfirmed at three months, create the urgent same-day coordinator task and require a recorded result before any stage change.
7. After human-confirmed installation, perform the one post-install follow-up and record the applicable closure outcome.

**Result:** The Costco path enforces its opportunity-level Centah identifier, source-specific handoff, dated installation check, three-month exception, and human verification.

## Acceptance review

- [x] Every meaningful prospect and job state has one defined stage or explicit outcome.
- [x] Every active prospect and job has a next action and due date or an approved exception.
- [x] Contact attempts, consultation, quote, accepted sale, canceled/lost outcomes, installation checks, the three-month exception, post-install follow-up, and past-customer re-entry are represented.
- [x] Minimum fields are assigned to customer, job, and task/activity records and are limited to information used by the workflow.
- [x] Centah lead number is required and unique only for Costco/Centah jobs and is prohibited for independent jobs.
- [x] Sanitized examples traverse independent prospect conversion and the Costco/Centah path without relying on memory or text history.
- [x] No CRM account was created, no integration was connected, no customer communication was sent, and no real customer data was used.

## CP-003 approval effect

CP-003 sign-off will allow the project to rely on this lifecycle, next-action rule set, and minimum field set when creating synthetic fixtures, platform scorecards, mobile test scenarios, and CRM prototypes. It will not authorize production accounts, real-data imports, external integrations, automated communications, purchases, or deployment.
