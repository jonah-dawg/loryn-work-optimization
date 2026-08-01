# Current Project State

**Updated:** August 1, 2026

**Overall status:** Active - P1-W04 Bigin evaluator result proposed; CP-008 review required
**Current phase:** Phase 1 - CRM candidate comparison
**Active work unit:** P1-W04 - Bigin Premier evidence-first screening

**Work-unit status:** D-103 evaluator run stopped on direct M-01 failure; proposed `Eliminated` result unapproved pending CP-008

**Last signed-off checkpoint:** CP-007 - Pipedrive Lite evaluator result (August 1, 2026)

**Last approval:** D-103 - begin the approved P1-W04 synthetic configuration and evaluator sequence (August 1, 2026)

## Confirmed baseline

- The product is a mobile-first workflow system for an independent window-covering sales consultant.
- Existing CRM products will be evaluated and configured before considering a custom application.
- Zoho CRM Free is the first prototype candidate; HubSpot Free and other approved CRMs may be compared. The current Centah-only workflow is a nonselectable reference baseline, not a candidate final system.
- The final platform must be a CRM that runs independent prospects and jobs outside Costco/Centah and supports an evidence-backed manual bridge or integration path for Costco-originated work.
- Centah remains authoritative for Centah-originated identifiers and governed fields until a later mapping decision changes that boundary.
- Each new order receives a new Centah lead number; store that identifier on the opportunity, not the reusable customer record.
- A returning customer may have multiple opportunities.
- Transfer only active and sold Centah leads; exclude canceled/inactive leads.
- Permitted transfer fields are name, phone, email, full address, Centah notes, appointments, quoted amount, and Centah lead number.
- Synthetic-only trials require no company permission. Real records are allowed in the selected production CRM only after access, security, retention, and export controls are configured.
- Real records remain prohibited from this ChatGPT Project, repository, documentation, tests, and trial fixtures.
- The initial post-sale workflow uses a six-week checkpoint after DocuSign. If installation is incomplete, add a note and defer by two to three weeks, repeating until installation is confirmed; then perform one post-install follow-up.
- Ongoing support and future repair-case management are outside the initial CRM scope.
- The project uses guided work units, explicit sign-off, durable checkpoints, and a simple two-person delivery model.
- The CRM must also support independently sourced leads and prospecting for possible future clients outside Centah/Costco.
- Confirmed prospecting sources include referrals, builders, networking, past customers, social media, purchased lists, local businesses, and direct outreach.
- A prospect may begin with a person name, business name, or social identity plus at least one reachable channel or location; source, next action, and follow-up date are always required.
- Approved prospecting activities are calls, texts, emails, social messages, in-person/networking conversations, mailed material, referral requests or introductions, research/preparation, and notes.
- Default reminder intervals are 2 days for engaged prospects, 7 days for warm prospects/referrals, 30 days for cold outreach or purchased-list prospects, 90 days for long-term prospects, and 6 months for past customers with possible future work; all are manually overridable and do not send automatically.
- A prospect converts when a real project is confirmed and the initial meeting is scheduled. The prospecting sequence closes as `Converted`, the customer and activity history remain intact, and one opportunity for that project begins at `Consultation Scheduled` with the morning-of confirmation as its next action. A direct inquiry about an immediate project may enter at this stage without first using prospecting.
- The approved active-job statuses are `New Customer Request`, `Trying to Contact`, `Appointment Scheduled`, `Appointment Completed`, `Preparing Quote`, `Quote Sent - Awaiting Decision`, `Customer Accepted - Handoff Due`, `Handoff Complete - Installation Pending`, `Installed - Customer Follow-Up Due`, and `Finished`. `Lost / Canceled` is an exit available where applicable, and an installation unconfirmed at three months becomes a visible exception.
- Calling hours are Monday through Friday from 9:00 a.m. to 6:00 p.m. and Saturday from 9:00 a.m. to 2:00 p.m. A new request received during those hours requires a manual first-contact attempt by closing time that day. A request received outside those hours is due at 9:00 a.m. on the next working day; Sunday rolls to Monday. The CRM creates a reminder and does not contact the customer automatically.
- After an unanswered first attempt on an active customer request, retry on the next working day. If unanswered again, make a third and final attempt two working days later. A third nonresponse closes the opportunity as `Lost / Canceled - No Response`; retain the record and notes and stop active-job reminders. Costco/Centah leads also follow the approved Centah cancel-to-inactive process. This does not change the separate long-term prospecting rules.
- For an appointment happening that day, create a reminder to send the manual confirmation text at approximately 7:45 a.m. This is a confirmation-text exception only. A confirmation phone call must wait until calling hours begin at 9:00 a.m.
- After a completed appointment that requires a quote, the primary goal is to finish and manually send the quote by the end of that same working day. If it is not sent by closing time, the quote task becomes visibly overdue and remains open until a new due date is recorded or the quote is sent.
- When the same-day quote target is missed, require a short delay reason and set the fallback deadline to the end of the next working day. A missed fallback stays overdue and requires another deliberate date and reason rather than being silently rescheduled.
- Immediately after emailing a quote, send a manual message through the customer's preferred and permitted channel telling them the quote was sent and asking them to check their email. Create the next manual decision-follow-up task for three working days later. If the customer responds first, cancel the reminder and record the response and resulting next action. No message is sent automatically.
- If the three-working-day post-quote follow-up receives no response, create another manual follow-up for one week later during normal calling hours and keep the opportunity at `Quote Sent - Awaiting Decision`.
- Continue unanswered quote follow-ups once a week for no more than three weeks. After the third weekly nonresponse, close the opportunity as `Lost / Canceled - No Decision`, retain the quote and communication history, and stop reminders. If the customer requests more time, use their requested date instead of the weekly schedule.
- When the customer accepts, complete the source-specific handoff by the end of that working day or by 9:00 a.m. on the next working day after an outside-hours acceptance. Costco/Centah requires both DocuSign and the quote emailed to the internal order coordinator; independent work skips DocuSign and requires only the coordinator email. Do not mark the handoff complete until all required items have actually been sent.
- After handoff, check installation at six weeks using the DocuSign-sent date for Costco/Centah work or the coordinator-email date for independent work. If installation is unconfirmed, add a note and check again in two to three weeks. At three months after the sold quote was emailed to the coordinator, stop normal deferral, show an urgent exception, contact the coordinator that day, and contact the customer if necessary. Never mark installation complete without human confirmation.
- After installation is confirmed, complete one manual customer follow-up by the end of the next working day. If the customer confirms everything is satisfactory, mark the job `Finished` and schedule the six-month past-customer reminder. If the customer reports a problem, keep it visibly unresolved with a next action and do not mark it finished; detailed repair-case management remains outside the initial CRM scope.
- If the customer does not answer the one post-install follow-up on a confirmed-installed job, record `Post-Install Follow-Up Attempted - No Response`, mark the job `Finished`, and stop post-install reminders. Schedule the six-month past-customer reminder only if the customer has not opted out and there is no known unresolved problem.
- The approved minimum CRM fields are assigned to customer/contact, opportunity/job, and task/activity records in `../deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`. Centah lead number is required and unique only for Costco/Centah jobs and prohibited for independent jobs.
- After acceptance, Centah/Costco opportunities require DocuSign and an emailed quote to the internal order coordinator in parallel. Opportunities outside Centah/Costco skip DocuSign and require only the emailed quote to the internal order coordinator.
- The six-week installation-check timer starts on the DocuSign-sent date for Centah/Costco sales and on the internal-order-email date for sales outside Centah/Costco.
- Installation should never take more than three months from the date the sold quote is emailed to the internal order coordinator; an unconfirmed installation at that boundary must become a visible exception rather than receiving indefinite routine deferrals.
- At the three-month exception, the CRM creates a same-day task to contact the internal order coordinator, requires a recorded result, prompts customer contact if the coordinator cannot confirm installation, and never marks installation complete without human verification.
- Prospect exit rules are approved: three unanswered attempts move the record to one 90-day nurture attempt; another nonresponse archives it. Declines, do-not-contact requests, invalid information, and duplicates use explicit retained outcomes.
- Prospect records will store preferred channel, acquisition source/date, permission status, overall do-not-contact information, and channel-specific opt-outs. Purchased-list imports and automated outreach require a later communications-compliance review.
- Eligible past customers enter prospecting six months after post-install follow-up for possible additional work and referrals, using a permitted letter, email, text, or call; opted-out customers and unresolved problems are excluded.
- Past-customer reminders may repeat at 6, 12, 18, and 24 months after post-install follow-up, then stop. An explicit rejection or opt-out ends the sequence immediately.
- Only Costco-originated opportunities use Centah. Independently sourced prospects and opportunities remain only in the selected CRM, are not entered into Centah, and do not require a Centah lead number.
- P0-W03 mandatory gates M-01 through M-13 are approved for the draft evaluation and recorded in `../deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`.
- The gates cover the daily action center, source-specific workflow, essential mobile speed, reminders, administration, portability, the approved record model, human-controlled communications, the Centah bridge, save reliability, cost evidence, sustainable administration, and a common synthetic evidence standard.
- Full offline capability remains a weighted preference; silent data loss or duplication is a mandatory failure.
- Loryn is the primary administrator and daily user. One secondary administrator provides occasional setup, troubleshooting, recovery, and other ad hoc administration.
- P0-W03 category weights total 100: mobile daily-work usability 35, workflow visibility and configuration 20, governance/security/administration 15, data portability and reliability 10, cost and maintenance burden 10, and Centah/integration fit 10.
- Mandatory gates override the weighted total; an applicable `Fail` or `Unverified` gate prevents a platform from being preferred.
- Weighted criteria use a common integer scale from 0 to 5 and contribute `criterion weight × score ÷ 5` to the 100-point total.
- Every score requires evidence and confidence. Missing evidence leaves the total incomplete and is never normalized away.
- The 35 mobile points are allocated as daily action center 10, essential task efficiency 10, customer/job search 5, appointment confirmation and directions 5, and mobile note capture and weak-signal behavior 5.
- The 20 workflow points are allocated equally across lifecycle/record configuration, next-action/overdue visibility, source-specific handoff/installation exceptions, and office workflow/activity/reporting.
- The 15 governance points are allocated 4/4/4/3 across secure account access, simple administration/access management, useful activity history, and retention/deletion guidance. Score only right-sized needs for a one-person operation; unused enterprise complexity earns no extra credit.
- The 10 portability/reliability points are allocated as usable data exports 4, understandable customer-to-job relationships after export 3, and saving/synchronization/recovery quality 3.
- The 10 cost/maintenance points are allocated as actual recurring cost for two administrators and required features 5, ongoing training/cleanup/support effort 3, and pricing clarity/forced-upgrade risk 2.
- The 10 Centah/integration points are allocated as practical Costco/Centah job and identifier handling 4, duplicate checking/reconciliation 3, and evidence-backed future import/export/API options 3. Unknown Centah capabilities remain unverified.
- All criterion-level weights now total 100.
- Seven common scenario areas are approved: quick prospect capture, morning action center, Costco/Centah lead handling, appointment workflow, visit/quote follow-up, both accepted-sale handoff branches, and the three-month installation exception.
- Eight fixed synthetic fixtures use clearly fictional identities and relative T0 dates to give every evaluated CRM and the Centah reference baseline identical starting conditions where applicable, including an intentional missing-next-action negative test.
- TS-01 through TS-07 now have approved common execution rules, exact steps, timing boundaries, no-send/no-travel controls, and expected results.
- Evaluator screening covers all candidates first. Loryn tests no more than two viable finalists in one guided session of about 20 minutes each and receives no homework or follow-up test tasks.
- The evaluator uses one test-run header and one compact result row per gate or criterion; Loryn does no evidence-recording work.
- CP-004 approved the complete P0-W03 platform-evaluation method; no platform has been scored or selected.
- P1-W01 account ownership is approved: Loryn is the account owner and primary administrator, and the technical partner is the secondary administrator for approved ad hoc support.
- Account recovery remains under Loryn's control. Credentials, recovery codes, and MFA secrets are prohibited from Codex and project artifacts.
- The P1-W01 execution contract is approved, and Loryn is authorized to perform the bounded account-creation procedure. Synthetic configuration remains separately unapproved.
- The minimum Zoho scope is approved for contract design: standard customer/prospect/job/task records, CP-003 minimum fields, approved stages and source rules, manual next actions, five practical views, eight synthetic fixtures, and manual communications.
- Real data, external connections, automatic messages, custom code, purchases, paid upgrades, detailed quote attachments, HubSpot configuration, and final scoring remain outside P1-W01.
- A Zoho Free limitation must be recorded rather than bypassed through unapproved scope expansion or purchase.
- The approved fixture procedure uses one repository sheet, preloads seven records, creates `SYN-PROSPECT-A` during TS-01, restores T0-relative states before each run, and assigns all setup/reset work to the evaluator.
- Fixture cleanup removes only the test-created prospect and duplicate attempt and restores changed synthetic fixtures; bulk deletion of unrelated records is prohibited.
- Zoho screening proceeds through official-evidence preflight, configuration viability, synthetic scenarios, evaluator mobile timing, and result summary, stopping after a confirmed mandatory failure with no acceptable production-tier or in-scope path.
- Paid-tier possibilities require exact feature and cost evidence for `Conditional Pass`; missing evidence stays `Unverified`, and no tier may be purchased or activated in P1-W01.
- Loryn does not test during P1-W01; her finalist sessions remain deferred until all candidates complete evaluator screening.
- Raw trial captures must remain in ignored local `.trial-evidence/`; only reviewed sanitized summaries, official links, screenshots, or exports may be committed under `evidence/P1-W01/zoho/`.
- Credentials, MFA/recovery material, cookies, tokens, account identifiers, billing details, private notifications, and unrelated personal information are prohibited from evidence artifacts.
- Zoho Free is the only prototype tier. Billing, paid trials, upgrades, and purchases are prohibited in P1-W01.
- A missing Free feature receives `Conditional Pass` only with exact official evidence for the lowest supporting tier, current cost, user limit, and restrictions; temporary promotional features do not count as Free.
- Account creation requires the exact instruction `Authorize Loryn to create the Zoho Free trial account` after contract approval.
- Configuration and testing require the later exact instruction `Begin P1-W01 synthetic configuration`; account creation alone does not authorize them.
- Loryn creates the account herself with private credentials, MFA, and recovery, a neutral synthetic organization label, no employer/Costco/Centah/customer information, and no billing or paid upgrade.
- P1-W01 acceptance requires current official tier, administrator, MFA, export, limit, and cost evidence; verified administrator roles after separate account authorization; the approved minimum configuration or documented limitations; resettable synthetic fixtures; evaluator screening; evidence-backed results; a privacy and secret review; and a clear viable, eliminated, or incomplete outcome.
- Any score remains incomplete while required evidence is `Unverified`, and Loryn performs no P1-W01 testing, setup, reset, evidence capture, or homework.
- CP-005 was defined to approve only a completed Zoho evaluator result and configuration inventory, but P1-W01 did not reach it.
- The complete P1-W01 execution contract is approved. Contract approval does not authorize account creation or synthetic configuration.
- The user subsequently gave the exact account-creation authorization. Loryn may create the Zoho Free account, enable private MFA and recovery, invite and verify the technical partner as secondary administrator, and then stop.
- Account-setup reporting must exclude credentials, MFA or recovery details, private email addresses, and account identifiers.
- Zoho initially placed the new account in a 15-day Enterprise promotional trial; it was moved to Free Edition before CRM configuration or test-data entry.
- Loryn-controlled MFA is enabled.
- The approved trial organization name is `Hazel Kaine`, superseding only the earlier planned neutral label. No additional employer, Costco, Centah, or customer information is authorized.
- Zoho vendor sample data was loaded during account creation. It is synthetic but is not part of the approved CP-004 fixtures; leave it untouched until configuration is authorized, then remove it through a verified method or isolate it before evaluator testing.
- The technical partner accepted the invitation and is confirmed as the second administrator. The bounded account-creation procedure is complete.
- The user gave the exact instruction `Begin P1-W01 synthetic configuration`. Verified vendor-sample cleanup, the approved minimum configuration, fixture handling, evaluator testing, and Zoho result preparation are authorized within P1-W01.
- External connections, real data, billing, paid trials, purchases, customer communications, production use, CP-005 sign-off, and platform selection remain unapproved.
- Zoho's vendor sample data was removed through the dedicated sample-removal control and no `(Sample)` records remain in the checked CRM modules.
- Direct tenant evidence confirms that Free disables custom modules and all new Deal field types. Free cannot represent the approved CP-003 fixture baseline.
- Standard's 10 custom fields per module is also below the approved Deal/job requirement. Professional's 155 fields per module is the lowest documented capacity path, at a current official two-admin cost of $46/month annually billed or $70 month-to-month before tax.
- No partial lifecycle or incomplete fixtures were saved. P1-W01 evidence is under `../evidence/P1-W01/zoho/`, the weighted total remains incomplete, and CP-005 was not reached.
- **Accepted (D-088 option 1):** Keep Zoho as a documentation-only Professional-tier possibility, do not upgrade or purchase it, close P1-W01 incomplete without CP-005, and proceed only to definition of the next CRM comparison work unit.
- **Accepted (D-089):** Approve the P1-W02 outcome and authorize detailed contract drafting plus current official-evidence research only.
- Official HubSpot evidence confirms that Free permits only 10 custom properties in total and cannot represent the CP-003 baseline or common fixture set.
- A Starter-level path remains a paid-tier `Conditional Pass` possibility with 1,000 custom properties per object and a conservative two-Core-Seat planning cost of $40/month before tax.
- Direct tenant evidence confirms that no clean no-billing Starter-equivalent evaluation appeared; the public 14-day offer is Marketing Hub Professional and cannot be used as Starter evidence.
- M-01 remains a decision-critical risk because the multi-source custom report builder is Professional-only; Starter must directly prove a practical single action center or equivalent.
- **Accepted (D-090):** Approve the complete P1-W02 execution contract, including its candidate/tier boundary, administrator model, minimum configuration, stopping rules, separate action gates, evidence handling, acceptance checks, and CP-006 effect.
- **Accepted (D-091):** Authorize Loryn to create the `Hazel Kaine` HubSpot Free account shell, enable private MFA and recovery, invite the technical partner as secondary Super Admin, inspect only permitted edition and offer details, and then stop.
- The technical partner created the account as Loryn's proxy and may retain Super Admin control during evaluator setup and testing. Direct tenant reporting confirms HubSpot Free and the `Hazel Kaine` organization name.
- **Accepted (D-092):** Make MFA optional only during the synthetic HubSpot Free evaluation. Record the deferral as a security limitation and require MFA before any paid or promotional tier, external connection, real-data use, production use, or later security approval.
- **Accepted (D-093):** Allow the technical partner to own and control evaluator-only prototype tenants as the sole prototype administrator, defer Loryn's account access until a candidate becomes one of no more than two viable finalists, and require a separate gate before her finalist session.
- The HubSpot Free `Hazel Kaine` account shell is complete with the technical partner as evaluator administrator and MFA deferred under D-092.
- Direct tenant Account & Billing confirms `Free Tools`, with no active trial or paid entitlement displayed.
- The available `Starter Customer Platform` path is a purchase offer, not a trial: one Core Seat at a limited `$7/mo` promotion, annual checkout selected by default, `$84` due before tax, and company-address plus payment details required.
- A monthly-commit option exists, but its exact immediate total, full term, renewal price, and tax remain unverified. No no-billing Starter-equivalent evaluation appeared.
- The checkout was abandoned without data entry, purchase, activation, or configuration, and the account was returned to the Free plan overview.
- **Accepted (D-094):** Close P1-W02 incomplete without CP-006, retain HubSpot Starter as documentation-only, and continue to official-evidence screening of the next CRM candidate.
- Official Pipedrive evidence identifies Lite as the lowest plausible next-candidate tier: a 14-day no-credit-card trial, 30 custom fields per company, `$14` per seat per month billed annually, mobile daily-work features, filters, import/export, duplicate merging, and API access.
- Pipedrive Lite synthetic execution under D-099 produced a proposed eliminated result. The model fits at 25 of 30 custom fields, but source-specific handoff enforcement and Centah duplicate control failed directly; M-01 remains unverified.
- D-094 does not authorize account creation, trial activation, configuration, fixture entry, testing, integration, real data, communications, billing, purchases, production use, finalist testing, checkpoint sign-off, or platform selection.
- **Accepted (D-095):** Approve the P1-W03 Pipedrive evidence-first outcome and authorize detailed execution-contract drafting plus additional current official research only.
- The CP-003 documentation map initially used 22 custom fields. Direct D-099 configuration corrected it to 25: 9 Person and 16 shared Lead/Deal fields, leaving five fields under Lite's limit. Activities use standard fields.
- Official evidence says deals have no native duplicate identifier. The searchable Centah field and a practical manual duplicate-review procedure must therefore pass M-09 directly.
- D-095 does not authorize an account, trial, configuration, fixtures, testing, integrations, billing, purchases, real data, communications, production use, Loryn participation, checkpoint sign-off, or platform selection.
- **Accepted (D-096):** Approve the complete P1-W03 execution contract, including the Lite-only tier boundary, technical-partner evaluator ownership, execution sequence, minimum configuration, stopping rules, separate action gates, acceptance checks, and CP-007 effect.
- D-096 does not authorize account creation, trial activation, configuration, fixtures, testing, integrations, billing, purchases, real data, communications, production use, Loryn participation, checkpoint sign-off, or platform selection.
- **Accepted (D-097):** Authorize the technical partner to create the bounded `Hazel Kaine` Pipedrive evaluator account and no-credit-card trial, then inspect only nonprivate edition, expiry, and feature-boundary labels before stopping.
- D-097 does not authorize configuration, fixtures, testing, integrations, billing, purchases, real data, communications, production use, Loryn participation, checkpoint sign-off, or platform selection.
- The D-097 account shell and read-only inspection are complete. Billing overview confirms a `14-day free trial` on Premium, billed monthly, with one seat in use, no billing details entered, and a `$0` trial amount.
- Premium includes LeadBooster, Smart Docs, and Projects, so the current tenant is not clean Lite evidence. Lite appeared at `$24` monthly or `$14` per seat per month billed annually but was not selected.
- The exact calendar expiration date was not displayed. Three preloaded activity indicators appeared before evaluator data entry and remain uninspected and untouched.
- During the D-097 inspection, no plan, billing, configuration, fixture, record, integration, communication, or invitation change was made.
- **Accepted (D-098):** Switch only the existing no-billing Pipedrive trial from Premium to Lite, remove carried-over trial add-ons, verify the resulting plan and remaining-trial labels, and stop before configuration.
- D-098 is complete. Billing overview now confirms Lite, one seat, `$24` monthly pricing, `$0` during the trial, no active add-ons, no billing details, and the preserved `14-day free trial` label.
- The change flow initially carried LeadBooster, Projects, and Smart Docs into a `$110` post-trial estimate. All were disabled before confirmation, reducing the summary to `$24`.
- The Activities count changed from three to four during the vendor plan transition. No record was opened or inspected, and all preloaded content remains untouched.
- D-098 does not authorize record inspection, configuration, fixtures, testing, integrations, billing, purchases, real data, communications, production use, Loryn participation, checkpoint sign-off, or platform selection.
- **Accepted (D-099):** Begin P1-W03 synthetic configuration, including verified vendor-sample cleanup, the approved minimum Lite configuration, synthetic fixture handling, evaluator testing, and result preparation.
- D-099 execution is complete enough to prepare the evaluator result. Verified vendor sample data was removed; the tenant uses 25 of 30 custom fields, the `Window Sales Jobs` pipeline, four added workflow activity types, six approved lost reasons, seven baseline People and Deals, six baseline activities, and two private exception filters.
- Direct TS-03 testing accepted a duplicate Deal with the existing synthetic Centah identifier without blocking or visibly routing it for review. Direct TS-06 testing showed that Lite cannot conditionally require or hide source-specific handoff fields or prevent premature completion. CP-007 therefore approves `Fail` for M-02 and M-09 and eliminates Lite.
- Entity exports were generated server-side, but Chrome blocked the vendor-hosted download with `ERR_BLOCKED_BY_CLIENT`; export contents and relationship reconstruction remain unverified.
- The TS-01 Lead and Person and the duplicate Deal and Person were deleted; the active People list returned to seven baseline synthetic records. The baseline scenario state requires reset before any rerun or tenant closeout.
- D-099 does not authorize integrations, billing, purchases, real data, communications, production use, Loryn participation, checkpoint sign-off, or platform selection.
- **Signed off (CP-007):** Approve the P1-W03 evaluator result, configuration inventory, Lite tier/cost record, and evidence-backed `Eliminated` status. M-02 and M-09 fail directly.
- CP-007 does not select another CRM, authorize another account or work unit, permit Loryn finalist testing, or authorize billing, production use, integrations, real data, or customer communications.
- Preliminary current official evidence identifies Bigin by Zoho CRM Premier as the strongest next candidate. Premier lists 25 custom fields per module, five Team Pipelines, Stage Transition Rules, unique fields, duplicate cleanup, advanced date automation, mobile apps, import/export, paid-edition backups, and developer APIs.
- Official US pricing lists Premier at `$15` per user monthly or `$12` per user per month billed annually. The two-administrator baseline is `$30` monthly or `$288` annually before applicable tax or add-ons.
- The 15-day Bigin trial requires no credit card, does not charge automatically, and falls back to Free. No account or trial is authorized.
- Express is not the proposed tier because its 10 custom fields per module are below the conservative 15-field Pipeline map. Premier's 25-field limit and Stage Transition Rules make it the lowest plausible tier.
- Freshsales Pro remains the documentation-only fallback. Its field dependencies and unique fields are promising, but its current `$39` per-user annual-billing rate is materially higher and its scope is less proportionate to the one-person operation.
- **Accepted (D-100):** Approve the P1-W04 Bigin Premier evidence-first outcome and authorize detailed execution-contract drafting, the CP-003 field-capacity map, and additional current official research only.
- The conservative documentation map uses 10 Contact custom fields, 15 Pipeline custom fields, and at most 2 Task custom fields. Each remains below Premier's separate 25-field-per-module limit without add-ons.
- D-100 does not approve the proposed execution contract or authorize an account, trial, tenant inspection, configuration, fixture entry, testing, billing, purchase, external connection, real data, communication, production use, Loryn participation, checkpoint, or platform selection.
- **Accepted (D-101):** Approve the complete P1-W04 Premier-only execution contract, including the tier boundary, prototype ownership, sequence, minimum configuration, stopping rules, separate action gates, acceptance checks, and CP-008 effect.
- D-101 approves the contract only. It does not authorize an account, trial, tenant inspection, edition change, configuration, fixture entry, testing, billing, purchase, external connection, real data, communication, production use, Loryn participation, checkpoint, or platform selection.
- **Accepted (D-102):** Authorize the technical partner to create the bounded `Hazel Kaine` Bigin evaluator account and no-credit-card trial, inspect only nonprivate plan, trial-expiry, feature-boundary, sample-data, and administrator labels, and then stop.
- D-102 does not authorize an edition change, configuration, fixture entry, testing, billing details, purchase, add-on, external connection, real data, communication, production use, Loryn participation, checkpoint, or platform selection.
- D-102 direct inspection is complete: the shell reports Premier with 15 trial days remaining, one active Super Admin, vendor sample content present, and no billing prompt. No sample record was opened and no tenant setting was changed.
- Premier-equivalent evidence was isolated without an edition change; D-103 subsequently opened the signed synthetic configuration and evaluator gate.
- **Accepted (D-103):** Begin the approved P1-W04 synthetic configuration, including verified vendor-sample cleanup, the bounded minimum configuration, CP-004 synthetic fixtures, evaluator scenarios, mobile timing, export evidence, and narrow cleanup under the signed stopping rules.
- Verified vendor sample records were moved to Bigin's recycle bin; active Pipeline, Contact, Company, Product, and Activity views then showed no records. The recycle bin was not emptied.
- The saved `Window Sales Work` Team Pipeline uses 10 Contact custom fields, 14 Pipeline custom fields plus standard Lead Source, nine open stages, `Finished`, and Bigin's native `Closed Lost` label.
- The system-retained `Window Sales Work Standard` sub-pipeline serves as the Independent route, while `Costco / Centah` provides the second route. Direct Stage Transition Rule prompts required Centah, DocuSign, and coordinator dates for Costco handoff and only coordinator date for Independent handoff.
- Seven synthetic Contacts, seven linked Opportunities, three Tasks, and one Event were saved. A manual duplicate using `SYN-CENTAH-1001` was blocked, and synthetic phone-number and last-name searches both returned the intended Contact.
- Direct TS-02 inspection confirmed that source record lists remain on separate tabs, dashboards expose aggregate components rather than actionable record lists, and Pipeline views cannot filter for an active record with no linked next Task. M-01 therefore fails, and M-04/M-07 also cannot uphold the approved next-action invariant.
- The signed stopping rule ended mobile timing, import-duplicate testing, export reconstruction, administrator removal, and later scenario work. The proposed `Eliminated` result remains unapproved pending CP-008 review.
- No external connection, billing detail, paid commitment, real data, customer communication, production action, Loryn participation, checkpoint sign-off, or platform selection occurred.

