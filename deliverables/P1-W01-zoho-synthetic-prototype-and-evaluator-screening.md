# P1-W01 - Zoho Synthetic Prototype and Evaluator Screening

**Status:** Approved for execution - account creation authorized; configuration gate closed
**Phase:** Phase 1 - Zoho prototype and HubSpot comparison
**Updated:** July 30, 2026
**Last signed-off checkpoint:** CP-004

## Proposed work-unit outcome

Create and evaluate the smallest useful synthetic Zoho CRM prototype against the CP-004 mandatory gates and scripted scenarios, then decide whether Zoho is viable enough to remain in the candidate pool for comparison. Loryn tests only later finalists after all candidates receive evaluator screening.

This outcome and execution contract are approved. Account creation and synthetic configuration remain separately gated and require their exact authorization phrases.

## Approved decisions

### Account ownership and administration

- Loryn will own the Zoho account and remain its primary administrator.
- The technical partner will be invited as secondary administrator for setup, troubleshooting, recovery support, and other approved ad hoc administration.
- Account recovery information will remain under Loryn's control.
- Passwords, recovery codes, MFA secrets, and other credentials will never be shared with Codex or stored in the repository, project artifacts, fixtures, screenshots, or logs.
- No account may be created until the complete P1-W01 contract is approved and the user separately authorizes the account-creation action.

### Minimum prototype configuration scope

Configure or attempt to configure only:

- Standard CRM records representing contacts or customers, prospects, jobs, and tasks or activities.
- The CP-003 minimum fields needed by the approved scenarios.
- Approved job stages, retained outcomes, source classification, and Costco/Centah-only identifier fields.
- A manual next action and due date on active records.
- Five practical work views: `Today`, `Overdue`, `Waiting on Others`, `Missing Next Action`, and `Installation Exceptions`.
- The eight CP-004 synthetic fixtures.
- Manual reminders and human-reviewed communications only.

Explicitly exclude:

- Real customer or prospect data.
- Email, calendar, maps-account, Centah, or other external connections.
- Automatic customer messages or outreach.
- Custom code or a separate application.
- Purchases, paid upgrades, or subscription changes.
- Detailed quote attachments.
- HubSpot configuration or final platform scoring.

If Zoho Free cannot support an item, record the limitation and evidence instead of expanding the build or purchasing an upgrade.

### Synthetic fixture entry and reset

- Maintain one repository fixture sheet containing only the eight CP-004 fictional records.
- Preload the seven existing-record fixtures. Keep `SYN-PROSPECT-A` absent at baseline because TS-01 creates it.
- Use import only if Zoho Free supports it safely; otherwise the evaluator enters fixtures manually.
- Before each run, calculate relative dates from evaluation day `T0` and restore approved stages, tasks, and the intentional missing-next-action condition.
- Verify fixture IDs and starting states with a short checklist before timing begins.
- After a run, remove the newly created prospect and duplicate attempt and restore changed synthetic fixtures.
- Assign all setup and reset time to the evaluator; it never counts against Loryn's guided-session cap.
- Do not bulk-delete or reset unrelated records.

### Evaluator screening sequence and early stopping

1. **Official-evidence preflight:** verify the current Zoho tier, two-administrator support, MFA, exports, limits, and expected production cost.
2. **Configuration viability:** test whether the approved records, fields, stages, tasks, source rules, and five work views can be configured.
3. **Synthetic scenario screening:** load or reset fixtures and run TS-01 through TS-07 without messages, integrations, or real data.
4. **Evaluator mobile timing:** measure the required one-minute actions only while Zoho remains viable.
5. **Result summary:** record mandatory results, weighted scores, limitations, confidence, and unresolved evidence.

Apply these stopping rules:

- Stop after a confirmed mandatory failure with no acceptable production tier or in-scope configuration path.
- Assign `Conditional Pass` to a paid-tier possibility only when exact feature and cost evidence exists; do not purchase or activate the tier.
- Keep missing evidence `Unverified`; never convert it into an assumed pass or failure.
- Loryn does not test Zoho during P1-W01. She participates only after every candidate receives evaluator screening and finalists are identified under CP-004.

### Evidence and screenshot storage

