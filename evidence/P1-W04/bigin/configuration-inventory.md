# P1-W04 Bigin Premier Configuration Inventory

**Status:** Approved at CP-008 as the signed Bigin Premier configuration inventory

**Configured:** August 1, 2026

## Boundary

This inventory records only the sanitized synthetic evaluator configuration in the `Hazel Kaine` Bigin Premier trial. It contains no credentials, account identifiers, private email addresses, real customer data, billing details, external connections, or customer communications.

D-103 authorized the bounded configuration, synthetic fixtures, evaluator scenarios, mobile timing, export evidence, and narrow cleanup defined by the D-101 contract. The run stopped when direct evidence confirmed the M-01 morning-action-center failure. D-103 did not authorize billing, a paid commitment, external connections, real data, customer communication, production use, Loryn participation, checkpoint sign-off, or platform selection.

## Verified starting state and sample cleanup

- Premier remained active with 15 trial days shown and no billing prompt.
- The single vendor sample Pipeline record, its linked sample Contact, and its linked sample Company were verified as vendor samples and moved to Bigin's recycle bin.
- Active Pipeline, Contact, Company, Product, and Activity views then showed no records.
- The recycle bin was not emptied. No permanent deletion was performed.

## Configured data model

- Team Pipeline: `Window Sales Work`
- Record labels: `Opportunities` and `Opportunity`
- Contact custom fields: 10 of the documented 25-field Premier allowance.
- Pipeline custom fields: 14 of the documented 25-field Premier allowance, plus standard `Lead Source`.
- Task custom fields: none.
- Events and Tasks use standard Bigin fields.
- Contacts are reusable and each synthetic opportunity links to one Contact.
- One Team Pipeline contains two source routes. The system-retained `Window Sales Work Standard` sub-pipeline is the Independent route; `Costco / Centah` is the Costco route.

### Contact fields

- Prospect state
- Preferred contact method
- Acquisition source
- Acquisition date
- Contact permission status
- Overall DNC status
- DNC date
- DNC reason
- Channel opt-outs
- Unresolved problem

The preferred-contact picklist was corrected after the first direct fixture exposed that `Text` had been omitted. `Text` was added and read back on the synthetic Beta contact.

### Pipeline fields

- Service address
- Standard Lead Source
- Source detail
- Centah lead number, configured as unique with duplicate prevention enabled
- Last-contact date/time
- Quote-sent date/time
- Acceptance date/time
- DocuSign-sent date/time
- Coordinator-email date/time
- Installation-confirmed date/time
- Post-install follow-up date/time
- Installation status
- Post-install result
- Close outcome/reason
- Exception/stall reason

Picklists retain the approved installation exception, post-install results, and finish/loss outcomes. Direct configuration corrected the preflight count from 15 custom Pipeline fields to 14 because `Lead Source` is standard.

## Configured stages

Both source routes use these open stages:

1. `New Customer Request`
2. `Trying to Contact`
3. `Appointment Scheduled`
4. `Appointment Completed`
5. `Preparing Quote`
6. `Quote Sent - Awaiting Decision`
7. `Customer Accepted - Handoff Due`
8. `Handoff Complete - Installation Pending`
9. `Installed - Customer Follow-Up Due`

The retained successful close stage is `Finished`. Bigin's correct native loss state is labeled `Closed Lost`; this is the evaluated platform-label variance for the approved `Lost / Canceled` exit. An attempted custom `Lost / Canceled` stage carried won semantics and was not used.

## Stage Transition Rules

The following rules were saved and directly prompted for their configured fields:

| Source route | Transition | Required fields |
|---|---|---|
| Costco / Centah | Customer Accepted - Handoff Due -> Handoff Complete - Installation Pending | Centah lead number; DocuSign-sent date/time; Coordinator-email date/time |
| Independent (`Window Sales Work Standard`) | Customer Accepted - Handoff Due -> Handoff Complete - Installation Pending | Coordinator-email date/time only |
| Costco / Centah | Handoff Complete - Installation Pending -> Installed - Customer Follow-Up Due | Installation-confirmed date/time |
| Costco / Centah | Installed - Customer Follow-Up Due -> Finished | Post-install follow-up date/time; Post-install result; Close outcome/reason |

The Costco and Independent handoff prompts were opened and canceled after verification. The Independent prompt did not request DocuSign or Centah. The installation transition prompted for installation confirmation and did not silently bypass the rule.

Closure Restriction was inspected but not configured because a broad restriction would also interfere with legitimate early `Closed Lost` exits. Premature `Finished` closure outside the tested transition path remains unverified.

