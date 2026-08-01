# P1-W03 Pipedrive Official-Evidence Preflight

**Status:** Official-evidence preflight complete; Lite-only boundary and initial D-099 configuration directly verified

**Candidate:** Pipedrive

**Reviewed:** August 1, 2026

## Preliminary disposition

Pipedrive is suitable for a bounded next-candidate contract. Lite is the lowest plausible production tier, but it is not yet a passing candidate. The documentation mapping in `field-capacity-preflight.md` uses 22 of Lite's 30 custom fields. Direct tenant inspection in `tenant-shell-inspection.md` confirmed that the no-billing trial starts on Premium, and D-098 successfully changed it to Lite with no active add-ons or billing details. Lack of hard required fields, no native deal duplicate identifier, and an unverified single-screen action center still require direct synthetic proof.

## Evidence summary

| Area | Current official evidence | P1-W03 effect |
|---|---|---|
| Trial | Pipedrive advertises a 14-day full-access trial with no credit card required. Without billing details, access locks after the trial rather than converting automatically to paid service. | A clean no-billing evaluation appears available, subject to exact tenant confirmation and a Lite-equivalent feature boundary. |
| Lite cost | Current US pricing lists Lite at `$14` per seat per month billed annually, one annual payment of `$168` per seat. | The two-administrator production baseline is `$336` per year before tax if Lite passes. Exact monthly price, tax, renewal, and checkout terms remain open. |
| Custom fields and volume | Lite allows 30 custom fields per company and 2,500 leads plus deals per seat. The initial documentation map used 22 fields; direct configuration corrected it to 25. | Directly confirmed at 25 of 30, leaving five fields of contingency. Fixture behavior remains untested. |
| Required data | Custom fields exist on Lite, but required-field rules and pipeline-specific field visibility require Premium. | Lite must pass M-07 through visible exception filters and views; do not infer that required fields exist. |
| Record model | People can have multiple open deals; activities can link to people, organizations, leads, and deals. | Plausible match for reusable customers, multiple jobs, and linked next actions. |
| Action visibility | Deals sort by next activity; advanced filters cover deals, contacts, activities, and projects; notifications include activity reminders and overdue scheduling visibility. | Plausible M-01 and M-04 path, but the combined morning action center requires direct proof. |
| Search | Global search covers people by name and phone number and returns linked deals. | Promising for Loryn's phone-number and last-name lookup preference. |
| Mobile | Both iOS and Android list Focus, Nearby, pipeline, activity, calendar, contacts, filtering, offline, audio-note, and notification support. Nearby can hand an address to the navigation app. | Strong preflight fit for mobile speed, directions, and lightweight notes; timing and save behavior remain untested. |
| Portability | Admin exports cover leads, deals, people, organizations, activities, notes, files, default and custom fields, and linked records. Lite includes import/export and API access. | Plausible M-06 and future Centah bridge path; reconstructability and API restrictions remain untested. |
| Duplicate handling | Lite includes duplicate merging for contacts, but official import guidance says deals have no native duplicate identifier. | The searchable Centah field and manual duplicate-review procedure must pass the synthetic test; otherwise M-09 fails. |

## Trial-contamination control

The signup page describes full access and premium LeadBooster, Smart Docs, and Projects features. Do not use full-trial availability as evidence that Lite supports a requirement. Before configuration, the execution contract must require either:

1. direct selection of Lite behavior inside the trial; or
2. a feature-by-feature Lite inventory that excludes every higher-tier or add-on capability.

If neither is possible, stop before fixture entry and report the candidate incomplete rather than fabricating a Lite result.

The August 1 direct inspection confirmed that the trial began on Premium and showed LeadBooster, Smart Docs, and Projects as included. D-098 then authorized a narrow plan transition. Lite was selected, the three carried-over add-ons were disabled, the order summary fell from `$110` to `$24`, and Billing overview confirmed Lite with no active add-ons, no billing details, `$0` during the trial, and the `14-day free trial` label preserved. No configuration or record action occurred.

## Open evidence items

- The direct 25-field correction is within Lite's 30-company-field limit; complete fixture and filter behavior testing.
- Verify whether Lite filters can expose all M-01 action-center states and M-07 missing-next-action exceptions without Premium required fields or custom reports.
- Verify renewal behavior, taxes, commitment, exact two-administrator production cost, and checkout terms. Direct tenant comparison displayed Lite at `$24` per seat per month on monthly billing.
- Verify the exact calendar expiration date; the tenant displayed only `14-day free trial`.
- Verify administrator roles, MFA, access removal, mobile timing, save/offline behavior, manual communication controls, exports, duplicates, and API restrictions only after the relevant action gates are approved.

## Official sources reviewed

- [Pipedrive pricing](https://www.pipedrive.com/en/pricing)
- [Pipedrive trial signup](https://www.pipedrive.com/en/register)
- [Trial expiry and billing behavior](https://support.pipedrive.com/en/article/what-happens-when-my-pipedrive-trial-expires)
- [Pipedrive plan features](https://support.pipedrive.com/en/article/what-features-do-the-pipedrive-plans-have)
- [Usage limits](https://support.pipedrive.com/en/article/usage-limits-in-pipedrive)
- [Custom fields and plan boundaries](https://support.pipedrive.com/en/article/custom-fields)
- [Pipedrive data relationships](https://support.pipedrive.com/en/article/how-is-pipedrive-data-organized)
- [Advanced filtering](https://support.pipedrive.com/en/article/filtering)
- [Pipeline and next-activity behavior](https://support.pipedrive.com/en/article/pipeline-view)
- [Global search](https://support.pipedrive.com/en/article/search-finding-what-you-need)
- [Mobile feature inventory](https://support.pipedrive.com/en/article/what-features-do-the-mobile-apps-have)
- [Nearby mobile directions](https://support.pipedrive.com/en/article/the-nearby-feature)
- [Data export](https://support.pipedrive.com/en/article/exporting-data-from-pipedrive)
- [Duplicate merging](https://support.pipedrive.com/en/article/merge-duplicates)
- [Pipedrive API reference](https://developers.pipedrive.com/docs/api/v1)