## Active work-unit contract

**Status:** D-103 evaluator evidence prepared; proposed `Eliminated` result unapproved pending CP-008 review.

**Approved outcome:** Evaluate Bigin Premier as the next independent-work CRM candidate through an evidence-first, evaluator-only process. Begin with a complete CP-003 field-capacity map and execution contract, and use the no-credit-card trial only after separate contract and account-creation approvals.

**Inputs:**

- The signed CP-003 lifecycle, next-action, and minimum-field specification.
- The signed CP-004 scorecard, mandatory gates, fixtures, scenarios, burden limit, and evidence format.
- The closed incomplete P1-W01 Zoho and P1-W02 HubSpot results.
- The signed P1-W03 Pipedrive Lite elimination at CP-007.
- The August 1 Bigin official-evidence preflight in `../evidence/P1-W04/bigin/official-evidence-preflight.md`.
- The August 1 conservative field map in `../evidence/P1-W04/bigin/field-capacity-preflight.md`.

**Acceptance checks:**

- The P1-W04 outcome is explicitly approved as D-100.
- Current official evidence identifies Premier as the lowest plausible Bigin tier and names every decision-critical uncertainty.
- Direct configuration fits within Premier at 10 Contact custom fields, 14 Pipeline custom fields plus standard Lead Source, and no Task custom fields.
- The approved contract separates account creation, trial/tier inspection, any edition change, configuration, fixture entry, testing, paid action, external connection, finalist work, checkpoint sign-off, and platform selection into explicit gates.
- Preserve the CP-004 common gates, fixtures, scenarios, evidence format, and Loryn burden limit.
- Continue to prohibit real data, external connections, communications, billing, purchases, production use, and platform selection.

