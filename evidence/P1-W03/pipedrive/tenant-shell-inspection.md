# P1-W03 Pipedrive Tenant-Shell Inspection

**Status:** Read-only account-shell and plan-boundary inspection complete; Premium trial contamination confirmed; no plan change or configuration authorized

**Candidate:** Pipedrive

**Inspected:** August 1, 2026

## Authorized scope

This inspection used the bounded D-097 authority to confirm only nonprivate account-shell, trial, plan, expiry, and feature-boundary labels. It did not authorize configuration, synthetic fixture entry, testing, an edition change, billing, a purchase, an external connection, real data, customer communication, production use, or Loryn participation.

## Direct tenant findings

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

## Actions deliberately not taken

- Did not select Lite, continue through a plan-change flow, or save a subscription change.
- Did not enter billing information, accept a paid commitment, or activate an add-on.
- Did not create, open, edit, import, delete, or inspect any contact, deal, activity, or other record.
- Did not configure fields, stages, filters, views, automations, permissions, integrations, email, calendar, maps, or mobile behavior.
- Did not invite Loryn or use real customer, employer, Costco, or Centah data.

## Disposition

The D-097 account-shell gate is complete, but the approved stopping rule has been reached. The trial currently exposes Premium and included add-ons, so P1-W03 cannot begin Lite configuration without a separate authorization to change the no-billing trial from Premium to Lite and then verify the resulting plan boundary.

Recommended next gate: authorize only a Premium-to-Lite trial change with no billing information, followed by a read-only confirmation that Lite is active and the remaining trial is preserved. If the change requires billing, a paid commitment, or an unexpected loss of the trial, stop without proceeding.
