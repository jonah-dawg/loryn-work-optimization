# P1-W05 Freshsales Pro Field-Capacity Preflight

**Status:** Closed documentation-only under D-108; 9 Contact, 17 Deal, and 0-2 activity fields mapped; no direct tenant confirmation

**Mapped:** August 1, 2026

## Result

The CP-003 model fits comfortably within Freshsales Pro's documented limit of 250 custom fields per module. The conservative map uses 9 Contact custom fields, 17 Deal custom fields, and at most 2 Task or custom-activity contingency fields. Default Contact fields cover identity, reachable channels, social profiles, address, lifecycle stage, source, and do-not-disturb state. Default Deal fields cover related Contacts, source, stage, value, and system activity metadata.

Capacity alone does not establish viability. The map deliberately retains explicit `Next action` and `Next action due` fields on active Contacts and Deals so a record with no next action can be detected without inferring from hidden activity relationships. Direct evaluation must determine whether those fields can remain the canonical entry point and create or align reminders without routine duplicate entry. If not, M-01, M-04, M-07, or M-12 may fail despite ample field capacity.

## Proposed evaluated record model

- Contacts are reusable people, businesses, or social identities and may begin as prospects.
- Activities hold Tasks, Appointments, Calls, and optional Pro custom sales activities linked to Contacts and, after conversion, Deals.
- A confirmed project creates one Deal linked to the reusable Contact. A returning customer may therefore have multiple Deals.
- Use one `Window Sales Work` Deal pipeline first, with a required `Work source` field controlling Costco/Centah-only Deal fields. Do not create separate source pipelines unless direct evidence proves that one action center remains unified.
- Accounts are optional and used only when a builder, business, or other company identity is operationally useful.

## Contact mapping

| CP-003 need | Proposed Freshsales mapping | Custom count |
|---|---|---:|
| Display name | Standard First name and Last name; Account association only when a business identity is useful | 0 |
| Reachable phone, email, social identity, or address | Standard Email, Work/Mobile/Other phone, Address, City, State, Zipcode, Country, Facebook, Twitter, and LinkedIn | 0 |
| Prospect state | Standard Lifecycle stage customized to `Active`, `Long-Term Nurture`, `Converted`, `Archived`, and `Do Not Contact` | 0 |
| Preferred contact method | Custom drop-down | 1 |
| Acquisition source and date | Standard Source plus custom date | 1 |
| Contact-permission status | Custom drop-down | 1 |
| Overall do-not-contact status, date, and reason | Standard Do not disturb plus custom date and text area | 2 |
| Channel-specific opt-outs | Custom multi-select | 1 |
| Unresolved-problem indicator | Custom checkbox | 1 |
| Prospect next action and due date/time | Custom text plus custom date picker; exact time support and reminder linkage require direct confirmation | 2 |
| **Contact total** |  | **9** |

## Deal mapping

| CP-003 need | Proposed Freshsales mapping | Custom count |
|---|---|---:|
| Linked customer | Standard Related contacts | 0 |
| Service address | Custom text field; direct mobile directions test is mandatory | 1 |
| Lead source and source detail | Standard Source plus custom text field | 1 |
| Work source | Custom drop-down: `Costco/Centah` or `Independent`; controlling field for source-specific dependencies | 1 |
| Centah lead number | Custom text field marked unique and conditionally required only for Costco/Centah | 1 |
| Current stage | Standard Deal pipeline and Deal stage | 0 |
| Last-contact date and time | Custom date picker; compare against standard Last activity date and related-contact last-contact information during direct inspection | 1 |
| Next action and due date/time | Custom text plus custom date picker; canonical-entry and reminder behavior require direct proof | 2 |
| Appointment date and time | Standard linked Appointment; a custom mirror is prohibited unless direct evidence proves it necessary and maintainable | 0 |
| Quoted amount | Standard Deal value | 0 |
| Quote-sent date and time | Custom date picker | 1 |
| Acceptance date and time | Custom date picker | 1 |
| DocuSign-sent date and time | Custom date picker; dependent and required only for Costco/Centah at the handoff boundary | 1 |
| Coordinator-email date and time | Custom date picker; required for every accepted job | 1 |
| Installation status and confirmed date/time | Custom drop-down plus custom date picker | 2 |
| Post-install follow-up date/time and result | Custom date picker plus custom drop-down or text area | 2 |
| Close outcome or reason | Custom drop-down; standard Lost reason may be reused only if it covers every retained close outcome | 1 |
| Exception or stall reason | Custom text area; filtering and required-state behavior require direct confirmation | 1 |
| **Deal total** |  | **17** |

