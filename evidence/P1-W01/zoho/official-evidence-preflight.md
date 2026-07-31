# P1-W01 Zoho Official-Evidence Preflight

**Status:** Complete for the closed documentation-only Zoho result

**Evidence checked:** July 30, 2026

**Prototype tier:** Zoho CRM Free

**Organization label:** Hazel Kaine

## Scope and evidence rule

This preflight separates current Zoho Free capabilities from paid-tier possibilities. It does not authorize a paid trial, upgrade, purchase, integration, production use, real data, or customer communication. Account credentials, private email addresses, identifiers, MFA details, and recovery information are intentionally excluded.

## Current evidence inventory

| Topic | Free evidence | P1-W01 interpretation | Status |
|---|---|---|---|
| Edition and users | Zoho describes Free as free for up to three users. | The two-person administrator model fits the Free user-count ceiling. The account handoff confirmed Free Edition, and the tenant directly showed the edition-consistent disabled custom-module and custom-field controls. No billing or trial control was opened. | Official evidence and sanitized tenant behavior verified |
| Administrators | Zoho's Free-user documentation states that Free users have the Administrator profile and CEO role. | Loryn and the technical partner can both administer the prototype. The account setup handoff separately confirmed both administrator roles without recording private account details. | Official evidence and non-sensitive handoff verified |
| MFA | Zoho Accounts supports self-configured MFA and organization-enforced MFA. | Loryn's MFA setup was confirmed during account setup. No MFA screen, code, method, secret, recovery code, or private identifier is recorded. | Official evidence and non-sensitive handoff verified |
| Standard CRM records | Free includes Leads, Contacts, Accounts, Deals, Tasks, Meetings, Calls, Notes, standard reports, and mobile apps. | The prototype can represent prospects, customers, jobs, and activities using standard modules. | Verified |
| Custom fields | Free has no custom fields. Standard has 10 custom fields per module; Professional has 155 per module. | Free cannot implement the CP-003 minimum field set. The Deal/job model alone needs more than 10 distinct nonstandard fields, so Standard is also insufficient without collapsing approved data into notes or unrelated fields. Professional is the lowest edition with an evidence-backed field allowance large enough for the approved model. In the tenant, all new-field types were disabled and the field listing contained only standard fields. | Official and tenant-confirmed Free limitation; paid-tier possibility only |
| Custom list views | Free supports five custom list views per module. | The numeric allowance matches the five named prototype views, but a single cross-module morning action center and the required criteria remain unverified until in-product screening. | Partially verified |
| Workflow rules | Free supports workflow rules, with current limits shown as 10 rules per module and no more than five active. | Manual tasks and reminders can be screened. No automated customer communication will be configured. | Verified with scope restriction |
| Import | Free imports up to 1,000 records per batch. | The seven preload fixtures are below the limit. Import remains optional; only the approved synthetic records may be imported. | Verified |
| Module export | Free supports module export up to 200,000 records per module and up to 10 exports per day. | A small synthetic portability check is available without an upgrade. Any reviewed export must contain only approved fixtures. | Verified |
| Complete backup | Zoho's current edition comparison lists a paid per-request backup on Free, while module export remains available. | P1-W01 will not purchase backup service. This is a cost and recoverability limitation, not an authorization to upgrade. | Verified limitation |
| API/integration path | Free exposes 5,000 API calls per day; current feature documentation also warns that integrations may require paid licenses. | This is evidence that a future technical bridge is possible in principle, not evidence that Centah exposes a compatible interface. No API, webhook, email, calendar, maps, Centah, or other connection is authorized. | Zoho side verified; Centah side unverified |
| Expected production cost | Current official USD comparison lists Standard at $14/user/month billed annually or $20 month-to-month, and Professional at $23/user/month billed annually or $35 month-to-month, before local taxes. | For two full administrators, the evidence-backed Professional field-capacity path is $46/month on annual billing or $70 month-to-month, before tax. This is documentation only and is not a purchase recommendation. | Verified from current official comparison; recheck before any future purchase |

## Minimum-field capacity finding

