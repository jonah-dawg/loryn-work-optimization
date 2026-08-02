# P1-W06 Less Annoying CRM Field-Model Preflight

**Status:** Approved contract input; public demo confirmed field controls but M-01 stopped the run under D-112 before configuration or tenant confirmation

**Mapped:** August 1, 2026

## Result

The CP-003 model fits LACRM's documented unlimited custom-field boundary. The proposed minimum uses 8 Contact custom fields, 7 Prospecting pipeline fields, and 20 Window Sales Work pipeline fields. Standard Contact fields hold identity, phone, email, and address; standard pipeline status holds lifecycle position; Tasks and Events hold reminders and timed appointments.

Field quantity does not establish viability. LACRM Tasks are documented with an optional `ContactId` and no `PipelineItemId`, while one Contact may hold multiple active pipeline items. The proposed model therefore keeps `Next action` and `Next action due` on each pipeline item as the canonical state. Any Task is a Contact-linked reminder labeled with the pipeline-item name. Direct evidence must prove that this design supports a practical missing-action view without routine duplicate entry.

## Proposed record model

- A Contact is the reusable person, company, or reachable prospect identity.
- A `Prospecting` pipeline item represents one pre-project prospecting thread and preserves its activity after conversion or closure.
- A `Window Sales Work` pipeline item represents one project or order. A returning customer may have multiple active or historical items.
- A successful prospecting conversion creates a linked Window Sales Work item without replacing the Contact or deleting prospect history.
- Tasks and Events remain Contact-scoped. Their titles must begin with the related pipeline-item label until direct evidence proves a native item-level link.

## Contact mapping

| CP-003 need | Proposed LACRM mapping | Custom count |
|---|---|---:|
| Display name and optional company | Standard Contact/Company name | 0 |
| Phone, email, and address | Standard Contact fields | 0 |
| Preferred contact method | Custom dropdown | 1 |
| Acquisition date | Custom date | 1 |
| Contact-permission status | Custom dropdown | 1 |
| Overall do-not-contact date and reason | Custom date plus text area | 2 |
| Channel-specific opt-outs | Custom checkbox list | 1 |
| Social identity or profile reference | Custom text box | 1 |
| Unresolved-problem indicator | Custom radio list | 1 |
| **Contact total** |  | **8** |

## Prospecting pipeline mapping

| CP-003 need | Proposed LACRM mapping | Custom count |
|---|---|---:|
| Prospect lifecycle | Standard Prospecting pipeline status | 0 |
| Prospect source | Custom dropdown | 1 |
| Source detail or referrer | Custom text box | 1 |
| Last-contact date | Custom date | 1 |
| Next action | Custom text box | 1 |
| Next action due | Custom date | 1 |
| Waiting on or exception reason | Custom text area | 1 |
| Conversion or close outcome | Custom dropdown | 1 |
| **Prospecting total** |  | **7** |

## Window Sales Work pipeline mapping

| CP-003 need | Proposed LACRM mapping | Custom count |
|---|---|---:|
| Distinct job label shown on pipeline badge | Custom text box with badge display enabled | 1 |
| Current job lifecycle | Standard Window Sales Work pipeline status | 0 |
| Service address | Custom text box; mobile directions behavior requires direct proof | 1 |
| Work source | Custom dropdown: `Costco/Centah` or `Independent` | 1 |
| Lead-source detail | Custom text box | 1 |
| Centah lead number | Custom text box; uniqueness and review behavior unverified | 1 |
| Last-contact date | Custom date | 1 |
| Next action | Custom text box | 1 |
| Next action due | Custom date | 1 |
| Waiting on | Custom dropdown | 1 |
| Appointment | Contact-linked Event whose title begins with job label; no pipeline field unless direct proof requires one | 0 |
| Quoted amount | Custom currency | 1 |
| Quote-sent date | Custom date | 1 |
| Acceptance date | Custom date | 1 |
| DocuSign-sent date | Custom date | 1 |
| Coordinator-email date | Custom date | 1 |
| Installation status and confirmed date | Custom dropdown plus date | 2 |
| Post-install follow-up date and result | Custom date plus dropdown | 2 |
| Close outcome | Custom dropdown | 1 |
| Exception or stall reason | Custom text area | 1 |
| **Window Sales Work total** |  | **20** |

## Activity and reminder mapping

| CP-003 need | Proposed LACRM mapping | Direct proof required |
|---|---|---|
| Dated action reminder | Contact-linked Task; title begins with pipeline-item label | Task remains distinguishable across two jobs and aligns with canonical pipeline fields |
| Timed appointment or confirmation | Contact-linked Event; title begins with pipeline-item label | Exact time, phone visibility, rescheduling, reminder, and mobile behavior |
| Completed action | Task completion record | Completion timestamp and export relationship are retained |
| Notes and outcome | Contact note plus job label, or pipeline-item field where structured state is required | Notes and structured outcomes remain reconstructable per job |

## Source-specific control design

- `Work source` is the visible branch selector.
- `Centah lead number` and `DocuSign-sent date` apply only to `Costco/Centah` items.
- `Coordinator-email date` applies to both accepted-sale branches.
- `Installation confirmed date` applies only when `Installation status` is `Confirmed`.
- `Exception or stall reason` is required operationally whenever the normal next-action rule is intentionally bypassed.
- Current official documentation does not establish conditional required fields or unique custom pipeline fields. The later evaluator must test whether saved filters, status conventions, and visible exception reports are sufficient; custom code is prohibited as a workaround.

## Mandatory direct checks

- One Contact with two active Window Sales Work items must preserve two independently visible next-action states.
- A saved pipeline view must find the specific item whose `Next action` or `Next action due` is blank even when the Contact has another pending Task.
- Routine task creation, completion, and rescheduling must not require unsustainable duplicate maintenance of Task and pipeline fields.
- Phone-number and last-name search, mobile directions, timed Events, weak-signal save/retry, and desktop/mobile consistency remain unverified.
- Manual entry and any later approved import must visibly detect or route duplicate Centah identifiers for review.
- Export must reconstruct Contacts, Prospecting items, Window Sales Work items, Tasks, Events, Notes, statuses, dates, outcomes, and relationships.

## Official sources

- [Custom field types](https://www.lessannoyingcrm.com/help/custom-field-types)
- [Creating custom contact fields](https://www.lessannoyingcrm.com/help/how-to-create-custom-contact-fields)
- [Creating custom pipeline fields](https://www.lessannoyingcrm.com/help/custom-pipeline-fields)
- [Using pipelines for multiple orders](https://www.lessannoyingcrm.com/help/use-pipelines-to-track-multiple-orders)
- [Task API and Contact linkage](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks)
- [Pipeline Item API](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items)
- [Creating automations](https://www.lessannoyingcrm.com/help/creating-automations)
- [Bulk data export](https://www.lessannoyingcrm.com/help/exporting-all-of-your-data-out-of-lacrm)
