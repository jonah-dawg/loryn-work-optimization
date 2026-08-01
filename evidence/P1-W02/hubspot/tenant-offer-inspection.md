# P1-W02 HubSpot Tenant Offer Inspection

**Status:** Direct tenant evidence; read-only inspection complete; no activation or purchase

**Candidate:** HubSpot CRM

**Inspected:** August 1, 2026

**Tenant boundary:** Evaluator-only `Hazel Kaine` synthetic tenant; private identifiers omitted

## Inspection scope

Inspect the signed-in tenant's current edition and available Starter-equivalent offer without creating records, changing configuration, connecting services, entering billing information, activating a trial or tier, or purchasing anything.

## Confirmed tenant state

- Account & Billing lists `Free Tools` and the free Marketing, Sales, Service, Content, and Data tools.
- The account remained on Free before and after the inspection.
- The upgrade comparison identifies `Free tools` as the current plan.
- No active trial, paid subscription, or Starter entitlement was displayed.

## Available Starter offer

- The offered product is `Starter Customer Platform` with `Core Seats (Starter)`.
- The upgrade page advertises a limited new-customer promotion starting at `$7/mo/seat`, described as up to 65% off and available with monthly or annual subscription choices.
- The plan configurator defaulted to one Core Seat at `$7/mo/seat`.
- Checkout displayed a `$20.00` base monthly amount and a `$7.00/mo` promotional amount.
- The default selected term was `Pay Annually`. Checkout showed `$240.00` billed annually, a `New Customer Starter Promotion Annual (65%)` discount of `$156.00`, and `$84.00` due immediately before tax.
- A `Pay Monthly` option labeled `Monthly commit` was visible, but its exact immediate total, future renewal price, and complete term were not selected or verified.
- Checkout required company address fields before the payment section and displayed a separate secure payment-details step.
- No `Start trial`, no-billing evaluation, delayed-charge evaluation, or Starter-equivalent trial option appeared in the inspected account, upgrade, plan-configuration, or checkout screens.
- Renewal pricing after the promotion was not disclosed on the inspected screens.

## Safety and privacy result

- No company address beyond the approved organization name was entered.
- No payment information was entered or saved.
- No purchase, subscription, trial, tier activation, external connection, CRM configuration, fixture entry, test, communication, or production action occurred.
- Checkout was abandoned and the browser was returned to the `Free Tools` Account & Billing overview.
- No credentials, private email addresses, account identifiers, session details, screenshots, or private notifications are stored in this artifact.

## Contract disposition

The direct tenant does not expose the clean no-billing Starter-equivalent evaluation required by the approved P1-W02 path. Under the stopping rule, HubSpot configuration and synthetic scenario testing must not begin from this Free tenant.

The next decision must select one of these separately gated outcomes:

1. Retain HubSpot Starter as documentation-only.
2. Authorize a separately scoped paid evaluation or purchase only after exact monthly checkout, renewal, tax, and total-cost review.
3. Close HubSpot incomplete and screen the next CRM candidate.

HubSpot Free remains `Fail` for M-07 and M-13 because its 10-custom-property total cannot represent the approved baseline. Starter remains a documentation-backed `Conditional Pass` possibility, not a tested candidate score or platform recommendation.
