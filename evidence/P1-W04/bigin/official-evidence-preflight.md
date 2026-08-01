# P1-W04 Bigin Official-Evidence Preflight

**Status:** Current official evidence; outcome approved as D-100; contract approved as D-101; all external actions unapproved

**Candidate:** Bigin by Zoho CRM

**Proposed evaluated tier:** Premier

**Reviewed:** August 1, 2026

## Preliminary disposition

Bigin Premier is the strongest remaining candidate for a bounded P1-W04 evaluation. It is designed for smaller operations, its official field and workflow controls directly target the two failures that eliminated Pipedrive Lite, and its current two-administrator price is lower than the documented Zoho CRM Professional and Freshsales Pro possibilities. D-100 approved the evidence-first outcome and D-101 approved the complete contract. The conservative field map fits within documented Premier limits, but Bigin is not yet viable or selected and direct synthetic proof remains mandatory.

## Evidence summary

| Area | Current official evidence | P1-W04 effect |
|---|---|---|
| Pricing and trial | Premier is `$15` per user monthly or `$12` per user per month billed annually. The trial lasts 15 days, requires no credit card, does not charge automatically, and falls back to Free. | Two-administrator baseline is `$30` monthly or `$288` annually before applicable tax/add-ons. Exact tenant checkout and renewal remain unverified. |
| Tier boundary | Express has 10 custom fields per module. Premier has 25, five Team Pipelines, Stage Transition Rules, advanced date automation, duplicate cleanup, and 100,000 records. | Express is below the 16-field job baseline before default-field reuse; Premier is the lowest plausible tier. |
| Record and source model | Team Pipelines support distinct business processes with their own fields, record types, stages, sub-pipelines, and permissions. Pipeline records link to contacts and expose activities, notes, files, and history. | Plausible reusable-customer/multiple-job model and a clean Costco-versus-Independent branch; direct cross-pipeline usability is required. |
| Field capacity | Premier permits 25 custom fields per module. Bigin fields include dates, date-times, picklists, checkboxes, lookup, user, formula, and unique values. | Conservative documentation fit: 10 Contact, 15 Pipeline, and at most 2 Task custom fields; direct tenant confirmation remains required. |
| Handoff enforcement | Premier Stage Transition Rules can require fields, notes, files, or checklists before stage movement and can restrict closure from selected stages. | Strongest current evidence for M-02 and M-07; both handoff branches and installation anchors still require direct testing. |
| Duplicate control | Custom fields can prohibit duplicate values, and Premier adds duplicate cleanup. | A Deal/Pipeline Centah identifier appears capable of blocking duplicates; TS-03 must verify manual entry and import. |
| Action visibility | Custom list views, customizable dashboards, tasks/events/calls, dashboard drill-down, and mobile calendar agenda/day/week/month views are documented. | Plausible M-01 and M-04 path; one practical morning action center remains unverified. |
| Mobile | Official Android/iOS documentation covers dashboards, contacts, advanced filtering, activities, and calendar views. | Promising for Loryn's daily work, but phone/last-name search, directions, notes, timing, and weak-signal behavior require direct testing. |
| Administration | Paid editions support multiple users; roles, profiles, invitations, deactivation, and deletion are documented. | Plausible two-administrator model; MFA, exact permissions, removal history, and recovery remain unverified. |
| Portability | Module/view exports produce CSV files; notes can be exported by parent module. Paid editions include two full data backups per month. APIs and developer tools are listed across editions. | Plausible manual Centah bridge and exit path; relationship reconstruction and API limits remain unverified. |

## Alternative screened

Freshsales Pro remains a plausible fallback because official documentation supports unique Deal fields, required fields, field dependencies, mobile offline records, and a no-credit-card 21-day trial. Field dependencies are unavailable on Free and Growth, making Pro the lowest plausible source-specific tier at `$39` per user per month billed annually. Bigin Premier is recommended first because it is more right-sized and materially less expensive while documenting equivalent decision-critical controls.

## Mandatory pre-account checks

- The conservative CP-003 field map is documented in `field-capacity-preflight.md`: 10 Contact, 15 Pipeline, and at most 2 Task custom fields. Direct tenant confirmation remains mandatory.
- Confirm whether separate Team Pipelines or sub-pipelines best preserve one morning action center and reusable customer history.
- Verify exact Premier trial behavior and ensure Bigin 360-only capabilities cannot contaminate evidence.
- Confirm stage-rule, unique-field, custom-view, mobile, export, user, MFA, retention, and API limits by tier.
- Define narrow sample-data inspection and cleanup before any synthetic fixture load.

## Official sources reviewed

- [Bigin pricing and edition comparison](https://www.bigin.com/pricing.html)
- [Bigin modules and custom-field limits](https://help.zoho.com/portal/en/kb/bigin/customization/articles/modules-and-fields)
- [Bigin default fields by module](https://help.zoho.com/portal/en/kb/bigin/customization/articles/default-fields-bigin)
- [Bigin custom fields](https://help.zoho.com/portal/en/kb/bigin/modules/pipelines/articles/add-custom-fields-9-2-2019)
- [Bigin Team Pipelines](https://help.zoho.com/portal/en/kb/bigin/team-pipelines/articles/team-pipelines)
- [Bigin Pipeline records](https://help.zoho.com/portal/en/kb/bigin/modules/pipelines/articles/pipeline-records)
- [Bigin Team Pipelines and stage FAQ](https://help.zoho.com/portal/en/kb/bigin/faqs/trouble-shooting-faqs/articles/pipelines-sub-pipelines-stages-and-stage-transition-rules)
- [Bigin Stage Transition Rules](https://help.zoho.com/portal/en/kb/bigin/automation/articles/stage-transition-rules)
- [Bigin workflow rules](https://help.zoho.com/portal/en/kb/bigin/automation/articles/workflows)
- [Bigin import and unique-field behavior](https://help.zoho.com/portal/en/kb/bigin/data-administration/articles/import-records)
- [Bigin data export](https://help.zoho.com/portal/en/kb/bigin/data-administration/articles/exporting-data)
- [Bigin data backup](https://help.zoho.com/portal/en/kb/bigin/data-administration/articles/data-backup)
- [Bigin user management](https://help.zoho.com/portal/en/kb/bigin/explore-settings/articles/managing-users)
- [Bigin mobile dashboards](https://help.zoho.com/portal/en/kb/bigin/mobile-1/android/viewing-dashboards/articles/viewing-dashboards-in-android)
- [Bigin Android contacts](https://help.zoho.com/portal/en/kb/bigin/mobile-1/android/contacts-module/articles/viewing-contacts-in-android)
- [Bigin mobile calendar FAQ](https://help.zoho.com/portal/en/kb/bigin/mobile/ipad/frequently-asked-questions)
- [Freshsales pricing](https://www.freshworks.com/crm/pricing/)
- [Freshsales field dependencies](https://crmsupport.freshworks.com/support/solutions/articles/50000002573-how-to-configure-field-dependency-)
- [Freshsales unique fields](https://crmsupport.freshworks.com/support/solutions/articles/50000002578-how-to-use-unique-fields-to-prevent-duplicate-records-in-freshworks-crm-)
- [Freshsales mobile offline behavior](https://crmsupport.freshworks.com/support/solutions/articles/50000002950-how-to-use-the-mobile-app-offline-)