- Store the Markdown result summary, official documentation links, and reviewed sanitized evidence under `evidence/P1-W01/zoho/`.
- Keep raw screenshots temporarily in local `.trial-evidence/`, which must remain excluded through `.gitignore`.
- Commit a screenshot or export only after cropping or redacting account email, organization or account IDs, browser tabs, notifications, billing details, and other private information.
- Never capture or store passwords, MFA screens or codes, recovery information, cookies, tokens, or credentials.
- Allow screenshots and exports to show only the approved synthetic fixtures.
- Name evidence by candidate and gate, criterion, or scenario ID rather than personal names.
- Run privacy and secret scans before every commit.
- Do not upload or externally share trial evidence during P1-W01.

### Free-tier and paid-tier handling

- Evaluate Zoho Free as the actual prototype tier.
- Do not enter billing information, start a paid trial, activate an upgrade, or purchase anything.
- Do not count a feature exposed temporarily by a promotional trial as a Free capability.
- When Free lacks a mandatory feature, identify the lowest production tier that official evidence says supports it.
- Assign `Conditional Pass` only when the exact tier, feature, current cost, user limit, and relevant restriction are documented.
- Otherwise assign `Fail` or `Unverified` according to the available evidence.
- Keep Free-tier and paid-tier evidence separate in every result.
- P1-W01 may document upgrade options but cannot recommend or authorize a purchase.

### Trial-account procedure and action gates

1. Complete and explicitly approve the full P1-W01 contract.
2. Require the user to say `Authorize Loryn to create the Zoho Free trial account` before account creation.
3. Loryn creates the account herself using an email and recovery method she controls.
4. Use the neutral organization label `Synthetic Window Workflow Trial`; do not enter employer, Costco, Centah, or customer information.
5. Select the normal U.S. region if Zoho asks for a data region.
6. Loryn enables MFA and stores recovery information privately.
7. Enter no billing details and decline paid trials or upgrades.
8. Invite the technical partner as secondary administrator and verify both administrator roles.
9. Stop after account and administrator setup and report that the account is ready.
10. Require the user to say `Begin P1-W01 synthetic configuration` before creating fields, entering fixtures, configuring views, or running tests.

Never share credentials, codes, or recovery information with Codex.

## Approved acceptance checks

P1-W01 is complete only when:

- Current official evidence records the Zoho tier, support for two administrators, MFA, exports, applicable limits, and expected production cost.
- After separately authorized account creation, account ownership and both administrator roles are verified without recording credentials or private account details.
- The approved minimum configuration is completed, or each unsupported item is recorded as a limitation with evidence.
- All eight synthetic fixtures are loaded or created and can be restored to the approved T0-relative baseline without real data.
- TS-01 through TS-07 receive evaluator screening unless an approved early-stop condition applies.
- Every applicable mandatory gate and weighted criterion records a result or score, evidence, confidence, and uncertainty; any total remains incomplete while required evidence is `Unverified`.
- Privacy and secret review confirms that committed artifacts contain no real data, credentials, billing information, external connections, customer messages, or unapproved private information.
- The result identifies Zoho as viable for the candidate pool, eliminated, or incomplete with named blockers.
- Loryn performs no P1-W01 testing, evidence capture, fixture setup, reset, or homework.

## CP-005 effect

CP-005 will approve only the completed Zoho evaluator result and configuration inventory. It will not select a platform or authorize HubSpot account setup, Loryn finalist testing, production use, real data, external integrations, purchases, customer communications, or automation.

## Contract status

The complete P1-W01 execution contract is approved. Account creation is authorized for Loryn under the approved procedure. Synthetic configuration and testing remain unapproved.

## Account-creation authorization status

- The user gave the exact account-creation authorization on July 30, 2026.
- Loryn may complete steps 3 through 9 of the approved trial-account procedure.
- After setup, report only whether the neutral-label Free account, MFA, and both administrator roles are ready; do not report credentials, codes, recovery information, private email addresses, or account identifiers.
- Stop after account and administrator setup.
- Do not create fields, enter fixtures, configure views, connect services, or run tests until the separate configuration gate opens.

## Approval boundary

The complete work-unit contract and Loryn's bounded account-creation action are approved. Actual Zoho configuration, platform testing, external connections, real-data use, customer communications, purchases, platform scoring, and platform selection remain unapproved. Configuration and testing require the later exact instruction `Begin P1-W01 synthetic configuration`.
