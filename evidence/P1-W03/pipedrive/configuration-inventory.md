# P1-W03 Pipedrive Lite Configuration Inventory

**Status:** Evaluator configuration and stopping-rule run complete under D-099; CP-007 pending

**Configured:** August 1, 2026

## Boundary

This inventory records only the sanitized synthetic evaluator configuration in the `Hazel Kaine` Pipedrive Lite trial. It contains no credentials, account identifiers, private email addresses, real customer data, billing details, external connections, or customer communications.

## Verified starting state

- Lite remained active with one evaluator seat, no active add-ons, no billing details, and the 14-day no-billing trial label.
- Eight visible vendor activities and their linked records were labeled `[Sample]`.
- Pipedrive's global-administrator sample-data removal confirmation named only `[Sample]` deals, people, organizations, and activities.
- The post-action activity screen confirmed successful sample-data deletion.

## Configured data model

- Custom-field usage: 25 of 30.
- Person fields: 9.
- Shared Lead/Deal fields: 16.
- Activities use standard Pipedrive fields.
- The detailed mapping and the three-field correction are in `field-capacity-preflight.md`.

## Configured pipeline

Pipeline name: `Window Sales Jobs`

1. `New Customer Request`
2. `Trying to Contact`
3. `Appointment Scheduled`
4. `Appointment Completed`
5. `Preparing Quote`
6. `Quote Sent - Awaiting Decision`
7. `Customer Accepted - Handoff Due`
8. `Handoff Complete - Installation Pending`
9. `Installed - Customer Follow-Up Due`

Pipedrive Won maps to `Finished`. Pipedrive Lost plus a retained reason maps to `Lost / Canceled`.

## Activity types

- Standard activity types remain available where applicable.
- Added `Quote follow-up`.
- Added `Handoff`.
- Added `Installation check`.
- Added `Customer follow-up`.
- Disabled the generic post-won three-month task prompt because it conflicts with the approved source-specific follow-up rules.

## Lost reasons

- `No Response`
- `No Decision`
- `Declined`
- `Customer Canceled`
- `Invalid Information`
- `Duplicate`

## Synthetic fixture state

- Imported the seven-row preload from `synthetic-fixtures.csv` using Pipedrive's merge-data option.
- The import mapped 17 of 19 columns. `fixture_id` and `pipeline` remained intentionally unmapped; the Stage mapping placed every deal in `Window Sales Jobs`.
- Import result: 14 items added, consisting of seven reusable People records and seven linked Deal records; zero updated, merged, or skipped.
- Added the six baseline activities required to expose today's appointment, today's contact, overdue quote work, two accepted-sale handoffs, and the installation exception. `SYN-QUEUE-H` intentionally has no activity.
- Added a synthetic note and `$4,250` deal value to `SYN-QUOTE-D` while retaining its synthetic quote-sent date and visibly overdue follow-up.

## Practical views and filters

- The Activities list exposes native `Today` and `Overdue` states and showed the scheduled appointment, first-contact call, overdue quote follow-up, installation check, and handoff activities.
- A private `Missing Next Action` Deal filter using an empty next-activity date returned only `SYN-QUEUE-H` after the baseline activities were scheduled.
- A private `Waiting on Others` Deal filter using `Installation status = Exception - 3 Months` returned only `SYN-INSTALL-G`.
- These controls expose the required conditions, but they do not combine all five M-01 states into one screen. M-01 therefore remains unverified rather than being treated as a pass.

## Direct scenario observations

- TS-01: created `Synthetic Prospect Alpha` with a fictional phone number, `Referral` source, and dated next action; confirmed it was searchable; then removed the test Lead and Person.
- TS-02: verified phone-number and last-name search, native Today/Overdue activity visibility, and the two saved exception filters.
- TS-03: Pipedrive accepted a second Deal carrying the existing `SYN-CENTAH-1001` value without blocking it or visibly routing it for review. This directly fails the approved duplicate-control result.
- TS-04: the desktop Deal and linked Person exposed the stored appointment context and service address. Selecting the address entered edit mode rather than opening directions. Native mobile directions and manual confirmation-composer timing were not tested.
- TS-05: the note, value, quote-sent date, manual notice notation, and overdue dated follow-up were directly visible. No communication was sent.
- TS-06: both source branches can store the approved facts, but Lite shows the same handoff fields on both and cannot conditionally require the source-specific set or prevent premature completion. Source-specific date-anchor behavior was not produced.
- TS-07: the three-month installation exception, retained fictional result, same-day coordinator task, and still-unconfirmed state were directly visible. Customer-contact prompting was not verified.

## Export observation

- Pipedrive generated server-side XLSX exports for Deals (7 items), People, Activities (7 items using `Date added`), Notes, and the temporary TS-01 Lead.
- A first Activities export used the wrong `Marked as done` date filter and correctly produced zero items; it was superseded by the seven-item export.
- The direct download redirected to a vendor-hosted object URL that Chrome blocked with `ERR_BLOCKED_BY_CLIENT`. No export file was downloaded or inspected, so field completeness and customer-to-job reconstructability remain unverified.

## Cleanup state

- Deleted the temporary TS-01 Lead and Person and the duplicate Deal and duplicate Person created during TS-03. The active People list returned to the seven baseline synthetic people.
- Pipedrive states that deleted records remain recoverable for 30 days. The TS-01 activity may remain as an unlinked synthetic activity after Person deletion.
- The seven baseline fixtures, scenario activities, quote note/value, saved filters, and generated server-side exports remain in the synthetic trial as evaluation evidence. Reset them before any later rerun or closeout cleanup.

## Remaining unverified evidence

- A single-screen M-01 action center.
- Native mobile timing, directions, offline behavior, notifications, and audio-note behavior.
- Cross-device save, synchronization, pending-state, retry, and duplicate-activity behavior.
- Downloaded export contents and customer-to-job reconstruction.
- Two-administrator access, MFA, removal, renewal, tax, and exact checkout behavior.
- Customer-contact prompting and source-specific date-anchor behavior.

Unverified items remain unscored and cannot be treated as a pass.
