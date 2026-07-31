# P1-W01 Zoho Configuration Inventory

**Status:** Closed at the Free field-capacity blocker; retained as documentation-only evidence

**Authorized tier:** Zoho CRM Free only

**Configuration rule:** Configure supported standard behavior; record limitations instead of starting a trial, upgrading, purchasing, or hiding approved data in unrelated fields.

## Planned standard-module mapping

| Approved record | Zoho standard module | Free disposition |
|---|---|---|
| Prospect | Leads | Available; required prospect-governance fields are only partially available without custom fields. |
| Customer/contact | Contacts, with Accounts only when a business identity requires one | Available; one contact can relate to multiple Deals/jobs. Required permission, preference, state, and opt-out fields are not fully available in Free. |
| Opportunity/job | Deals | Available; standard Stage, Amount, Lead Source, Closing Date, Next Step, Contact, and Account fields cover only part of CP-003. The remaining approved job fields require custom fields. |
| Task/activity | Tasks, Meetings, Calls, and Notes | Available; test due dates, status, reminders, history, appointment context, and manual-only communications. |

## Configuration checklist

| Item | Free target | Current result | Evidence or limitation |
|---|---|---|---|
| Confirm Free edition | Verify handoff and edition-consistent tenant controls without private account details | Confirmed | Account handoff says Free. Tenant directly disabled new custom modules and all new Deal field types; no billing or trial page was opened. |
| Remove Zoho vendor sample data | Use Setup > Data Administration > Remove Sample Data after exact target verification | Complete | Dialog explicitly targeted sample data. Removal was scheduled, then all checked CRM modules showed no remaining `(Sample)` records. This deletion is not recoverable through the prototype workflow. |
| Customer-to-multiple-jobs relationship | Contact related to multiple Deals | Available in the standard model; fixture verification blocked | Deal field listing includes the standard Contact and Account lookups. Full fixture verification is blocked by the missing approved job fields. |
| Prospect capture | Lead with name, phone, source, and dated follow-up task | Pending | Source and phone are standard; dated next action likely requires a related Task. |
| Independent/Costco source | Deal Lead Source | Partially available | `Lead Source` is a standard Deal picklist. Source-detail requirement remains unsupported. |
| Unique opportunity-level Centah number | Custom unique field on Deal only | Unsupported on Free | Free has no custom fields. Do not place the number on a Contact or bury it in Notes. |
| Full CP-003 job field set | Distinct Deal fields plus activities | Unsupported on Free | Tenant field listing contains only the 17 documented standard Deal fields and disables every new-field type. Standard also appears insufficient at 10 custom fields/module; Professional has adequate documented field capacity. |
| Approved stages | Use the standard Deal Stage field if Free permits stage editing | Available but deliberately not saved as a partial build | The Stage-Probability Mapping screen is editable. Saving stages without the approved supporting fields would create a misleading configuration, so the default stages were left unchanged. |
| Manual next action and due time | Standard Next Step plus a related Task | Structurally available; full rule unverified | `Next Step` is a standard Deal field and Tasks support due dates. Missing-next-action reporting and combined visibility remain unverified. |
| Today view | Custom list view or practical standard equivalent | Pending | Free allows five custom list views/module, but cross-module visibility is unverified. |
| Overdue view | Custom list view or practical standard equivalent | Pending | Field and criteria dependency unverified. |
| Waiting on Others view | Custom list view or practical standard equivalent | Pending | Approved state likely needs a stage or custom field. |
| Missing Next Action view | Custom list view or practical standard equivalent | Pending | Detection across active Deals and related Tasks is unverified. |
| Installation Exceptions view | Custom list view or practical standard equivalent | Pending | Required date/status fields are unsupported on Free. |
| Synthetic fixtures | Seven baseline records; TS-01 prospect absent | Not loaded | The Free tenant cannot represent the approved baseline without omitting or misplacing required fields. Source sheet: `synthetic-fixtures.csv`. No incomplete fixtures were entered. |
| Module export | Export only approved synthetic records | Pending | Officially supported on Free; full backup is paid per request. |
| External connections | None | Compliant | Email, calendar, maps accounts, Centah, API, webhooks, and other services remain disconnected. |
| Customer communication | Human-reviewed composer only; send nothing | Compliant | No outbound message is authorized. |

## Expected decision effect

If Free cannot meet a mandatory gate but Professional has exact feature, limit, and price evidence, record a paid-tier `Conditional Pass` possibility without activating it. If no acceptable production-tier path exists, apply the approved early-stop rule. P1-W01 does not select Zoho or authorize CP-005.

## Current configuration-viability outcome

Zoho Free cannot host the approved synthetic prototype faithfully. Entering fixtures now would either omit required CP-003 facts or conceal them in notes and unrelated standard fields, both of which would invalidate TS-02, TS-03, TS-05, TS-06, TS-07, M-02, M-04, M-07, and M-09. The tenant is therefore clean and intentionally left without partial lifecycle changes or incomplete fixtures.

Professional is the lowest edition with clearly sufficient documented field capacity, at $46/month for two administrators on annual billing or $70 month-to-month before tax under the current official USD comparison. That is a paid-tier `Conditional Pass` possibility only; no paid trial, upgrade, purchase, or recommendation is authorized. Remaining direct scenario and mobile evidence cannot be produced on the authorized Free tier.
