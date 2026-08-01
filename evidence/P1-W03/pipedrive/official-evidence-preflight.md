# P1-W03 Pipedrive Official-Evidence Preflight

**Status:** Official-evidence preflight complete; field-capacity follow-up linked; no account, trial, configuration, or purchase authorized

**Candidate:** Pipedrive

**Reviewed:** August 1, 2026

## Preliminary disposition

Pipedrive is suitable for a bounded next-candidate contract. Lite is the lowest plausible production tier, but it is not yet a passing candidate. The documentation mapping in `field-capacity-preflight.md` uses 22 of Lite's 30 custom fields. Lack of hard required fields, no native deal duplicate identifier, trial feature contamination, and an unverified single-screen action center still require direct synthetic proof.

## Evidence summary

| Area | Current official evidence | P1-W03 effect |
|---|---|---|
| Trial | Pipedrive advertises a 14-day full-access trial with no credit card required. Without billing details, access locks after the trial rather than converting automatically to paid service. | A clean no-billing evaluation appears available, subject to exact tenant confirmation and a Lite-equivalent feature boundary. |
| Lite cost | Current US pricing lists Lite at `$14` per seat per month billed annually, one annual payment of `$168` per seat. | The two-administrator production baseline is `$336` per year before tax if Lite passes. Exact monthly price, tax, renewal, and checkout terms remain open. |
| Custom fields and volume | Lite allows 30 custom fields per company and 2,500 leads plus deals per seat. The documentation map uses 22 custom fields. | Plausible with eight fields of contingency; direct tenant confirmation remains required before fixtures. |
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

## Open evidence items

- Directly confirm the 22-field documentation map and correct it without exceeding Lite's 30-company-field limit.
- Verify whether Lite filters can expose all M-01 action-center states and M-07 missing-next-action exceptions without Premium required fields or custom reports.
- Verify exact monthly Lite pricing, renewal behavior, taxes, commitment, trial expiry, and two-administrator production cost.
- Verify the trial's exact starting plan and whether it can be constrained to Lite without entering billing information.
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