**Approved checkpoint effect:** A future CP-008 would approve only a completed Bigin evaluator result, configuration inventory, exact tier/cost record, and evidence-backed comparison status. It would not select Bigin or authorize payment, production use, integrations, real data, customer communication, or a Loryn finalist session.

**Out of scope:** Edition changes, billing, purchases, external connections, real data, customer communications, production use, Loryn participation, checkpoint sign-off, and platform selection. D-103 now permits only the signed synthetic configuration, fixture, evaluator-test, mobile-timing, export, and narrow-cleanup actions.

## Open items

- Review the proposed Bigin evaluator result and linked configuration inventory. CP-008 requires explicit sign-off; do not infer approval from D-103 or this saved evidence.
- If CP-008 approves the proposed elimination, separately define and authorize the next candidate or work unit. No next CRM account or tenant action is currently authorized.
- Vendor sample records and one blank malformed synthetic Contact remain recoverable in Bigin's recycle bin; seven baseline synthetic Contacts and Opportunities plus activities remain as evaluator evidence.
- Mobile timing, import duplicate behavior, export reconstruction, administrator removal, exact two-administrator checkout, API limits, and retention remain unverified because the mandatory stopping rule ended the run.
- If P1-W03 is reopened, reset the seven baseline fixtures and remove any orphaned TS-01 activity before another run or tenant closeout.
- D-011: production CRM tenant, sign-in method, access removal, and security/retention controls.
- D-012: Centah API, webhook, export, sandbox, limits, and support model.
- D-013: retention and deletion periods.
- D-014: exact Costco program fields and restrictions.
- D-016: final platform trial result.
- D-017: whether a Centah adapter is justified after the manual bridge.
- Complete the current communications-compliance review before purchasing/importing prospect lists or enabling automated outreach.
- Deferred: whether detailed quote files enter the CRM and whether the personal Google account may connect directly.

