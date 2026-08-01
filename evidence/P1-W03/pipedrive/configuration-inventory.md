# P1-W03 Pipedrive Lite Configuration Inventory

**Status:** In progress under D-099

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

- The seven-record preload is prepared in `synthetic-fixtures.csv`.
- `SYN-PROSPECT-A` is intentionally absent from the preload and reserved for TS-01.
- The fixture file parses as seven rows and contains only fictional names, reserved example contact values, and synthetic identifiers.
- The file has not yet been loaded into Pipedrive at this saved state.

## Incomplete configuration and evidence

- Practical action-center and exception filters/views.
- Synthetic fixture import and activity scheduling.
- TS-01 through TS-07 desktop execution.
- Native mobile timing and mobile-only behavior.
- Duplicate-review behavior for `Centah lead number`.
- Synthetic export and reconstructability.
- Save/synchronization/recovery evidence.
- Narrow cleanup and evaluator result.

Unverified items remain unscored and cannot be treated as a pass.
