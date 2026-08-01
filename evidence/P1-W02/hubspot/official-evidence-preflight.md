# P1-W02 HubSpot Official-Evidence Preflight

**Status:** Preliminary official-evidence finding; no account or external action authorized

**Candidate:** HubSpot CRM

**Reviewed:** July 31, 2026

**Evidence scope:** Current official public HubSpot documentation only

## Scope and evidence rule

This preflight checks whether a plausible HubSpot production tier can represent the signed CP-003 workflow before another account is created or Loryn is involved. It does not score HubSpot, approve the P1-W02 execution contract, authorize an account or trial, activate a paid feature, enter billing information, connect an external service, use real data, or select a platform.

Feature packaging, promotional pricing, and account-specific offers can change. Any later tenant must confirm the exact edition, seats, features, commitment, and billing state before configuration begins.

## Preliminary result

HubSpot Free is not a faithful configuration tier for the approved baseline because it permits only 10 custom properties in total. The CP-003 model needs substantially more distinct nonstandard contact and deal fields, including source-specific dates, permission and opt-out controls, installation states, exception reasons, and a unique opportunity-level Centah lead number. Loading the common fixtures on Free would therefore omit approved facts or collapse them into notes, violating M-07 and M-13.

A Starter-level paid path remains plausible on paper. HubSpot's Product & Services Catalog lists 1,000 custom properties per object, required fields, two deal pipelines, CRM imports and exports, and a $20-per-Core-Seat starting price for Smart CRM Starter. For the approved two-administrator model, the nonpromotional planning cost is therefore $40 per month before tax.

This is a `Conditional Pass` possibility only. Official HubSpot pages currently describe Starter packaging differently, limited-time promotional pricing is present, and the public 14-day trial is specifically Marketing Hub Professional rather than a clean Starter evaluation. The exact Starter-equivalent SKU, commitment, feature exposure, and no-billing trial availability remain unverified. No account should be created until the P1-W02 contract is approved, and no paid or promotional tier should be activated without its separate gate.

## Current evidence inventory

| Area | Current official evidence | P1-W02 implication | Status |
|---|---|---|---|
| Free users and capacity | Free is $0, supports up to two users, 1,000 contacts, and 1 million records across other standard object types. | The two-person model fits the user limit, but capacity does not cure the field-model blocker. | Verified |
| Standard CRM records | Free includes contacts, companies, deals, tasks, and activities. | Contacts can represent reusable customers and deals can represent multiple jobs related to one customer. Direct relationship behavior still needs fixture testing. | Plausible; direct test required |
| Free custom properties | Free permits 10 custom properties in total. | This is below the CP-003 contact-and-job requirement. Free cannot receive the common fixture set faithfully. | Confirmed Free blocker |
| Starter field capacity | The catalog lists 1,000 custom properties per object for Starter, Professional, and Enterprise Smart CRM. | Starter has ample field capacity on paper. Exact account packaging must be confirmed before configuration. | Conditional Pass |
| Required and unique values | Required fields are listed for paid Smart CRM. Property validation, including up to 10 unique-value properties per object, is available; regex validation alone requires Professional or Enterprise. | A unique deal-level Centah number is plausible without regex. Stage-specific and source-conditional enforcement still requires direct testing or visible exception reporting. | Conditional Pass |
| Pipelines and stages | Free has one deal pipeline; Starter lists two. | One approved active-job pipeline is sufficient for the minimum design. Prospecting can remain on contact records rather than requiring a second deal pipeline. | Plausible |
| Views, tasks, and dashboard | Saved record views, task views, dashboards, and due/overdue task filters are documented. The multi-source custom report builder requires Professional or Enterprise. | Starter may support the five operational views, but M-01's single practical action center is a decision-critical risk. Direct testing must prove an acceptable dashboard or equivalent without relying on Professional-only custom reports. | Unverified mandatory risk |
| Mobile | HubSpot provides iOS and Android apps. All plans can create, view, associate, and complete tasks on mobile; due work appears on the mobile Home and Tasks screens. | The mobile foundation is plausible. Phone/last-name search, directions, notes, save feedback, weak-signal behavior, and one-minute timings require direct testing. | Unverified |
| Two administrators and access | Users can be made Super Admins; Super Admins can add, deactivate, and remove users. Paid users require an appropriate seat. | Loryn can be primary Super Admin and the technical partner secondary Super Admin if the exact two-seat tier is confirmed. | Conditional Pass |
| MFA and recovery | HubSpot supports 2FA on all plans and requires it for paid Starter, Professional, and Enterprise username/password users. Backup and reset procedures are documented. | The security model is suitable on paper. Credentials, methods, codes, and recovery details must remain private and outside project artifacts. | Conditional Pass |
| Change history | Record property history is available on all plans. Starter-level centralized audit logs cover login and security activity; broader audit categories are Enterprise features. | Record history may be sufficient for the right-sized two-person operation, but important-change coverage and usability require direct verification. | Conditional Pass |
| Exports and relationships | All plans can export record properties and associations. Activities such as calls and notes require separate contact export, activity reports, or the engagements API. | Customer-to-job relationships appear reconstructable, but complete multi-record activity and note portability must be tested with synthetic exports. | Conditional Pass |
| Deletion and exit | Records can be restored for 90 days after normal deletion; contacts can be permanently deleted. Paid subscriptions end at the commitment boundary before the account can be deleted. | Lifecycle controls are documented, but exact production retention remains governed by D-013 and subscription terms must be verified before purchase. | Conditional Pass |
| API path | Private apps on Free and Starter are documented at 100 requests per 10 seconds and 250,000 requests per day per account. | A future CRM-side integration path exists in principle. Centah capabilities remain unverified under D-012, and no app or connection is authorized. | HubSpot side plausible; Centah side unverified |
| Production cost | The catalog lists Smart CRM Starter at $20 per Core Seat per month. Current pricing pages also display limited promotional Starter prices and inconsistent standalone packaging descriptions. | Use $40/month before tax for two administrators as the conservative planning figure. Verify exact SKU, term, renewal price, and checkout total before any purchase. | Planning cost verified; purchasable offer unverified |
| Trial path | The public 14-day trial is Marketing Hub Professional. No reviewed official page confirms a clean, no-billing Starter-equivalent trial. | Do not use Professional trial behavior as evidence of Starter capability. Trial activation requires a separate gate only after exact tier exposure and billing behavior are verified. | Unverified blocker to direct Starter evaluation |