## Completed checkpoints

CP-001 approved `../deliverables/P0-W01-current-workflow-and-permission-boundary.md`. Decisions D-020 through D-023 record the approved production boundary, transfer filter and Centah identifier model, post-install reminder rule, and initial support scope.

CP-002 approved `../deliverables/P0-CR01-independent-leads-and-prospecting-scope.md`. Decisions D-024 through D-029 record the separate prospecting lifecycle, Costco-only Centah boundary, prospect cadence and outcomes, source-specific post-sale handoff, installation exception, past-customer outreach, and communication controls. Word is intentionally deferred and marked stale until a release or sharing milestone.

CP-003 approved `../deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`. Decisions D-033 through D-048 record prospect conversion, the active-job stages, contact and quote timing, follow-up limits, source-specific handoff, installation and post-install rules, and the minimum customer/job/task fields. D-035 and D-040 were superseded during the signed design sequence. At CP-003, the authoritative Markdown master was Version 1.24; Word remains intentionally stale until a release or sharing milestone.

CP-004 approved `../deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`. Decisions D-049 through D-061 record the mandatory gates, D-062 through D-069 record the complete 100-point scorecard and scoring rule, D-070 through D-072 record the scenarios, fixtures, and scripts, D-073 records the staged test-burden rule, and D-074 records the evaluator-only evidence format. At CP-004, the authoritative Markdown master was Version 1.39; Word remains intentionally stale.