Zoho Free cannot pass the CP-003 minimum-field gate because it permits no custom fields. Standard's 10-field-per-module allowance is also below the approved Deal/job requirement: even after using appropriate standard fields and related activities, the model still needs distinct storage for the service address, source detail, unique Costco/Centah identifier, next-action due time, quote-sent date, acceptance date, DocuSign-sent date, coordinator-email date, installation status, installation-confirmed date, post-install follow-up date, post-install result, and exception or stall reason. These items must not be silently collapsed into notes because the approved scenarios require clear fields, filtering, source rules, or dated exceptions.

Professional's 155 custom fields per module is the lowest currently documented Zoho CRM allowance that is clearly large enough. This supports only a `Conditional Pass` possibility until the exact model, views, mobile behavior, duplicate controls, exports, and scenarios are tested on an authorized tier. P1-W01 will not activate or purchase that tier.

## Vendor sample-data removal method

Zoho's official data-administration FAQ documents this path:

1. Open **Setup**.
2. Open **Data Administration**.
3. Select **Remove Sample Data**.
4. Confirm only when the dialog explicitly identifies Zoho sample data.

Removal is scheduled by Zoho. P1-W01 authorization covers only the vendor sample records created during account setup. If the product does not clearly isolate those records, stop without deleting anything.

## Sanitized tenant observations

Observed in the authorized `Hazel Kaine` tenant on July 30, 2026 without capturing credentials, private email addresses, account identifiers, billing information, or MFA details:

- The user-administration view contained two distinct active rows with the Administrator profile.
- `Create New Module` was disabled.
- The Deal layout exposed only the standard fields `Account Name`, `Amount`, `Campaign Source`, `Closing Date`, `Contact Name`, `Created By`, `Deal Name`, `Deal Owner`, `Description`, `Expected Revenue`, `Lead Source`, `Modified By`, `Next Step`, `Probability (%)`, `Reason For Loss`, `Stage`, and `Type`.
- Every new-field type in the Deal layout palette was disabled. No field was created and no paid trial or upgrade prompt was accepted.
- Zoho's removal dialog stated that it would remove the sample data and warned that changes made to that sample data would be lost. After the authorized confirmation, Zoho reported that removal had been scheduled.
- After processing, Leads showed zero records and no `(Sample)` entries remained in Leads, Contacts, Accounts, Deals, Tasks, Meetings, or Calls. No unrelated record deletion was performed.
- The Stage-Probability Mapping screen was available and showed editable standard sales stages, but no stage changes were saved. The approved model depends on additional CP-003 fields that Free cannot create, so saving a partial lifecycle would produce a misleading prototype.

## Sources

- [Zoho CRM Free Edition overview](https://www.zoho.com/crm/what-is-zoho-crm-free-edition.html)
- [Zoho CRM current feature comparison](https://www.zoho.com/crm/complete-feature-list.html)
- [Zoho CRM current pricing page](https://www.zoho.com/crm/zohocrm-pricing.html)
- [Current Zoho CRM and Bigin edition comparison PDF](https://www.zoho.com/sites/default/files/bigin/bigin-zohocrm-editions-comparison.pdf)
- [Zoho CRM user FAQ](https://help.zoho.com/portal/en/kb/crm/faqs/security-administration/users/articles/faqs-users)
- [Zoho Accounts MFA introduction](https://help.zoho.com/portal/en/kb/accounts/multi-factor-authentication/articles/mfa-introduction)
- [Zoho CRM custom fields](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-fields/articles/use-custom-fields)
- [Zoho CRM import FAQ](https://help.zoho.com/portal/en/kb/crm/faqs/data-administration/import/articles/faqs-import)
- [Zoho CRM module export](https://help.zoho.com/portal/en/kb/crm/data-administration/export-data/articles/export-crm-data)
- [Zoho CRM complete data backup](https://help.zoho.com/portal/en/kb/crm/data-administration/data-backup/articles/requesting-data-backup)
- [Zoho CRM sample-data removal FAQ](https://help.zoho.com/portal/en/kb/crm/faqs/data-administration/general/articles/faqs-data-administration)

## Open evidence items

- If a future purchase is considered, recheck the live edition label and price immediately before authorization; the current configuration-viability result already confirms the Free feature boundary without opening billing.
- Determine whether the five Free views can expose the approved conditions without custom fields and whether a practical cross-module morning equivalent exists.
- Test only the standard-field subset that Free actually supports; record unsupported fields rather than repurposing unrelated fields.
- Verify mobile behavior, duplicate handling, exports, and applicable mandatory gates only while the candidate remains viable under the approved stopping rule.
