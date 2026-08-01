# P1-W04 Bigin Premier Field-Capacity Preflight

**Status:** Direct field configuration approved at CP-008

**Mapped:** August 1, 2026

## Result

The CP-003 model was directly configured within Bigin Premier's documented limit of 25 custom fields per module without add-ons: 10 Contact fields, 14 custom fields in `Window Sales Work` plus standard `Lead Source`, and no Task custom fields. Events use documented default fields. The counts are module-specific and are not added into one shared allowance.

Direct configuration corrected the Pipeline estimate from 15 custom fields to 14 because standard `Lead Source` is available. It also confirmed that standard Task Due Date is date-only; a reminder may carry an on-due-date time, while Events retain start and end times. Mobile visibility, completion timestamp export, import behavior, and relationship reconstruction remain unverified because the M-01 stopping rule ended the run.

## Approved evaluated record model

- Contacts are reusable people, businesses, or social identities and may begin as prospects.
- Activities hold calls, tasks, and appointments linked to Contacts and, after conversion, to Pipeline records.
- A confirmed project creates one Pipeline record linked to the reusable Contact. A returning customer may therefore have multiple Pipeline records.
- One Team Pipeline is preferred so fields and the action center remain unified. Costco/Centah and Independent sub-pipelines are permitted only if direct inspection proves they can use different stage controls without fragmenting daily work.

## Contact mapping

| CP-003 need | Proposed Bigin mapping | Custom count |
|---|---|---:|
| Display name | Standard First Name and Last Name; Company record only when a business identity is useful | 0 |
| Reachable phone, email, social identity, or address | Standard email, mobile/work/home phone, mailing address, and documented social profiles | 0 |
| Prospect state | Custom single-select: `Active`, `Long-Term Nurture`, `Converted`, `Archived`, `Do Not Contact` | 1 |
| Preferred contact method | Custom single-select | 1 |
| Acquisition source and date | Custom single-select source plus custom date | 2 |
| Contact-permission status | Custom single-select | 1 |
| Overall do-not-contact status, date, and reason | Custom checkbox, date, and multiline text; standard Email Opt Out remains channel-specific only | 3 |
| Channel-specific opt-outs | Custom multi-select | 1 |
| Unresolved-problem indicator | Custom checkbox | 1 |
| **Contact total** |  | **10** |

## Pipeline mapping

| CP-003 need | Proposed Bigin mapping | Custom count |
|---|---|---:|
| Linked customer | Standard Related Contacts lookup | 0 |
| Service address | Custom single-line text; direct mobile directions test is mandatory | 1 |
| Lead source and source detail | Standard Lead Source plus custom single-line text | 1 |
| Centah lead number | Custom single-line text marked unique; Costco/Centah only | 1 |
| Current stage | Standard Team Pipeline, sub-pipeline, and stage | 0 |
| Last-contact date and time | Custom date-and-time | 1 |
| Next action and due date/time | Standard linked Task, Event, or Call; direct missing-next-action and timing proof required | 0 |
| Appointment date and time | Standard Event From/To date and time | 0 |
| Quoted amount | Standard Amount | 0 |
| Quote-sent date and time | Custom date-and-time | 1 |
| Acceptance date and time | Custom date-and-time | 1 |
| DocuSign-sent date and time | Custom date-and-time; Costco/Centah only | 1 |
| Coordinator-email date and time | Custom date-and-time; every accepted job | 1 |
| Installation status and confirmed date/time | Custom single-select plus custom date-and-time | 2 |
| Post-install follow-up date/time and result | Custom date-and-time plus custom single-select or multiline text | 2 |
| Close outcome or reason | Custom single-select; stage provides open/closed state | 1 |
| Exception or stall reason | Custom multiline text that remains filterable; do not use a large multiline type if filtering is unavailable | 1 |
| **Pipeline total** |  | **14** |

## Activity mapping

| CP-003 need | Proposed Bigin mapping | Custom count |
|---|---|---:|
| Linked customer and job | Standard Related To link to Contact and Pipeline record | 0 |
| Activity or task type | Standard Task, Event, or Call modules plus subject/title | 0 |
| Due date/time and status | Standard Task Due Date and Status; Due Date is date-only, while Reminder may carry an on-due-date time; one custom date-and-time remains a possible but untested correction | 0-1 |
| Completed date/time | Use system activity/timeline timestamp if directly exportable; otherwise one custom date-and-time on Tasks | 0-1 |
| Result or note | Standard Task Description or Call Outcome/Result; direct completion enforcement test required | 0 |
| **Task contingency total** |  | **0-2** |

Events and Calls have their own documented default date/time and outcome fields. Any direct correction must remain within the relevant module's Premier limit and map to an approved CP-003 requirement.

## Capacity summary

| Module | Conservative custom-field use | Premier documented limit | Headroom |
|---|---:|---:|---:|
| Contacts | 10 | 25 | 15 |
| `Window Sales Work` Team Pipeline | 14 | 25 | 11 |
| Tasks | 0-2 | 25 | 23-25 |
| Events | 0 | 25 | 25 |
| Calls | 0 | 25 | 25 |

The `Centah lead number` uses one of the two documented custom unique fields available per module. No other custom unique field is currently required in the Pipeline module.

## Mandatory controls that capacity does not prove

- Stage Transition Rules must conditionally require the Centah identifier and DocuSign only for Costco/Centah, require the coordinator email for both sources, and prevent premature closure.
- The same Team Pipeline preserved reusable Contacts and source-specific transition rules, but separate sub-pipeline tabs fragmented record lists. Dashboard components exposed aggregates rather than actionable record lists, and Pipeline views could not filter for records with no linked next Task. This directly failed M-01 in the evaluated configuration.
- The unique Centah field must prevent or visibly route duplicates during both manual entry and import; case-insensitive matching is documented but direct behavior remains required.
- Contact-only prospects must support the approved next-action rule and convert into one linked project without losing activities or duplicating the customer. This remained unverified after the M-01 stopping rule fired.
- Task due time, completed timestamp, result enforcement, mobile address-to-directions behavior, and export relationship reconstruction remain unverified direct-test items.
- The eleven-field Pipeline headroom is not permission to add scope. Adding duplicated next-action fields would not resolve the directly observed separation of source record lists and absence of dashboard record-list components.

## Official sources

- [Bigin modules and custom-field limits](https://help.zoho.com/portal/en/kb/bigin/customization/articles/modules-and-fields)
- [Bigin default fields by module](https://help.zoho.com/portal/en/kb/bigin/customization/articles/default-fields-bigin)
- [Bigin custom and unique fields](https://help.zoho.com/portal/en/kb/bigin/modules/pipelines/articles/add-custom-fields-9-2-2019)
- [Bigin Team Pipelines](https://help.zoho.com/portal/en/kb/bigin/team-pipelines/articles/team-pipelines)
- [Bigin Pipeline records](https://help.zoho.com/portal/en/kb/bigin/modules/pipelines/articles/pipeline-records)
- [Bigin Stage Transition Rules](https://help.zoho.com/portal/en/kb/bigin/automation/articles/stage-transition-rules)
- [Bigin import and unique-field behavior](https://help.zoho.com/portal/en/kb/bigin/data-administration/articles/import-records)