P1-W01 is closed incomplete by D-088 option 1; Zoho Professional remains documentation-only and CP-005 was not reached. P1-W02 is closed incomplete by D-094 option 3; HubSpot Starter remains documentation-only and CP-006 was not reached. D-093 continues to allow technical-partner-only prototype administration while deferring Loryn until a viable finalist. D-095 and D-096 approved the P1-W03 outcome and contract. D-097 completed the account-shell inspection, D-098 completed the no-billing transition to Lite with no active add-ons, D-099 produced the Pipedrive evaluator result, and CP-007 approved that result and eliminated Lite. D-100 approved the P1-W04 Bigin Premier outcome, D-101 approved the complete Premier-only execution contract, D-102 completed the bounded account shell, and D-103 authorized the synthetic run. Direct M-01 evidence now supports a proposed Bigin `Eliminated` result, but CP-008 has not been signed. The authoritative Markdown master is Version 1.78; Word remains intentionally stale.

CP-007 approved `../evidence/P1-W03/pipedrive/evaluator-result.md` and the linked configuration, tier, and cost evidence. Pipedrive Lite fails M-02 source-specific workflow and M-09 safe Centah/Costco bridge because the evaluated tier cannot enforce the required source-specific handoff and accepted a duplicate synthetic Centah identifier without a block or visible review route. CP-007 does not select another CRM or authorize another candidate.

