# P1-W03 Pipedrive Evaluator Result

**Status:** Prepared under D-099 - proposed Lite elimination; CP-007 not signed

**Candidate:** Pipedrive

**Directly evaluated tier:** Lite in a no-billing trial

**Evaluation date:** August 1, 2026

**Evaluator:** Technical-partner session with Codex-assisted Chrome control

**Device and application:** Windows desktop; Chrome version not exposed

**Fixture reset confirmation:** Vendor sample data removed; seven approved preload fixtures imported; temporary TS-01 and duplicate-test records removed after the run; baseline scenario changes remain and require reset before another run

## Proposed outcome

Pipedrive Lite is proposed as `Eliminated`. It can represent the baseline at 25 of 30 custom fields and provides useful search, activities, pipeline stages, filters, and desktop task visibility. However, two directly observed mandatory failures make the evaluated tier nonviable:

1. M-02 fails because Lite cannot conditionally require the Costco/Centah versus Independent handoff fields, hide false-source fields, prevent premature handoff completion, or produce the required source-specific installation anchor.
2. M-09 fails because a duplicate Deal using the existing synthetic Centah lead number was accepted without a block or visible duplicate-review route.

The approved stopping rule ends further evaluator testing after a confirmed mandatory failure. Native mobile timing, cross-device save behavior, and downloaded-export reconstruction therefore remain unverified and no weighted score is calculated. This result does not approve CP-007, select a platform, authorize Loryn testing, or permit billing, production use, integrations, real data, or customer communications.

## Scenario result summary

| Scenario | Result | Direct observation | Remaining uncertainty |
|---|---|---|---|
| TS-01 quick prospect | Desktop `Pass`; mobile `Unverified` | Created a fictional Lead with name, phone, Referral source, and dated call; found it again; removed the Lead and Person after testing. | No phone timing, tap count, or mobile save test. |
| TS-02 morning action center | `Partial / Unverified` | Today and Overdue activity states plus `Missing Next Action` and `Waiting on Others` filters exposed all five conditions; phone and last-name search found the correct customer and job. | The five states were not combined on one screen, so M-01 is not treated as passed. |
| TS-03 Costco/Centah lead | `Fail` | Source and Deal-level identifier were visible and a dated first-contact activity was saved; a second Deal with `SYN-CENTAH-1001` was accepted silently. | No reliable native duplicate-review route was found in the tested Lite workflow. |
| TS-04 appointment | Desktop `Partial`; mobile `Unverified` | Customer, appointment, phone, preferred method, context, and service address were reachable. Clicking the desktop address entered edit mode rather than opening directions. No message was sent. | Manual composer flow, mobile directions, and one-minute timing were not tested. |
| TS-05 visit and quote | Desktop `Pass` | Added a synthetic visit note and `$4,250` value; retained the quote-sent date, manual-notice notation, and visibly overdue dated follow-up. | Mobile note entry and cross-device save were not tested. |
| TS-06 accepted-sale handoff | `Fail` | Both records stored the fields and explicit handoff activities, but Lite exposed the same fields on both sources and allowed blank or false-source handoff data. | No conditional enforcement, premature-completion block, or automatic source-specific anchor was available in the tested configuration. |
| TS-07 installation exception | Desktop `Partial` | Three-month exception, fictional unconfirmed result, same-day coordinator task, and unconfirmed installation state were visible; no automatic completion occurred. | Customer-contact prompting and mobile visibility were not tested. |

## Mandatory-gate record

| ID | Result | Evidence | Limitation or uncertainty | Confidence |
|---|---|---|---|---|
| M-01 | `Unverified` | Native Today/Overdue activities; two saved Deal filters; TS-02 | All five states were reachable but not combined into one practical screen. | Medium |
| M-02 | `Fail` | Direct TS-03 and TS-06 observations; `configuration-inventory.md` | Source can be stored, but Lite cannot enforce unique Costco-only identifiers, source-specific handoff requirements, or installation anchors. | High |
| M-03 | `Unverified` | Desktop checks only | No parked-phone timing run occurred. | High |
| M-04 | `Pass` | Activities list, overdue quote, handoff and installation tasks, missing-next-action filter | Directly verified on desktop with synthetic records; notification delivery was not separately tested. | Medium |
| M-05 | `Conditional Pass` | `official-evidence-preflight.md`; `tenant-shell-inspection.md` | Two-administrator production roles, MFA, removal, permissions, and history were not directly tested in this one-seat evaluator tenant. | Low |
| M-06 | `Unverified` | Server-side export generation | Entity exports were generated, but the download was blocked by Chrome and contents or relationships were not inspected. | High |
| M-07 | `Pass` | 25-field map, People-to-Deals model, pipeline, retained reasons, Leads Inbox, missing-next-action filter | Lite uses visible exception reporting rather than hard required fields. | High |
| M-08 | `Unverified` | Manual-only configuration and permission fields; no-send tests | No communication was sent, but opt-out suppression and composer behavior were not fully tested. | Medium |
| M-09 | `Fail` | Direct TS-03 duplicate attempt | Duplicate Deal with the same Centah number was accepted without a block or visible review route. | High |
| M-10 | `Unverified` | Desktop save observations only | No phone/desktop, weak-signal, pending-state, retry, or duplicate-activity test occurred. | High |
| M-11 | `Conditional Pass` | Official `$14` annual and direct `$24` monthly per-seat labels | Exact two-administrator checkout, renewal, tax, and commitment terms remain unverified. | Medium |
| M-12 | `Unverified` | Evaluator desktop setup only | No guided Loryn session or representative weekly-administration measurement occurred. | High |
| M-13 | `Pass` | CP-004 fixtures and TS-01 through TS-07; synthetic-only run | The run stopped after mandatory failures, as the approved method requires. | High |

## Export and cleanup evidence

- Pipedrive generated XLSX exports for Deals (7 items), Activities (7 items using Date added), and the other tested entities. A zero-item Activities export created with the wrong date filter was superseded.
- The vendor-hosted download was blocked with `ERR_BLOCKED_BY_CLIENT`; no exported file was committed or inspected.
- The temporary Lead and Person and the duplicate Deal and Person were deleted. The active People list returned to seven baseline synthetic records.
- Deleted records remain recoverable in Pipedrive for 30 days. The prospect activity may remain unlinked, and the baseline fixtures plus scenario changes require reset before another run or tenant closeout.

## Weighted-score status

The weighted total is intentionally incomplete. Mandatory failures M-02 and M-09 already prevent Pipedrive Lite from being preferred, and assigning preference scores to untested mobile, reliability, administration, or export behavior would create false precision.

## Approval boundary

This prepared result is unapproved. CP-007 would approve only this Pipedrive evaluator result, configuration inventory, tier/cost record, and evidence-backed comparison status. It would not select Pipedrive, authorize a purchase or production use, connect Centah or another service, permit real data or customer communications, start a Loryn finalist session, or authorize the next candidate.
