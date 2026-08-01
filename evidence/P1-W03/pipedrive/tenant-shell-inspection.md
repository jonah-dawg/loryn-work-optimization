# P1-W03 Pipedrive Tenant-Shell Inspection

**Status:** Lite-only no-billing trial boundary verified under D-098; configuration remains unapproved

**Candidate:** Pipedrive

**Inspected:** August 1, 2026

## Authorized scope

The initial inspection used the bounded D-097 authority to confirm only nonprivate account-shell, trial, plan, expiry, and feature-boundary labels. D-098 subsequently authorized changing only the existing no-billing trial from Premium to Lite, removing carried-over trial add-ons, and verifying the resulting plan and remaining-trial state. Neither decision authorized configuration, synthetic fixture entry, testing, billing, a purchase, an external connection, real data, customer communication, production use, or Loryn participation.

## Initial D-097 findings

| Area | Direct observation | Effect |
|---|---|---|
| Account shell | The evaluator account opened successfully with the organization label `Hazel Kaine`. | The bounded account shell is complete. |
| Trial state | Billing overview displayed `14-day free trial`. It did not display an exact calendar expiration date. | Trial duration is confirmed; exact expiration date remains unverified. |
| Current edition | Billing overview identified the current plan as `Premium`, billed monthly, with one seat in use. | The trial is not a clean Lite environment. Premium behavior cannot count as Lite evidence. |
| Current charge state | The overview paired the Premium plan amount of `$74` with `$0` during the trial. No billing details had been entered. | No purchase or paid commitment was made. The Premium amount is not an approved production recommendation. |
| Included trial features | LeadBooster, Smart Docs, and Projects appeared as included with the Premium trial. | These higher-tier or add-on features must not contaminate a Lite evaluation. |
| Lite availability | The read-only plan comparison displayed Lite at `$24` per seat per month on monthly billing or `$14` per seat per month when billed annually. | Lite appears selectable, but D-097 did not authorize changing the trial edition. |
| Lite limits | The comparison displayed 2,500 leads and deals per seat, 30 custom fields per company, 15 reports per seat, and 30,000 API tokens per seat for Lite, subject to the displayed company-wide caps. | The direct labels support the official preflight, but configuration and testing remain required before viability can be determined. |
| Preloaded content | The setup surface showed an Activities count of three before any evaluator record entry. The contents and origin were not inspected. | Treat the items as possibly vendor-provided and leave them untouched until a later configuration gate defines a narrow cleanup procedure. |

## D-098 Lite transition and readback

- Selected Lite on monthly billing inside the existing no-billing trial.
- Pipedrive initially carried LeadBooster, Projects, and Smart Docs into the change summary, producing a `$110` estimated post-trial total. All three add-ons were turned off before confirmation.
- Confirmed the plan change only after the order summary showed Lite at `$24` for one seat with no selected add-ons.
- Returned to Billing overview and directly verified `Lite`, `1 seats (1 in use)`, `14-day free trial`, `$24`, and `$0`.
- The active-add-ons section and `INCLUDED` labels were gone. LeadBooster, Campaigns Standard, Smart Docs, and Projects appeared only as optional `View trial offer` items.
- Billing details remained absent, and no payment or paid commitment was made.
- The exact calendar expiration date still was not displayed; the remaining-trial label continued to show `14-day free trial`.
- The Activities navigation count changed from three to four after the plan transition. No activity record was opened or inspected, so its origin remains unverified; all preloaded content remains untouched.

## Actions deliberately not taken

- Did not enter billing information, accept a paid commitment, or activate an add-on.
- Did not create, open, edit, import, delete, or inspect any contact, deal, activity, or other record.
- Did not configure fields, stages, filters, views, automations, permissions, integrations, email, calendar, maps, or mobile behavior.
- Did not invite Loryn or use real customer, employer, Costco, or Centah data.

## Disposition

The D-098 plan-boundary gate is complete. The tenant now exposes Lite with no active add-ons, no billing details, and the 14-day trial label preserved. This resolves the Premium-contamination blocker but does not prove configuration viability or any mandatory gate.

Recommended next gate: obtain the separately required `Begin P1-W03 synthetic configuration` authorization before inspecting or cleaning preloaded records, configuring the approved field and lifecycle model, entering synthetic fixtures, or running tests.