## Chat and artifact protocol

- Keep the current guided checkpoint in one pinned project chat.
- Use separate project chats for materially different outcomes and reconcile their results into the guided checkpoint before sign-off.
- Treat Markdown and project-control files as authoritative; chat transcripts and Word copies are not restart sources.
- Generate and fully verify Word only at a final release or explicit sharing milestone.
- Use `COLLABORATOR_PACKET.md` to collect asynchronous mobile input in a shared ChatGPT Project. Its handoffs remain unapproved until reconciled and explicitly signed off through this repository workflow.

## Repository backup

- **Remote:** `https://github.com/jonah-dawg/loryn-work-optimization.git`
- **Branch:** `main`
- **Local checkout:** `C:\Users\jonah\Documents\GitHub\loryn-work-optimization`
- **Tracked scope:** authoritative Markdown deliverables and project-control files, plus repository guidance.
- **Excluded from routine checkpoints:** the stale Word distribution copy, rendering/QA intermediates, ChatGPT-synced source mirrors, credentials, real customer data, and local temporary files.
- Until the repository folder is attached or opened as the primary Codex project, the app-managed project folder remains the interactive working copy and the repository is refreshed from it at saved checkpoints.

## Next work-unit starting point

Phase 0 is complete at CP-004. Phase 1 P1-W01 and P1-W02 are closed incomplete under D-088 and D-094. P1-W03 is closed at CP-007 with Pipedrive Lite eliminated. P1-W04 has a completed proposed evaluator result under D-103: direct M-01 evidence supports `Eliminated`, but CP-008 remains unsigned.

## Exact next action

Review `../evidence/P1-W04/bigin/evaluator-result.md` and the linked configuration inventory. If the proposed Bigin Premier elimination is accepted, explicitly sign CP-008. Do not infer that sign-off, authorize a next candidate, or select a platform from this evidence alone.

## Resume instruction

Read this file, Session S-078 in `SESSION_LOG.md`, `../deliverables/P0-W03-crm-platform-scorecard-and-mobile-test-scenarios.md`, `../deliverables/P1-W04-bigin-evidence-first-screening.md`, and the linked Bigin configuration and evaluator evidence. CP-007 is the last signed checkpoint; D-103 is the last approval. The proposed Bigin `Eliminated` result is unapproved pending CP-008 review. Never request or record credentials, codes, recovery information, private email addresses, or account identifiers. Do not continue tenant testing after the mandatory stopping result, authorize a next candidate, change edition, connect services, add billing, use real data, communicate with customers, begin finalist testing, sign CP-008, or select a platform without the applicable separate approval.
