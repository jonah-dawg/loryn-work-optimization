# P1-W03 Pipedrive Lite Field-Capacity Preflight

**Status:** Direct Lite configuration confirmed under D-099

**Mapped:** August 1, 2026

## Result

The directly configured CP-003 model uses 25 Pipedrive custom fields: 9 Person fields and 16 shared Lead/Deal fields. Activities use standard fields. The Lite tenant displayed `25/30 custom fields in use`, leaving five fields of contingency.

The three-field correction from the documentation map is evidence-backed: Pipedrive does not offer a combined custom date-time field, so last contact uses separate date and time fields; and the standard acquisition metadata does not represent the approved Costco/independent operational branch, so `Lead source` and `Source detail` are explicit shared Lead/Deal fields. Filter, search, fixture, and scenario behavior still require direct testing.

## Person mapping

| CP-003 need | Pipedrive mapping | Custom count |
|---|---|---:|
| Display name, phone, email | Standard Person name, phone, and email | 0 |
| Alternate reachable social identity or location | `Alternate reachable channel` custom text | 1 |
| Preferred contact method | Custom single option | 1 |
| Acquisition date | Custom date; source itself uses the linked Lead/Deal source fields | 1 |
| Contact-permission status | Custom single option | 1 |
| Overall do-not-contact status | Custom single option | 1 |
| Do-not-contact date | Custom date | 1 |
| Do-not-contact reason | Custom large text | 1 |
| Channel-specific opt-outs | Custom multiple option | 1 |
| Unresolved-problem indicator | Custom yes/no | 1 |
| **Person total** |  | **9** |

## Lead and deal mapping

Pipedrive uses the same custom fields for leads and deals, so prospect fields do not consume a second copy when a lead converts.

| CP-003 need | Pipedrive mapping | Custom count |
|---|---|---:|
| Prospect state | Custom single option; directly test preservation through conversion and archive outcomes | 1 |
| Linked customer | Standard linked Person or Organization | 0 |
| Service address | Custom address field on Lead/Deal | 1 |
| Source and source detail | Custom `Lead source` single option and `Source detail` text; standard acquisition metadata is not used as the operational branch | 2 |
| Centah lead number | Custom text on Lead/Deal; Costco/Centah only | 1 |
| Current stage | Standard pipeline and stage | 0 |
| Last-contact date and time | Separate custom date and time fields; the tenant has no combined custom date-time type | 2 |
| Next action and due date/time | Standard linked next Activity | 0 |
| Appointment date and time | Standard linked meeting Activity | 0 |
| Quoted amount | Standard Deal value | 0 |
| Quote-sent date | Custom date | 1 |
| Acceptance date | Custom date | 1 |
| DocuSign-sent date | Custom date | 1 |
| Coordinator-email date | Custom date | 1 |
| Installation status | Custom single option | 1 |
| Installation-confirmed date | Custom date | 1 |
| Post-install follow-up date | Custom date | 1 |
| Post-install result | Custom single option or text after direct option review | 1 |
| Close outcome or reason | Standard won/lost status and lost reason; directly prove the `Finished` mapping | 0 |
| Exception or stall reason | Custom large text | 1 |
| **Lead/Deal total** |  | **16** |

## Activity mapping

| CP-003 need | Pipedrive mapping | Custom count |
|---|---|---:|
| Linked customer and job | Standard linked Person and Deal | 0 |
| Activity/task type | Standard or custom activity type | 0 |
| Due date/time and status | Standard due date, due time, and done status | 0 |
| Completed date/time | Standard done time | 0 |
| Result or note | Standard activity note | 0 |
| **Activity total** |  | **0** |

## Mandatory controls that field capacity does not prove

- Lite cannot hard-require custom fields. Missing-field and next-action controls must work through filters or visible exception views.
- Official import guidance says deals have no native duplicate identifier. The Centah lead number must therefore be searchable and supported by a reliable duplicate-review procedure; the synthetic duplicate test must fail Pipedrive if that procedure is impractical or unreliable.
- The Lead-to-Deal conversion must preserve the prospect history and shared fields without duplicate customers or jobs.
- The five-field contingency is not permission to add scope. Any added field must map to an approved requirement or an evidence-backed correction.

## Direct configuration inventory

### Person fields (9)

`Alternate reachable channel`, `Preferred contact method`, `Acquisition date`, `Contact-permission status`, `Overall do-not-contact status`, `Do-not-contact date`, `Do-not-contact reason`, `Channel-specific opt-outs`, and `Unresolved-problem indicator`.

### Shared Lead/Deal fields (16)

`Prospect state`, `Service address`, `Lead source`, `Source detail`, `Centah lead number`, `Last-contact date`, `Last-contact time`, `Quote-sent date`, `Acceptance date`, `DocuSign-sent date`, `Coordinator-email date`, `Installation status`, `Installation-confirmed date`, `Post-install follow-up date`, `Post-install result`, and `Exception or stall reason`.

## Sources

- [Pipedrive usage limits](https://support.pipedrive.com/en/article/usage-limits-in-pipedrive)
- [Pipedrive custom fields](https://support.pipedrive.com/en/article/custom-fields)
- [Pipedrive import fields](https://support.pipedrive.com/en/article/import-fields)
- [Pipedrive import duplicate behavior](https://support.pipedrive.com/en/article/how-to-avoid-duplicates-during-an-import)
- [Pipedrive data organization](https://support.pipedrive.com/en/article/how-is-pipedrive-data-organized)