## Mandatory-gate implications before direct testing

| Gate | Preliminary state | Reason |
|---|---|---|
| M-01 | `Unverified` | Starter dashboards and saved views exist, but a single practical cross-object action center may depend on Professional-only custom reporting. |
| M-02 | `Conditional Pass` | Starter field capacity and unique-value rules can represent source and Centah logic on paper; conditional enforcement is untested. |
| M-03 | `Unverified` | Mobile tasks exist, but the five one-minute actions require the common timed test. |
| M-04 | `Conditional Pass` | Tasks, due/overdue views, saved views, and deal-stage task triggers are documented; the complete reminder set is untested. |
| M-05 | `Conditional Pass` | Two paid Core Seats, Super Admin controls, required MFA, access removal, and record history are documented. |
| M-06 | `Conditional Pass` | Record and association exports exist; activity completeness and relationship reconstruction require synthetic export testing. |
| M-07 | Free: `Fail`; Starter: `Conditional Pass` | Free has only 10 custom properties total. Starter has sufficient field capacity on paper. |
| M-08 | `Conditional Pass` | Manual activities and custom permission/opt-out fields are possible; suppression behavior remains untested. |
| M-09 | `Conditional Pass` | Unique deal properties and imports are documented; Centah-side interfaces remain unverified. |
| M-10 | `Unverified` | Cross-device, weak-signal, save, retry, and duplicate behavior need direct testing. |
| M-11 | `Conditional Pass` | Conservative two-seat planning cost is $40/month before tax; exact SKU, commitment, renewal, and trial path remain unverified. |
| M-12 | `Unverified` | Learning and weekly administration burden require the evaluator trial. |
| M-13 | Free: `Fail`; Starter: `Unverified` | Free cannot hold the common fixtures. Starter requires direct configuration and scenario evidence. |

## Pre-account decision rule

Proceed to account creation only after the complete P1-W02 contract is approved. After account creation, stop before configuration unless the account clearly exposes a no-billing Starter-equivalent evaluation matching the documented field, view, task, export, and administration scope.

If no clean Starter-equivalent evaluation is available, stop and present three separately gated options:

1. Retain HubSpot Starter as documentation-only.
2. Authorize a separately scoped paid evaluation or purchase after exact checkout and commitment review.
3. Close HubSpot incomplete and screen the next CRM candidate.

Do not substitute the Marketing Hub Professional trial, infer Starter behavior from Professional features, or load an incomplete Free fixture set.

## Official sources

- [HubSpot Product & Services Catalog](https://legal.hubspot.com/hubspot-product-and-services-catalog)
- [HubSpot Free and Starter pricing](https://www.hubspot.com/pricing/crm)
- [HubSpot Smart CRM pricing](https://www.hubspot.com/pricing/smart-crm)
- [HubSpot public 14-day trial](https://offers.hubspot.com/free-trial)
- [Create and edit properties](https://knowledge.hubspot.com/properties/create-and-edit-properties)
- [Set property validation rules](https://knowledge.hubspot.com/properties/set-validation-rules-for-properties)
- [Create and manage saved views](https://knowledge.hubspot.com/records/create-and-manage-saved-views)
- [Filter tasks and manage task views](https://knowledge.hubspot.com/tasks/filter-tasks-and-manage-task-views)
- [Use tasks in the HubSpot mobile app](https://knowledge.hubspot.com/mobile/use-tasks-in-the-hubspot-mobile-app)
- [Manage HubSpot dashboards](https://knowledge.hubspot.com/dashboards/manage-your-dashboards)
- [HubSpot custom report builder](https://knowledge.hubspot.com/reports/understand-the-custom-report-builder)
- [Add HubSpot users](https://knowledge.hubspot.com/account-management/add-hubspot-users)
- [Remove HubSpot users](https://knowledge.hubspot.com/user-management/remove-hubspot-users)
- [Set up HubSpot 2FA](https://knowledge.hubspot.com/account-security/set-up-two-factor-authentication-for-your-hubspot-login)
- [View record property history](https://knowledge.hubspot.com/articles/kcs_article/contacts/view-property-history)
- [Export CRM records](https://knowledge.hubspot.com/import-and-export/export-records)
- [Delete CRM records](https://knowledge.hubspot.com/records/delete-crm-records)
- [Downgrade or cancel HubSpot](https://knowledge.hubspot.com/account/how-do-i-cancel-my-hubspot-account)
- [HubSpot API usage limits](https://developers.hubspot.com/docs/developer-tooling/platform/usage-guidelines)

## Open evidence items

- Verify the exact Starter-equivalent SKU, two-Core-Seat total, commitment term, renewal price, and tax treatment without purchasing.
- Determine whether a no-billing Starter-equivalent trial exists and whether it avoids Professional-only feature contamination.
- Verify whether Starter can deliver M-01's single practical action center without the Professional custom report builder.
- Directly verify required/unique field behavior, source-specific exceptions, mobile search and directions, manual communications, export completeness, duplicate handling, and cross-device reliability only after the relevant action gates are approved.