## Activity mapping

| CP-003 need | Proposed Freshsales mapping | Custom count |
|---|---|---:|
| Linked customer and job | Standard Related to links for Contact and Deal | 0 |
| Activity or task type | Standard Task, Appointment, Call log, or Pro custom sales activity plus title/type | 0 |
| Due date/time and status | Standard Task due date/time and status; direct time granularity, overdue, and mobile behavior required | 0 |
| Completed date/time | Use system completion/activity timestamp if directly exportable; otherwise one bounded custom field | 0-1 |
| Result or note | Standard description/outcome if it can be required at completion; otherwise one bounded custom result field | 0-1 |
| **Activity contingency total** |  | **0-2** |

## Capacity summary

| Module | Conservative custom-field use | Pro documented limit | Headroom |
|---|---:|---:|---:|
| Contacts | 9 | 250 | 241 |
| Deals | 17 | 250 | 233 |
| Tasks or custom sales activities | 0-2 | 250 | 248-250 |

The large headroom is not permission to expand scope, mirror every activity, or add a custom application layer. Direct corrections must remain tied to a CP-003 requirement and preserve sustainable administration.

## Proposed dependency and uniqueness design

- `Work source` controls the visibility and requirement of `Centah lead number` and `DocuSign sent date`.
- `Coordinator email date` remains required for both source branches at the accepted-sale handoff boundary.
- `Installation confirmed date` becomes required only when installation status is `Confirmed`.
- `Exception or stall reason` becomes required only when the normal next-action rule is deliberately overridden or a designated exception state is selected.
- `Centah lead number` is unique on Deals. Direct tests must cover manual save, CSV import, and any permitted API/upsert evidence.
- Dependency validation does not protect imports or bulk updates. The later evaluator run must include a negative source/dependency import and a visible reconciliation route; uniqueness alone is insufficient.

## Mandatory controls that capacity does not prove

- One practical M-01 view must contain today's appointments, people to contact today, overdue actions, waiting-on-others jobs, and active Contacts or Deals missing next action/due date.
- Canonical next-action fields and linked Tasks must not require routine duplicate entry. If a workflow creates Tasks, rescheduling and completion must remain understandable and reliable.
- One pipeline must support both handoff branches, source-specific installation anchors, retained exits, and the three-month exception without hiding records in separate source views.
- Appointment timing, working-day calculations, reminder times, date-time precision, and missing-next-action filtering require direct tenant proof.
- Contact prospecting must convert into a linked project without losing activity history or duplicating the reusable Contact.
- Activity completion timestamps, result enforcement, mobile address-to-directions behavior, offline conflict handling, and export relationship reconstruction remain unverified.
- Pro's record/activity history must be sufficient for right-sized M-05 administration without relying on Enterprise-only audit logs or field-level permissions.

## Official sources

- [Freshsales Contact fields](https://crmsupport.freshworks.com/support/solutions/articles/50000002371-what-are-contact-fields-and-how-to-customize-them-)
- [Freshsales Deal fields](https://crmsupport.freshworks.com/support/solutions/articles/50000002554-how-to-create-a-deal-)
- [Freshsales required fields](https://crmsupport.freshworks.com/support/solutions/articles/50000002404-what-is-a-required-field-how-to-make-a-field-required-)
- [Freshsales custom fields and plan limits](https://crmsupport.freshworks.com/support/solutions/articles/50000002389-how-to-create-custom-fields-for-contacts-accounts-and-deals-)
- [Freshsales field dependencies](https://crmsupport.freshworks.com/support/solutions/articles/50000002573-how-to-configure-field-dependency-)
- [Freshsales unique fields](https://crmsupport.freshworks.com/support/solutions/articles/50000002578-what-are-unique-fields-why-are-few-fields-marked-as-unique-by-default-)
- [Freshsales Customer 360 summary fields](https://crmsupport.freshworks.com/support/solutions/articles/50000003911-default-configuration-in-summary-section-for-contact-account-and-deal-pages)
- [Freshsales custom sales activities](https://crmsupport.freshworks.com/support/solutions/articles/50000002991-what-are-custom-sales-activities-how-to-use-them-)