## Synthetic fixture state

Seven reusable synthetic Contacts and seven linked Opportunity records were saved:

| Fixture | Route | Stage | Purpose |
|---|---|---|---|
| `SYN-APPT-B` | Independent | Appointment Scheduled | Today's appointment and search fixture |
| `SYN-COSTCO-C` | Costco / Centah | New Customer Request | First-contact and Centah identifier fixture |
| `SYN-QUOTE-D` | Independent | Quote Sent - Awaiting Decision | Overdue quote-follow-up fixture |
| `SYN-HANDOFF-COS-E` | Costco / Centah | Customer Accepted - Handoff Due | Costco handoff enforcement fixture |
| `SYN-HANDOFF-IND-F` | Independent | Customer Accepted - Handoff Due | Independent handoff enforcement fixture |
| `SYN-INSTALL-G` | Costco / Centah | Handoff Complete - Installation Pending | Three-month installation exception fixture |
| `SYN-QUEUE-H` | Independent | Quote Sent - Awaiting Decision | Intentional missing-next-action fixture |

One malformed but blank synthetic Epsilon Contact created during a timing race was verified as containing no contact information and moved to the recycle bin. The intended full Epsilon fixture remains active. No real data was entered.

## Activities and time behavior

- Task `SYN-COSTCO-C - First contact`, due August 1, 2026.
- Task `SYN-QUOTE-D - Decision follow-up`, due July 31, 2026, deliberately overdue.
- Task `SYN-INSTALL-G - Coordinator check`, due August 1, 2026.
- Event `SYN-APPT-B - In-home appointment`, August 1, 2026 from 6:00 p.m. to 7:00 p.m., with a 15-minute reminder and synthetic location.
- The Tasks dashboard directly showed 3 created, 3 open, and 1 overdue task.
- Standard Task Due Date is date-only. A reminder can carry an on-due-date time, but it must be in the future. Events support start and end times.
- The evaluator calendar treated Saturday as outside working days even though the approved operating schedule includes Saturday 9:00 a.m. to 2:00 p.m. Calendar-business-hour correction was not attempted after the stopping rule fired.

## Direct duplicate and search evidence

- A manual attempt to save `SYN-COSTCO-C-DUP` with the existing synthetic `SYN-CENTAH-1001` value was blocked with Bigin's same-Centah-number duplicate message. The unsaved duplicate form was discarded, and the original route still showed one New Customer Request record.
- Global search by the synthetic Beta phone number returned the correct Contact.
- Global search by last name `Beta` returned the same Contact.
- Import duplicate behavior was not tested before the stopping rule fired.

## Morning-action-center stopping result

- Bigin's default Tasks dashboard exposed aggregate counts, including the one overdue task.
- The custom dashboard builder offered KPI, Chart, and Target Meter components. The inspected KPI builder could count one module with date duration and criteria, but no actionable record-list component was available.
- Pipeline saved views are scoped to the selected source sub-pipeline. The Independent list showed four records while Costco/Centah remained on a separate tab.
- Pipeline custom-view criteria exposed Pipeline fields such as Stage, Sub-Pipeline, Last Activity Time, installation fields, and exception reason. It did not expose a next-activity field or a condition for an active Pipeline record with no linked Task.
- Consequently, `SYN-QUEUE-H` cannot be detected reliably as missing its next action from the same practical screen that shows the other four TS-02 conditions. The dashboard can show counts, and module/source views can show records, but the evaluated Premier configuration cannot combine the five named actionable records in one practical action center.
- This directly fails M-01 and also leaves the M-04/M-07 next-action invariant unsupported. The signed stopping rule ended mobile timing, export, import-duplicate, administrator-removal, and later scenario work.

## Cleanup and handoff state

- Vendor samples and the malformed blank synthetic Contact remain recoverable in the recycle bin.
- The blocked duplicate Opportunity was never saved.
- Seven baseline synthetic Contacts, seven synthetic Opportunities, three Tasks, one Event, the saved fields, source routes, stages, and transition rules remain in the evaluator tenant as evidence.
- No dashboard or custom-view draft from the final M-01 inspection was saved.
- No external connection, add-on, billing detail, paid commitment, real data, customer communication, production action, Loryn participation, checkpoint sign-off, or platform selection occurred.

## Approved result boundary

CP-008 approves the `Eliminated` result for Bigin Premier because M-01 fails directly. It approves this inventory and the linked evaluator evidence only; it does not authorize another candidate, account, billing, production use, integration, real data, customer communication, or Loryn testing.
