# P1-W03 Pipedrive Lite Field-Capacity Preflight

**Status:** Documentation mapping; direct tenant confirmation pending; no account action authorized

**Mapped:** August 1, 2026

## Result

The CP-003 minimum model maps to 22 planned Pipedrive custom fields: 9 Person fields and 13 shared Lead/Deal fields. Activities use standard fields. This is below Lite's official 30-custom-field company limit and leaves eight fields of contingency.

This is a capacity finding, not a configuration result. Field availability, filter behavior, search behavior, and the exact count must be confirmed in an authorized Lite-equivalent trial before fixtures are entered.

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
| Source and source detail | Standard source channel and source channel ID; confirm allowed values | 0 |
| Centah lead number | Custom text on Lead/Deal; Costco/Centah only | 1 |
| Current stage | Standard pipeline and stage | 0 |
| Last-contact date and time | Custom date/time unless the trial proves a standard system value is complete and filterable | 1 |
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
| **Lead/Deal total** |  | **13** |

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
- The eight-field contingency is not permission to add scope. Any added field must map to an approved requirement or an evidence-backed correction.

## Sources

- [Pipedrive usage limits](https://support.pipedrive.com/en/article/usage-limits-in-pipedrive)
- [Pipedrive custom fields](https://support.pipedrive.com/en/article/custom-fields)
- [Pipedrive import fields](https://support.pipedrive.com/en/article/import-fields)
- [Pipedrive import duplicate behavior](https://support.pipedrive.com/en/article/how-to-avoid-duplicates-during-an-import)
- [Pipedrive data organization](https://support.pipedrive.com/en/article/how-is-pipedrive-data-organized)
