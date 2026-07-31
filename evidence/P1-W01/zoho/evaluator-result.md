# P1-W01 Zoho Evaluator Result

**Status:** Closed incomplete by D-088 option 1 - documentation-only paid-tier possibility; no CP-005 approval

**Candidate:** Zoho CRM

**Directly evaluated tier:** Free

**Paid-tier evidence path:** Professional, documentation only

**Evaluation date:** July 30, 2026

**Evaluator:** Technical-partner session with Codex-assisted in-app browser control

**Device and application:** Windows desktop; in-app browser version not exposed

**Fixture reset confirmation:** Vendor sample data removed; approved fixtures not loaded because Free cannot represent their required baseline

## Outcome

Zoho Free cannot host the approved P1-W01 prototype faithfully because it provides no custom fields. The CP-003 workflow requires distinct, filterable, dated, source-specific, and unique job fields that do not exist among the 17 standard Deal fields. Entering the fixtures would therefore omit required facts or hide them in notes or unrelated fields, invalidating the common evidence standard.

Zoho Professional is the lowest current edition with clearly sufficient documented field capacity: 155 custom fields per module. For two full administrators, the current official USD comparison lists $46/month on annual billing or $70 month-to-month, before local taxes. This is a paid-tier possibility only. No trial, upgrade, billing action, purchase, or recommendation is authorized.

The result is therefore `Incomplete`, not a Free-tier prototype pass and not a platform selection. D-088 option 1 retains Professional as documentation-only evidence and ends P1-W01 without paid-tier testing. Direct field, view, fixture, scenario, export-relationship, mobile, save/sync, and administration results remain unverified.

## Configuration-viability evidence

- The vendor-only sample-removal dialog was verified before confirmation. Zoho scheduled the removal, and the checked CRM modules no longer contain `(Sample)` records.
- Two distinct active Administrator rows were observed without recording names, email addresses, or account identifiers.
- `Create New Module` was disabled.
- All new custom-field types in the Deal layout were disabled.
- Only the standard Deal fields listed in `configuration-inventory.md` were available.
- Stage-Probability Mapping was editable, but no partial stages were saved because the supporting CP-003 fields cannot be created on Free.
- No real data, incomplete fixture, external connection, message, paid trial, billing action, upgrade, or purchase was created.

## Mandatory-gate record

The Free result and paid-tier possibility are stated separately. A paid-tier `Conditional Pass` never counts as a verified pass.

| ID | Result | Time or friction | Evidence reference | Limitation or uncertainty | Confidence |
|---|---|---|---|---|---|
| M-01 | Free: `Fail`; Professional: `Unverified` | Preflight stopped before view configuration | `configuration-inventory.md`; `official-evidence-preflight.md` | Free cannot store the fields needed to distinguish waiting, installation exceptions, or complete missing-next-action conditions. Professional has sufficient fields and list-view capacity, but the required practical cross-module action center is untested. | High for Free; Low for Professional |
| M-02 | Free: `Fail`; Professional: `Conditional Pass` | Configuration viability only | Same evidence plus current feature comparison | Free cannot create a unique opportunity-level Centah number or distinct source-specific dates and handoff fields. Professional has sufficient fields and validation-rule capacity, but the exact source rules are untested. | High / Medium |
| M-03 | `Unverified` | No mobile timing run | No direct evidence | The approved baseline cannot be loaded on Free, so one-minute task timing would not be comparable. | High |
| M-04 | Free: `Fail`; Professional: `Conditional Pass` | Configuration viability only | `configuration-inventory.md` | Free cannot represent all quote, handoff, installation, and exception dates or states needed for reliable reminders. Professional has sufficient field/workflow limits, but direct behavior is untested. | High / Medium |
| M-05 | `Conditional Pass` | Account setup and sanitized user check | `official-evidence-preflight.md` | Two active administrators and MFA are verified. Prompt removal, practical permissions, and preserved activity history still need a bounded direct check. | Medium |
| M-06 | `Conditional Pass` | Official evidence only | `official-evidence-preflight.md` | Free module export is available, but complete backup is paid per request. Relationship reconstruction, note/activity completeness, deletion behavior, and subscription exit have not been directly tested. | Medium |
| M-07 | Free: `Fail`; Professional: `Conditional Pass` | Direct field and layout observation | `configuration-inventory.md`; `official-evidence-preflight.md` | Free has no custom fields and cannot store CP-003. Standard's 10 custom fields/module is also below the job requirement. Professional's 155-field allowance is sufficient on paper; exact configuration remains untested. | High / Medium |
| M-08 | Free: `Fail`; Professional: `Conditional Pass` | Configuration viability only | Same evidence | Free cannot distinctly record approved permission, preferred-channel, opt-out, unresolved-problem, and suppression information. Professional has sufficient fields; the no-send and suppression workflow remains untested. | High / Medium |
| M-09 | Free: `Fail`; Professional: `Conditional Pass` | Configuration viability only | Same evidence | Free cannot create the unique Deal-level Centah identifier. Professional documents unique custom fields, but duplicate review, import/reconciliation, and the Centah-side interface remain untested or unresolved. | High / Medium |
| M-10 | `Unverified` | No cross-device or weak-signal test | No direct evidence | Save confirmation, retry, duplicate prevention, pending state, and phone/desktop consistency were not tested. | High |
| M-11 | `Pass` | Official evidence preflight | `official-evidence-preflight.md` | Professional is the lowest field-capacity tier; two-user cost is $46/month annually billed or $70 month-to-month before tax. Prices and packaging require recheck before any future purchase. | High |
| M-12 | `Unverified` | No guided-use or maintenance trial | No direct evidence | Learning time, weekly cleanup, and ordinary admin effort cannot be inferred from field limits. | High |
| M-13 | `Unverified` | Common scenarios not run | `synthetic-fixtures.csv`; CP-004 scripts | The common fixture baseline cannot be represented on Free; no exception to the common evidence standard is approved. | High |

## Weighted-score status

The weighted total is intentionally incomplete. No mobile or scenario score is assigned, and the documented governance, portability, and cost observations are not normalized into a partial total. Mandatory Free failures and unverified direct evidence prevent Zoho from being preferred at this point.

## Approved disposition and next work unit

On July 31, 2026, the user explicitly approved D-088 option 1:

- Keep Zoho as a documentation-only Professional-tier possibility.
- Do not start a Zoho paid trial, upgrade, or purchase.
- Close P1-W01 incomplete without CP-005.
- Move only to definition of the next CRM comparison work unit.

This disposition does not approve a HubSpot or other candidate account, configuration, integration, customer data, communication, purchase, finalist test, or platform selection.
