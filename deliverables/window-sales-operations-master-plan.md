# Window Sales Operations

## Master Project Plan

**Version:** 1.18
**Status:** Working source of truth  
**Updated:** July 29, 2026  
**Primary team:** Window-covering sales consultant and technical partner

> **Product outcome:** Configure a company-approved, mobile-capable CRM to manage Costco/Centah opportunities, independently sourced leads, and future-client prospecting while telling the consultant whom to contact, where to go, what is missing, and what must happen next. Build only the Centah integration and workflow extensions that prove necessary - without replacing approved company systems or creating an uncontrolled customer database.

## 1. How to use this plan

This Markdown file is the durable, renderable project source of truth. Keep it in the repository and make material decisions here at each signed checkpoint. Generate or refresh the editable Word distribution copy only at a final release or explicit sharing milestone. Product requirements, architecture decisions, and sprint plans may expand the detail, but they should link back to this plan.

**Change discipline**

- Record material choices in the decision log before implementation.
- Keep unresolved questions visible; do not silently convert assumptions into facts.
- Keep ChatGPT Project content, repository artifacts, documentation, tests, and trial configurations synthetic or anonymized. Use real records only in the selected production CRM after access, security, and retention controls are configured.
- Review this plan at the end of each phase and during the weekly product review.
- Treat Centah, Costco program rules, security requirements, and OpenAI product capabilities as changeable external dependencies.

## 2. Product charter

### Problem

The consultant performs prospecting, sales, scheduling, field measurement, customer service, builder coordination, installation support, and account management across metro Atlanta. Work arrives through Centah/Costco, referrals, builders, networking, past customers, social media, purchased lists, local businesses, direct outreach, calls, texts, and email. The resulting context switching, repeated data entry, scattered notes, and geographic travel create missed follow-ups and after-hours administration.

### Product vision

A configured CRM becomes the consultant's mobile workflow hub: one reliable daily queue, a complete prospect and opportunity history, fast field capture, human-reviewed outreach, and approved data exchange for Costco leads through Centah. Existing CRM capabilities are used before custom code, while retailer and company program controls remain intact.

### Success outcomes

- Capture or import a new lead in under one minute.
- Capture a partial prospect with its source, reachable channel, next action, and follow-up date.
- Convert a qualified prospect into an opportunity without losing source or activity history.
- Identify every overdue, uncontacted, stalled, or next-action-free opportunity.
- Prepare for a visit and record its outcome from one screen.
- Reduce duplicate entry between Centah and the selected CRM.
- Reduce driving and administrative time without lowering response quality.
- Preserve an auditable trail for lead, appointment, quote, and installation events.

### Non-goals for the first release

- Replacing Centah, the employer's systems, or Costco program controls.
- Building a complete custom CRM, customer database, API, or mobile website before a configured CRM pilot demonstrates a specific gap.
- Automatic outbound email, SMS, or calls without an explicit review step.
- Purchased-list imports or automated prospecting before communications-compliance review and approval.
- Custom route optimization, full offline synchronization, accounting, inventory, commissions, customer portals, or AI-generated measurements.
- Storing unrestricted copies of all customer communications, photographs, or retailer data.

## 3. Operating model: two parallel workstreams

The operational and technical workstreams run in parallel and meet in a 30-minute weekly product review. The operational stream defines the real workflow and policies; the technical stream implements only validated rules.

| Stage | Operational workstream | Technical workstream | Exit signal |
|---|---|---|---|
| Foundation | Map lead-to-install variants; confirm data authority; define priorities and territory rules | Evaluate Zoho, HubSpot, and Centah fit; establish synthetic test data, scoring criteria, and the integration boundary | Approved workflow map, data-governance checklist, and platform shortlist |
| Configured MVP | Define canonical stages, required fields, next-action rules, and message templates | Configure CRM objects, fields, pipeline, tasks, views, permissions, and mobile layout | A complete synthetic lead can move through the core loop without custom application code |
| Field pilot | Standardize visit preparation, post-visit capture, zone days, and follow-up cadence | Configure appointments, mobile capture, navigation links, templates, and pilot reporting | Consultant can run representative days from the selected CRM |
| Integration pilot | Confirm Centah source-of-truth boundaries, identifiers, API/webhook/CSV options, and write-back permissions | Add the smallest approved import/sync adapter, reconciliation, monitoring, and controlled write-back | Test records reconcile without duplication or data loss |
| Scale and intelligence | Tune policies and define useful recommendations | Add approved CRM automation, calendar/communication connections, AI assistance, or targeted extensions | Measured time savings and stable operations justify expansion |

## 4. Operational workstream

### O1. Workflow discovery

Map at least one real example of each workflow using anonymized data:

- Costco-originated lead.
- Independently sourced lead with a current project.
- Future-client prospect from referral, builder, networking, past customer, social media, purchased list, local business, or direct outreach.
- Builder/community lead.
- Existing customer or referral.
- Warranty or installation issue.
- New construction and occupied-home consultation.

For each step capture trigger, required information, current system, expected timing, common failure, completion signal, and next action.

**Approved baselines:** The current Costco/Centah workflow, systems, gaps, and permission boundary are recorded in `P0-W01-current-workflow-and-permission-boundary.md` and were signed off at CP-001. CP-002 approved `P0-CR01-independent-leads-and-prospecting-scope.md`, extending the product to independently sourced leads, future-client prospecting, and past-customer outreach. Key problems are duplicate appointment entry, memory-driven quote and prospect follow-up, an email-only internal handoff, and no post-handoff status view.

The target design uses two connected lifecycles so future prospects do not distort the active sales pipeline.

**Approved prospecting lifecycle:**

1. Active prospect with source, reachable channel, next action, and due date.
2. Long-term nurture after three unanswered attempts, with one final 90-day reminder.
3. Converted when a real project is confirmed and the initial meeting is scheduled.
4. Archived as no response, not interested, invalid information, or duplicate.
5. Do not contact when the person explicitly opts out.

**Accepted prospect-to-opportunity conversion rule:** A prospect becomes an active opportunity only when a real window-covering project is confirmed and the initial consultation is scheduled. At conversion, close the prospecting sequence as `Converted`, retain the reusable customer record and all prospecting history, and create one opportunity for that specific project at `Consultation Scheduled`. The first required next action is the morning-of appointment confirmation. A direct inquiry about an immediate project may enter the active-opportunity lifecycle at `Consultation Scheduled` without first passing through prospecting.

**Approved active-opportunity lifecycle:**

1. `New Customer Request`.
2. `Trying to Contact`.
3. `Appointment Scheduled`.
4. `Appointment Completed`.
5. `Preparing Quote`.
6. `Quote Sent - Awaiting Decision`.
7. `Customer Accepted - Handoff Due`.
8. `Handoff Complete - Installation Pending`.
9. `Installed - Customer Follow-Up Due`.
10. `Finished`.

An opportunity may exit as `Lost / Canceled` from any applicable stage. An installation that remains unconfirmed at the approved three-month boundary receives a visible overdue-installation exception instead of advancing automatically or remaining in routine deferral indefinitely. The sequence deliberately avoids asserting that an order was placed or an installation was scheduled when the consultant has not received confirmation of those events.

**Invariant:** Every active opportunity has a current stage, last-contact timestamp, next action, and next-action date. Exceptions require a recorded reason.

**Prospecting invariant:** Every active prospect has a source, at least one reachable channel or location, a next action, and a follow-up date. Conversion preserves the source and activity history.

**Approved next-action rule for `New Customer Request`:** The CRM creates a reminder for a human to make the first contact attempt; it does not contact the customer automatically. Calling hours are Monday through Friday, 9:00 a.m. to 6:00 p.m., and Saturday, 9:00 a.m. to 2:00 p.m. A request received during calling hours is due for contact by that day's closing time. A request received outside calling hours is due at 9:00 a.m. on the next working day. Sunday requests are therefore due Monday at 9:00 a.m. unless that day is later configured as unavailable.

**Approved next-action rule for `Trying to Contact`:** If the first contact attempt receives no answer, the second attempt is due on the next working day. If the second attempt receives no answer, the third and final attempt is due two working days later. If the third attempt also receives no answer, close the opportunity as `Lost / Canceled - No Response`, retain the record and attempt notes, and stop creating active-job reminders. This rule applies to active customer requests, not the separately approved long-term prospecting lifecycle. For a Costco/Centah lead, the related Centah record also follows the approved current process of being canceled and retained as inactive.

**Approved next-action rule for `Appointment Scheduled`:** Create a morning-of reminder to send the customer a manual confirmation text at approximately 7:45 a.m. This is a limited exception to calling hours and does not permit an automated message. Use another requested channel when needed, but do not place a confirmation phone call before the 9:00 a.m. calling-hours start.

**Approved next-action rule for `Appointment Completed` and `Preparing Quote`:** After an appointment is completed and a quote is needed, the primary goal is to finish and manually send the quote by the end of that same working day. The opportunity moves to `Preparing Quote` with that deadline. If the quote is not sent by closing time, it remains visibly overdue until the consultant records a short delay reason and sets the fallback deadline to the end of the next working day. If that fallback is also missed, the task remains overdue and requires another deliberate date and reason; it is never silently cleared or rescheduled.

**Approved next-action rule for `Quote Sent - Awaiting Decision`:** Immediately after emailing the quote, send a manual message through the customer's preferred and permitted channel telling them the quote was sent and asking them to check their email. Then create the next manual decision-follow-up task for three working days later. If that follow-up does not produce a response, follow up manually once a week for three weeks during normal calling hours. If the customer still does not respond after the third weekly follow-up, close the opportunity as `Lost / Canceled - No Decision`, retain the quote and communication history, and stop active reminders. If the customer asks for more time, replace the weekly reminder with the specific date they request. If the customer responds before a task is due, cancel that reminder and record the response and resulting next action or outcome. No message is sent automatically.

### O2. Communication policy

- **Interrupt immediately:** same-day access changes, installation problems, builder emergencies, safety issues.
- **Batch frequently:** new-lead responses, quote questions, appointment coordination, routine builder requests.
- **Batch daily or less:** vendor announcements, marketing, and nonurgent administration.
- Define expected response windows by source and severity.
- Approve reusable templates for first contact, confirmations, on-my-way messages, quote delivery, follow-ups, delays, completion, and referrals.
- Record preferred channel, acquisition source/date, contact-permission status, overall do-not-contact status, and channel-specific opt-outs.
- Keep prospecting human-reviewed. Purchased-list imports and automated outreach require a separate communications-compliance review before use.

### O3. Territory and scheduling policy

Create practical metro Atlanta zones such as North Fulton, Cobb, Gwinnett, Intown/Buckhead, Cherokee, South/East Metro, and outer-market trips. For each zone define preferred days, maximum appointments, travel buffers, service radius, and exception rules. The MVP displays and recommends zones; it does not automatically reschedule customers.

### O4. Field operating standard

- Before the visit: confirm address, contact, access, products of interest, source/program, and prior communications.
- During the visit: capture product selections, measurements, constraints, photos only when approved, and customer decisions.
- Before leaving: record visit outcome, update stage, and create the next action.
- End of day: clear quick-capture drafts, reconcile exceptions, and prepare tomorrow's route.

### O5. Operational scorecard

Track only metrics that change behavior:

- Median lead response time.
- Active opportunities missing a next action.
- Consultation-to-quote turnaround.
- Follow-ups completed on time.
- Appointment no-show/cancellation rate.
- Consultations per field day and driving time per consultation.
- Conversion and cycle time by lead source.
- Centah import/sync exceptions and unreconciled records.

## 5. CRM-first product and MVP

### Product definition

The selected CRM is the system of engagement for the consultant's daily workflow and the sole workflow system for independently sourced prospects and opportunities. Centah is used only for Costco-originated leads and remains the initial system of record for their identity and any retailer/program fields governed there. The CRM becomes authoritative for independent prospecting and for explicitly approved local workflow fields such as personal tasks, next actions, and local notes.

The first release is a configured product, not a newly built application. A custom API, database, PWA, or website is authorized only when a measured requirement cannot be met safely and economically through CRM configuration or a thin integration adapter.

### Platform evaluation gate

Prototype the workflow in **Zoho CRM Free** first and evaluate **HubSpot Free** alongside it. Use synthetic records and the same scripted scenarios in both products. Do not select a platform from a feature checklist alone; observe the consultant completing real mobile tasks.

Score each candidate on:

- Mobile speed and usability while parked.
- Pipeline, field, view, task, and reminder configuration.
- Ability to enforce or visibly flag a missing next action.
- Calendar, email, maps, and approved attachment handling.
- API access, import/export, deduplication, and webhook options.
- Permissions, audit history, retention, deletion, and company administration.
- Reporting, automation limits, support model, upgrade cost, and exit portability.
- Fit with the confirmed Centah integration mechanism.

**Selection rule:** choose the lowest-total-cost platform that passes all mandatory governance, mobile workflow, data portability, and Centah integration requirements. Treat free tiers as prototypes, not as a promise that production will remain free.

### Configured first release

Use standard CRM objects whenever practical:

- **Contact:** reusable prospect/customer identity, approved communication information, preferences, and opt-outs.
- **Deal or Opportunity:** one window-covering order or project. A returning customer may have multiple opportunities.
- **Company or Account:** builder, community, Costco source, or referral partner.
- **Activities:** calls, email records, approved text notes, meetings, site visits, and stage events.
- **Tasks:** next action, due date, priority, and completion state.
- **Attachments:** only approved measurement sheets, quotes, selections, or photographs.

Configure custom fields only where the standard model is insufficient:

- Centah lead number and source-system timestamp, required and unique only on Costco/Centah opportunities. Each new Costco order receives a new Centah lead number.
- Lead/prospect source, source detail, Costco program reference, builder, and community.
- Prospect state, reachable channel/location, next action/date, acquisition date, permission status, preferred channel, do-not-contact status, and channel-specific opt-outs.
- Service address, territory/zone, property type, and access notes.
- Product interests, consultation outcome, quote status, and installation status.
- Next-action type, next-action date, last-contact date, and stall reason.
- Import/sync state, mapping version, last successful sync, and reconciliation status.

Initial import and retention rules:

- Transfer only active and sold Centah leads; exclude canceled/inactive leads.
- Use the Centah lead number as the opportunity-level external ID for traceability and deduplication.
- Keep independent prospects and opportunities only in the selected CRM; do not enter or synchronize them into Centah.
- Keep detailed quote files outside the initial CRM scope until their storage and transfer controls are approved; Centah currently stores only the quoted dollar amount.
- After acceptance, Costco/Centah opportunities require DocuSign and the quote emailed to the internal order coordinator in parallel; independent opportunities skip DocuSign and require the quote emailed to the internal order coordinator.
- Create a follow-up checkpoint six weeks after DocuSign for Costco/Centah sales or six weeks after the quote is emailed to the internal order coordinator for independent sales. If installation is incomplete, add a note and reschedule by two to three weeks.
- If installation is still unconfirmed three months after the sold quote was emailed to the internal order coordinator, flag an exception, create a same-day task to contact the coordinator, require the result, and prompt customer contact if the coordinator cannot confirm. Never mark installation complete without human verification.
- After the post-install follow-up, eligible past customers receive manually reviewed additional-work/referral reminders at 6, 12, 18, and 24 months, then stop. Opt-out or unresolved problems suppress promotional outreach.
- Do not include ongoing support or future repair-case management in the initial CRM scope.

### Required mobile views

1. **Today:** appointments, overdue prospect and sales follow-ups, uncontacted leads, quotes due, missing next actions, installation exceptions, and sync exceptions.
2. **Prospecting:** active prospects, nurture reminders, source, preferred channel, latest result, and due work.
3. **Pipeline:** filterable deals by stage, source, zone, and builder/community.
4. **Opportunity:** customer, property, stage, next action, appointments, source reference, source-specific handoff checklist, and activity history.
5. **Field update:** consultation outcome, stage change, next action, note, and approved attachments.
6. **Calendar/route:** ordered appointments, zone context, travel buffer, and links to the preferred maps app.

These may be native CRM screens, configured views, forms, or dashboards. A custom screen is a later exception, not an MVP assumption.

### First configured slice

> Create an independent synthetic prospect or import a synthetic Costco/Centah lead, assign its state or stage and next action, make it visible in the daily work queue, and preserve its source and activity history using CRM-native capabilities.

**Acceptance criteria**

- An authorized CRM user can create or import a lead using synthetic or approved data.
- An independent prospect can be created without a Centah identifier and converted into an opportunity without losing history.
- A new opportunity begins in `New` unless an imported source supplies an approved mapped state.
- Active opportunities require a next action and due date, or appear in a visible exception view.
- Creation preserves source provenance and an attributable activity event.
- The item appears in the daily queue when attention is due.
- Replaying the same import does not create a duplicate.
- The consultant can complete the core loop from the CRM mobile app without a spreadsheet.
- Customer fields, credentials, and raw integration payloads are excluded from logs and project artifacts.

### MVP definition of done

- The consultant completes the create/import -> review -> contact -> next-action loop on a phone-sized screen.
- A stalled opportunity is discoverable without searching email or texts.
- Every material change is attributable and timestamped to the extent supported by the selected tier.
- The selected tier's automation, API, record, file, and history limits are documented and acceptable for the pilot.
- Export, deletion, access removal, integration disablement, and recovery procedures have been exercised.
- Data use, retention, vendor administration, and integration permissions are documented.
- Pilot telemetry measures time saved without exposing message or customer content.

## 6. Centah and Costco integration strategy

### Confirmed public capability and current uncertainty

Centah publicly describes home-services lead/workflow management, mobile field use, calendar synchronization, and a turnkey integration engine using REST APIs and webhooks. Public marketing material is not an implementation contract, and no public developer specification was located during this planning pass. Obtain the company-specific data dictionary, API/webhook documentation, sandbox, credentials, limits, and support process before designing production endpoints.

Costco is the only lead channel in this plan that flows through Centah. Do not build a direct Costco connector or store Costco member data merely because a lead originated there. Independent business remains only in the selected CRM and is excluded from Centah synchronization.

### Integration principles

- **Centah-first identity:** Preserve Centah's immutable lead/job ID and retailer/program references.
- **Approved-record filter:** Transfer only active and sold leads; exclude canceled/inactive leads.
- **Minimal replication:** Copy only fields needed for the consultant workflow.
- **Provenance everywhere:** Record source system, source timestamp, mapping version, and last successful sync.
- **Idempotent processing:** Imports and webhooks must be safely replayable.
- **Human-visible exceptions:** Conflicts and rejected records appear in a reconciliation queue.
- **Controlled write-back:** No Centah update until each field, trigger, and permission is approved.
- **Adapter boundary:** Domain logic never depends directly on Centah payload shapes.

### Integration maturity path

1. **Discovery and authorization** - obtain any required company permission, Centah technical documentation, contract terms, data classification, allowed purposes, sandbox, and sample sanitized payloads.
2. **Configured CRM bridge** - support validated CSV import or assisted entry with external IDs. This proves CRM fit, mapping, and deduplication without production credentials.
3. **Read-only incremental sync** - use the selected CRM API plus the approved Centah interface to ingest leads/statuses; checkpoint, retry, reconcile, and alert.
4. **Selective write-back** - send only approved events such as appointment outcome or status, with explicit source-of-truth rules and audit history.
5. **Operational automation** - use CRM-native workflows first; add custom integration actions only after consent, reliability, and a workable support process are proven.

### Proposed synchronization contract

| Data domain | Initial authority | Initial direction | Conflict rule |
|---|---|---|---|
| Centah lead number and retailer program | Centah | Centah -> selected CRM for active/sold leads | Centah wins; never regenerate; one number per opportunity/order |
| Customer identity/contact | Centah or approved company system | Centah -> selected CRM, minimal fields | Quarantine material conflicts; do not silently overwrite |
| Independent prospect/customer identity and preferences | Selected CRM | Local only | Selected CRM wins; do not send to Centah |
| Opportunity workflow stage | Centah for governed statuses; selected CRM for local substate | Read first; selective two-way later | Field-level authority map and explicit transition mapping |
| Next action and personal task | Selected CRM | Local only initially | Selected CRM wins |
| Appointment | Confirm during discovery | Read first; two-way later if approved | Reject overlapping or stale updates to review queue |
| Activity notes | Selected CRM, minimal approved content | Local only initially | Append; never destructively merge |
| Quote/order/install facts | Company/Centah system as confirmed | Read-only initially | Source system wins; selected CRM stores reference and summary |

### Reliability design

- Use a webhook inbox, integration queue, or import staging area before updating CRM records.
- Store payload hash, external event ID, received time, mapping version, status, and retry count.
- Apply exponential retry with a dead-letter/review state; do not retry permanent validation failures indefinitely.
- Run scheduled reconciliation against updated-since queries or approved exports.
- Monitor freshness, duplicate rate, failure rate, backlog age, and unmapped status values.
- Contract-test mappings against sanitized fixtures and version them.
- Provide a kill switch that pauses write-back independently of read sync, even when CRM-native automation is active.

### Centah discovery questions

- Is access available through REST API, webhooks, scheduled export, or another partner integration path?
- Which object IDs are immutable, and are updates versioned?
- Which events are delivered, retried, ordered, and signed?
- What authentication, IP restrictions, rate limits, and sandbox environments apply?
- Which fields may the company copy, transform, retain, or send to another processor?
- Which statuses must be written back, within what service levels?
- Does Centah already synchronize Google or Outlook calendars for this account?
- What support process applies when a lead is delayed, duplicated, rejected, or mismatched?
- Are Costco program fields subject to additional retention, access, or audit rules?

## 7. Architecture

### Recommended shape

- **User application:** the selected CRM's web and mobile applications.
- **Workflow:** configured objects, properties, pipeline stages, tasks, views, forms, permissions, templates, and reports.
- **Primary workflow data:** stored in a company-approved CRM tenant under documented retention and administration controls.
- **Centah integration:** begin with manual/CSV transfer, then add a thin adapter only when supported access and measurable value justify it.
- **Custom data storage:** none by default. If integration staging is required, retain only minimal payload metadata and approved transient data.
- **Identity:** CRM-native or company-approved federated identity, MFA, least privilege, and documented offboarding.
- **Secrets:** company-approved managed secret storage for any connector credentials.
- **Operations:** CRM audit/usage reporting plus content-free integration telemetry, reconciliation, and alerts.
- **Delivery:** versioned configuration inventory, field mappings, test scripts, runbooks, and CI/CD only for custom integration code.

### Build-versus-configure boundary

```text
Costco leads in Centah         Independent prospects/leads
          |                               |
          v                               v
Manual import or thin adapter       CRM-native capture
          |                               |
          +---------------+---------------+
                          v
                    Selected CRM
  - contacts, deals, tasks, activities
  - mobile views, pipeline, reports
  - approved workflows and templates
          |
          v
Optional targeted extension only for a proven gap
```

Do not create a parallel API, database, or web application merely to reproduce native CRM functions. Custom code is justified only when a documented requirement fails configuration, marketplace integration, and safe low-code options, and when expected time savings exceed build and support cost.

### Platform trial recommendation

- **Zoho CRM Free - first prototype:** currently positioned for up to three users and includes core lead/deal management, mobile access, standard reports, a small number of workflows, and API access. Validate exact limits in the trial tenant before relying on them.
- **HubSpot Free - comparison candidate:** currently positioned for up to two users with foundational CRM tools and email connectivity. Its full workflow builder generally requires higher paid tiers, so model likely upgrade cost before choosing it for automation-heavy use.
- **Centah-only option:** include Centah in the evaluation. If its existing mobile, task, calendar, and reporting capabilities satisfy the operating model, avoid adding another CRM.

The platform decision is not final until the same synthetic workflow script has been completed in each viable candidate and the production tenant's access, security, retention, data portability, and likely cost are acceptable.

### Repository organization

```text
window-sales-ops/
  AGENTS.md
  README.md
  docs/
    product/master-plan.md
    product/workflow.md
    product/glossary.md
    platform/evaluation-scorecard.md
    platform/configuration-inventory.md
    platform/field-dictionary.md
    platform/test-scenarios.md
    integration/centah/
    integration/field-mapping.md
    integration/reconciliation.md
    decisions/
    plans/
    security/data-classification.md
    operations/
  src/integration/       # created only if a connector is approved
  tests/integration/     # sanitized contract fixtures
  infra/                 # connector infrastructure only
```

### Key design rules

- Prefer standard CRM objects and native configuration over custom objects or code.
- Enforce stage, next-action, authorization, and transition rules through CRM controls where possible; otherwise expose exception views rather than hiding violations.
- Keep Centah and CRM source-of-truth rules explicit and versioned.
- Preserve external IDs and idempotency keys so imports and sync events can be replayed safely.
- Keep integration DTOs and mappings outside business-facing CRM configuration.
- Avoid storing full raw payloads unless approved for a short troubleshooting retention period.
- Keep customer-facing communication human-reviewed until approval and quality gates allow automation.
- Require an export and exit plan so the company can recover its data and configuration.
- Build a custom PWA or modular monolith only after a decision-log entry identifies the failed CRM requirement, expected value, and maintenance approach.

## 8. Data governance and security

CP-001 confirmed that the independent consultant may create a synthetic-only CRM trial without company permission and may transfer the approved customer fields for active and sold Centah/Costco leads into the selected CRM. CP-002 added independent prospecting and customer records that exist only in the selected CRM. Neither approval authorizes placing real data in the ChatGPT Project, repository, documentation, tests, an unsecured personal trial, or a third-party AI service. Configure the production tenant, access, retention, export, and integration controls before importing or entering real records.

### Data classes

- **Restricted customer data:** names, phone numbers, email addresses, home addresses, access notes, photos, measurements, quotes, and communication content.
- **Company/confidential data:** builder terms, program rules, pricing, commissions, performance reports, integration documentation, and credentials.
- **Operational metadata:** stages, due dates, timestamps, zones, status mappings, and system health.
- **Synthetic/test data:** invented records that cannot be linked to real customers or properties.

### Controls

- Data minimization and purpose limitation by field.
- Role-based access, least privilege, MFA, and periodic access review.
- Encryption in transit and at rest; managed secret storage.
- No sensitive payloads in logs, traces, test fixtures, screenshots, issue trackers, prompts, or analytics.
- Separate CRM sandbox/test records from production data where the selected tier permits; otherwise use a separate approved test tenant or synthetic-only configuration process.
- Audited export, deletion, correction, and account-offboarding procedures.
- Documented retention schedule for records, attachments, logs, backups, and integration payloads.
- Review the current personal-Google-account quote storage before connecting Google or copying full quote files into the CRM.
- Preserve contact source, acquisition date, permission status, preferred channel, and opt-outs; suppress promotional tasks for do-not-contact records.
- Complete a current communications-compliance review before purchasing/importing prospect lists or enabling automated calls, texts, email, social messages, or mailed campaigns.
- Incident response with company, Centah, and retailer notification paths as contractually required.
- Threat modeling before external integration and before adding AI or communications.

### AI use policy for the project

- Use synthetic or redacted data in personal ChatGPT/Codex workspaces unless the company has approved the account, plan, data use, and retention controls.
- Keep customer-facing AI output in draft/review mode.
- Do not use AI to infer measurements, contractual terms, or binding prices.
- Store prompts/templates as versioned product assets; do not store sensitive completions by default.
- Evaluate hallucination, disclosure, prompt-injection, and over-automation risks before enabling CRM-connected AI.

## 9. ChatGPT Projects and Codex organization

### ChatGPT Project

Use one project named **Window Sales Operations**. Projects keep related chats, files, and project instructions together; use separate chats for distinct outcomes so context remains focused.

**Guided-workflow chat strategy**

- Pin one chat as the active **Guided Implementation** thread. Keep discovery, clarification, checkpoint review, and sign-off for the current work unit together there.
- Continue in that chat while the same checkpoint is being refined so the immediate conversational context remains available.
- Start a new project chat when the outcome changes materially, such as platform evaluation, Centah integration research, CRM configuration, implementation, security review, or release preparation.
- Use the durable Markdown files to hand off between chats. Every new execution chat begins by reading `project-control/CURRENT_STATE.md`, the latest signed entry in `project-control/SESSION_LOG.md`, and the relevant approved artifact.
- Do not split one interactive checkpoint across multiple chats unless there is an independent research or implementation task. Do not allow two chats to edit the same durable artifact concurrently.
- Pin the current guided chat and archive outcome-specific chats when their results have been incorporated and signed off.

**Recommended chats**

- `00 - Product Decisions and Weekly Review`
- `01 - Workflow Discovery`
- `02 - CRM Evaluation and Configuration`
- `03 - Mobile Field Workflow Pilot`
- `04 - Integration Architecture and ADR Review`
- `05 - Backlog and Acceptance Criteria`
- `06 - Security and Data Governance`
- `07 - Centah Integration Discovery`
- `08 - Release and Pilot Review`

**Project sources**

- This Markdown master plan and the project-control files. Add a Word copy only when generated for a release or sharing milestone.
- Sanitized workflow notes and blank forms/templates.
- Product glossary, approved pipeline, CRM field dictionary, and status mappings.
- Platform scorecard, configuration inventory, decision index, and current release notes.
- Never upload live customer data, credentials, or unapproved Centah documentation.

### Codex working model

- Keep durable repository guidance in `AGENTS.md`; Codex reads layered instruction files from project root toward the working directory.
- Use one task/chat per coherent outcome: platform evaluation, CRM configuration, sanitized test scripts, integration mapping, connector implementation, or release review.
- Use a living plan under `docs/plans/` for multi-hour features.
- Use Git worktrees only for nonoverlapping custom integration or extension work; keep CRM configuration changes in a versioned configuration record.
- Run a privacy/authorization diff review before merging customer-data or integration work.
- Create a reusable skill only after the same workflow has repeated enough to stabilize, for example privacy review, user-story generation, or release QA.

### Project instruction summary

ChatGPT should distinguish confirmed facts, assumptions, decisions, and open questions; prioritize mobile workflow; require next actions; prefer human-reviewed assistance; use synthetic data; challenge low-value features; and produce acceptance criteria, edge cases, security implications, and a definition of done.

## 10. Phased roadmap and gates

### Phase 0 - Authority, workflow, and evaluation design (week 1)

**Operational:** workflow interviews, data authority, program rules, territory model, required outcomes, and mandatory controls.  
**Technical/configuration:** create the weighted platform scorecard, synthetic fixtures, scripted mobile scenarios, field inventory, Centah discovery checklist, and vendor/security questions.  
**Gate:** the two-person team agrees on the synthetic-only trial boundary, mandatory requirements, and scoring method. CP-001 confirmed permission to transfer approved real fields, but real imports and external integrations remain blocked until production access, security, retention, and connection controls are defined.

**Progress:** P0-W01 was signed off at CP-001. CP-002 then approved the independent-lead and prospecting scope, including prospect capture, conversion, reminders, communication preferences, source-specific post-sale rules, installation exceptions, and past-customer outreach. Within P0-W02, D-033 approved the prospect-to-opportunity conversion rule and D-034 approved the active-opportunity stage sequence. Stage-specific next-action rules and minimum CRM fields remain to be approved before CP-003.

### Phase 1 - Zoho prototype and HubSpot comparison (weeks 2-3)

**Operational:** approve the separate prospecting and active-opportunity lifecycles, next-action rules, priorities, minimum fields, and representative daily scenarios.  
**Technical/configuration:** configure Zoho first, reproduce the same scenarios in HubSpot, document tier limits and likely upgrade costs, and include a Centah-only baseline.  
**Gate:** observed mobile tests and the scorecard identify a preferred platform or show that no candidate passes mandatory requirements.

### Phase 2 - Configured CRM pilot and manual Centah bridge (weeks 4-6)

**Operational:** pilot a small approved workload; refine visit, scheduling, territory, and follow-up standards.  
**Technical/configuration:** finalize fields, pipeline, views, permissions, tasks, reports, templates, mobile layout, CSV import, deduplication, and exception handling.  
**Gate:** the consultant completes representative days with acceptable data quality and measurable time savings without custom application code.

### Phase 3 - Centah read integration (weeks 7-10, dependent on access)

**Operational:** approve field map, service levels, exception handling, and support process.  
**Technical:** implement the smallest approved adapter using scheduled export, API polling, or webhooks; add checkpoints, retries, sanitized contract tests, monitoring, and reconciliation.  
**Gate:** parallel run demonstrates completeness, timeliness, and no duplicate production records.

### Phase 4 - CRM automation, selective write-back, and communications (weeks 11-14)

**Operational:** approve each workflow, write-back, and message template; define customer consent and escalation.  
**Technical/configuration:** enable CRM-native automation first; add field-level authority rules, write-back kill switch, calendar connection, and review-before-send actions.  
**Gate:** rollback and incident drills are complete, tier cost is accepted, and both members of the project team agree to proceed.

### Phase 5 - Targeted extensions and intelligence (after stable pilot)

Add a custom screen, route recommendation, builder-specific workflow, AI summary/draft, or other extension only when measured evidence identifies a gap that CRM configuration cannot address economically. Record each build decision and its maintenance approach before implementation.

## 11. Delivery cadence and backlog order

**Weekly product review**

1. Inspect scorecard and field observations.
2. Review sync/reconciliation exceptions.
3. Resolve decision-log items needed for the next slice.
4. Confirm one operational experiment and one technical outcome.
5. Update this plan, the backlog, and relevant ADRs.

**Recommended backlog order**

1. Define mandatory platform requirements and weighted scorecard.
2. Define the prospecting lifecycle, active sales pipeline, conversion rule, source branch, next actions, and minimum fields.
3. Configure the synthetic core loop in Zoho CRM Free.
4. Reproduce and compare the core loop in HubSpot Free and Centah where possible.
5. Select the pilot platform and document tier limits, cost triggers, and exit plan.
6. Configure contacts/prospects/deals, lifecycles, next actions, daily views, permissions, and mobile layout.
7. Configure consultation scheduling, navigation, post-visit outcome, quote follow-up, installation exceptions, past-customer reminders, and approved templates.
8. Pilot manual Centah import, external IDs, deduplication, and reconciliation for Costco leads only.
9. Build a read-only Centah connector only after the interface and value are confirmed.
10. Add operational dashboards and CRM-native automation justified by pilot evidence.
11. Add selective write-back, reviewed communications, or a targeted custom extension only after approval.

## 12. Risk register

| Risk | Probability / impact | Leading indicator | Mitigation |
|---|---|---|---|
| Uncontrolled duplication of customer data | Medium / Critical | Real records appear in personal trials, files, prompts, or unapproved integrations | Approved-field allowlist; active/sold filter; synthetic project artifacts; production access, retention, and export controls |
| Centah access differs from assumed REST/webhook model | Medium / High | No developer docs, sandbox, or credentials | Adapter boundary; manual bridge; vendor discovery gate |
| Two systems disagree on status or appointment | High / High | Growing reconciliation queue | Source-of-truth matrix, versions, idempotency, human review |
| Selected CRM adds work instead of removing it | Medium / High | User keeps returning to texts/spreadsheets | Observed pilot, fast mobile configuration, import automation, remove low-value fields |
| Free tier hides a production-critical limit | High / Medium | Required workflow, history, permission, or integration is unavailable | Document tier limits and paid cost before selection; test every mandatory scenario |
| Vendor lock-in or weak data portability | Medium / High | Configuration cannot be exported or reconstructed | Versioned field/config inventory, recurring exports, exit test, minimal custom objects |
| CRM cannot enforce the next-action invariant | Medium / High | Active records lack due work despite training | Exception view, scheduled audit, workflow where supported, targeted extension only if justified |
| Mobile experience is unsafe or awkward in transit | Medium / High | Use while driving or abandoned capture | Design for parked use, large targets, voice drafts, no driving interaction |
| Sensitive data leaks through logs, prompts, fixtures, or screenshots | Medium / Critical | Raw payloads in telemetry/issues | Redaction, structured allowlist logs, secret scanning, reviews |
| Prospecting violates consent or communication rules | Medium / Critical | Purchased lists, unclear acquisition source, missing opt-out, or unreviewed automation | Record provenance and preferences; suppress do-not-contact tasks; compliance gate before list import or automated outreach |
| Prospecting overwhelms the active sales queue | Medium / Medium | Sales appointments and quotes are buried by nurture reminders | Separate prospecting lifecycle/view; priority rules; configurable cadence; archive and two-year limits |
| Integration silently stops | Medium / High | Freshness lag or missing lead counts | Health metrics, reconciliation, alerts, runbook, kill switches |
| Premature feature expansion | High / Medium | Route/AI/portal work before core loop succeeds | Phase gates and explicit non-goals |
| One-person technical dependency | Medium / High | Configuration, export, or reconciliation cannot be repeated from written steps | Runbooks, configuration inventory, and tested export and restore |

## 13. Decision log

Update this table whenever a decision changes. Supersede rather than delete prior decisions.

| ID | Status | Decision | Rationale / consequence | Review trigger |
|---|---|---|---|---|
| D-001 | Accepted | Build a workflow companion, not a generic replacement CRM | Focuses on next actions, field capture, and integration value | User needs expand beyond workflow |
| D-002 | Accepted | Run operational and technical workstreams in parallel | Development can begin with synthetic data while policies are validated | Weekly review shows dependency conflicts |
| D-003 | Accepted | Treat Centah as initial authority for Centah-originated identity and governed fields | Avoids unauthorized divergence from retailer/company processes | Company designates the selected CRM as authoritative instead |
| D-004 | Accepted | Use manual-first, then read-only, then selective write-back integration | Reduces coupling and compliance risk | Centah contract provides a different required pattern |
| D-005 | Superseded | Use a React/TypeScript PWA and ASP.NET Core modular monolith on Azure | Replaced by CRM-first decision D-015; retain as a fallback architecture | Selected CRM fails a proven high-value requirement |
| D-006 | Accepted | Require a next action for every active opportunity | Prevents forgotten work and powers Today | Approved exception model is needed |
| D-007 | Accepted | Maintain an append-only activity timeline | Preserves auditability and recovery context | Retention or legal requirements demand changes |
| D-008 | Accepted | Keep customer communications human-reviewed in early phases | Reduces brand, consent, and hallucination risk | Quality and approval gates support automation |
| D-009 | Superseded | Use synthetic/anonymized data until written authorization | Replaced by the narrower artifact and production-boundary decision D-020 after CP-001 | Production data authority or environment changes |
| D-010 | Superseded | Use Azure App Service, Azure SQL, Blob Storage, Key Vault, and Application Insights | No longer the default product stack; may apply only to an approved connector | Connector hosting is approved |
| D-011 | Open | Confirm the production CRM tenant, sign-in method, access removal, and security/retention controls | Data-transfer permission is confirmed, but the production environment still requires controlled administration | Before any production CRM data |
| D-012 | Open | Confirm Centah API, webhook, export, sandbox, rate limits, and support model | Public feature claims are insufficient for implementation | Before Phase 3 commitment |
| D-013 | Open | Define approved retention and deletion periods | Needed for database, backups, logs, and attachments | Before production data |
| D-014 | Open | Confirm exact Costco program fields and restrictions | May impose additional governance or write-back requirements | During Centah/company discovery |
| D-015 | Accepted | Configure an existing CRM before building a custom application | Reduces cost, delivery time, security surface, and support burden | All evaluated CRMs fail a documented mandatory requirement |
| D-016 | Proposed | Prototype Zoho CRM Free first and compare the same scenarios in HubSpot Free and Centah | Zoho offers a useful low-cost configuration baseline; comparison prevents premature selection | Platform scorecard and observed mobile tests are complete |
| D-017 | Proposed | Limit custom development initially to a thin Centah integration adapter | Preserves vendor capabilities while solving the unique integration gap | Manual bridge proves value and Centah access is confirmed |
| D-018 | Accepted | Use guided work units, explicit sign-off, and durable session checkpoints | Keeps chat-based execution resumable, auditable, and synchronized | Process overhead exceeds value or checkpoint recovery fails |
| D-019 | Accepted | Use a simple two-person delivery model with no formal role roster | Matches the small family-business context and avoids unnecessary process | The team expands or the company requires formal governance |
| D-020 | Accepted | Keep project, repository, test, and trial artifacts synthetic; allow approved real fields only in the controlled production CRM | CP-001 confirmed transfer permission while preserving a safe working boundary | Permission, vendor, or production controls change |
| D-021 | Accepted | Transfer only active and sold Centah leads and store the Centah lead number on each opportunity | Canceled leads are inactive and every new order receives a new lead number | Centah identity or retention behavior changes |
| D-022 | Accepted | Create a six-week post-DocuSign checkpoint; defer by two to three weeks while installation is incomplete, then perform one post-install follow-up | Replaces memory-driven follow-up with a bounded task rule | Installation timing or desired follow-up policy changes |
| D-023 | Accepted | Exclude ongoing support and future repair-case management from the initial CRM scope | Keeps the first release focused on the current sales workflow | Measured service workload justifies expansion |
| D-024 | Accepted | Support a separate pre-opportunity prospecting lifecycle for independent sources | Keeps future-client cultivation out of the active sales pipeline while preserving source and history through conversion | Prospecting volume or platform object limits require a different model |
| D-025 | Accepted | Use Centah only for Costco leads; keep independent business solely in the selected CRM and require Centah lead numbers only for Costco opportunities | Prevents false identifiers and unnecessary Centah synchronization | Company workflow or Centah scope changes |
| D-026 | Accepted | Require every active prospect to have a reachable channel/location, source, next action, and date; use three attempts, one 90-day nurture attempt, and explicit retained outcomes | Replaces memory-driven prospecting with bounded, searchable work | Observed prospecting results justify cadence changes |
| D-027 | Accepted | Branch post-sale handoff by source and enforce installation checks through a three-month exception | Costco sales use DocuSign plus the internal-order email; independent sales use the internal-order email; overdue installations receive a same-day verified escalation | Handoff or installation timing changes |
| D-028 | Accepted | Prospect eligible past customers at 6, 12, 18, and 24 months after post-install follow-up, then stop | Supports repeat work and referrals without indefinite reminders | Conversion, customer feedback, or outreach policy changes |
| D-029 | Accepted | Record communication provenance, preferences, permission state, and opt-outs; require compliance review before purchased-list imports or automated outreach | Supports channel-aware human review and prevents premature automation | Applicable rules, channels, or automation scope changes |
| D-030 | Accepted | Use a hybrid ChatGPT Project strategy: one pinned guided chat for the active checkpoint and separate chats for materially distinct outcomes | Preserves short-term conversational continuity without mixing research, configuration, implementation, and review into one unbounded transcript | Handoffs become unreliable or chat overhead exceeds value |
| D-031 | Accepted | Treat Markdown as the live source of truth and generate the Word distribution copy only at a final release or explicit sharing milestone | Keeps every checkpoint fast and visible while retaining a polished sharing artifact when it is actually needed | A stakeholder requires synchronized Word copies during execution |
| D-032 | Accepted | Back up the authoritative Markdown and project-control files to `jonah-dawg/loryn-work-optimization` on GitHub | Provides version history and recovery outside the app-managed ChatGPT Project directory | Repository ownership, visibility, or working-location strategy changes |
| D-033 | Accepted | Convert a prospect into one project-specific opportunity when a real project is confirmed and the initial consultation is scheduled | Preserves the customer and prospecting history, starts the opportunity at `Consultation Scheduled`, and makes the morning-of confirmation its first required next action; immediate-project inquiries may enter there directly | The observed sales process needs an earlier or later qualification point |
| D-034 | Accepted | Use ten plain-language active-opportunity stages from `New Customer Request` through `Finished`, with `Lost / Canceled` as an exit and overdue installation as a visible exception | Gives the consultant understandable job statuses while avoiding unverified claims that an order was placed or installation was scheduled | Daily use shows a missing state, ambiguous wording, or a state the consultant cannot reliably verify |
| D-035 | Superseded | Require the first manual contact attempt by closing time when a new request arrives during working hours, or at 10:00 a.m. on the next working day when it arrives outside working hours | The original 10:00 a.m. start was replaced by the 9:00 a.m. calling-hours rule in D-037 | Retained for decision history |
| D-036 | Accepted | After an unanswered first attempt, retry on the next working day and once more two working days later; after a third nonresponse, close the active request as `Lost / Canceled - No Response` | Creates a bounded three-attempt sequence, preserves the activity record, and stops active-job reminders without changing the separate prospect-nurture rules | Response results show the cadence is too fast or slow, or source policy requires different treatment |
| D-037 | Accepted | Use calling hours of 9:00 a.m.-6:00 p.m. Monday-Friday and 9:00 a.m.-2:00 p.m. Saturday, while keeping approximately 7:45 a.m. for manual same-day appointment-confirmation texts only | Prevents early lead and follow-up calls while preserving the established confirmation routine; outside-hours new requests are due at 9:00 a.m. on the next working day | Availability, customer feedback, or observed response patterns justify different hours |
| D-038 | Accepted | Set the primary quote deadline to the end of the same working day as the completed appointment | Reflects the desired fast customer response and creates a visible overdue task when the quote is not sent that day | Actual quote complexity or workload shows that a different default is needed |
| D-039 | Accepted | If the same-day quote target is missed, require a short delay reason and set the fallback deadline to the end of the next working day | Prevents a missed quote from disappearing and gives the consultant one clear recovery deadline | Actual quote workload shows that a different fallback is more realistic |
| D-040 | Superseded | Create the first manual customer follow-up two working days after a quote is sent, canceling the reminder if the customer responds earlier | Replaced by D-041, which adds an immediate quote-sent notice and moves the next decision follow-up to three working days later | Retained for decision history |
| D-041 | Accepted | Immediately notify the customer manually after emailing the quote, then create the next decision-follow-up task for three working days later | Confirms that the customer should check their email and replaces memory-driven follow-up with a dated task without automatic sending | Customer response patterns justify a different interval or channel |
| D-042 | Accepted | If the three-working-day post-quote follow-up receives no response, create another manual follow-up for one week later during normal calling hours | Keeps the active quote visible without contacting the customer too frequently | Customer response patterns or a later stopping rule justify a different interval |
| D-043 | Accepted | After the three-working-day check, follow up weekly for up to three weeks; after a third weekly nonresponse, close as `Lost / Canceled - No Decision`, unless the customer requested a specific later date | Prevents indefinite reminders while preserving customer-directed timing, the quote, and communication history | Sales-cycle evidence shows the sequence is too short or long |

## 14. Immediate next actions

- [x] Confirm the synthetic-only trial boundary and approved real-data transfer scope.
- [ ] Obtain Centah integration documentation, sandbox access, sanitized sample payloads, status dictionary, and support process.
- [x] Conduct a workflow interview and map one Costco/Centah lead from receipt through post-install follow-up.
- [x] Define independent-lead and prospecting sources, minimum capture, cadence, conversion, exit, source branching, and past-customer outreach.
- [ ] Approve the canonical pipeline, next-action invariant, minimum fields, and mandatory platform requirements.
- [ ] Create the weighted platform scorecard and scripted mobile test scenarios.
- [ ] Configure the synthetic core workflow in Zoho CRM Free.
- [ ] Reproduce the same scenarios in HubSpot Free and document the Centah-only baseline.
- [ ] Review likely paid-tier costs, data portability, retention, permissions, API limits, and support before selecting the pilot platform.
- [ ] Initialize the lightweight repository structure and baseline `AGENTS.md` for plans, configuration records, decisions, and any later connector code.
- [ ] Agree on a lightweight recurring check-in cadence for reviewing progress and decisions.

## 15. References and evidence boundary

- [Centah platform features](https://www.centah.com/platformfeatures/) - public description of REST APIs, webhooks, calendar synchronization, lead capture, and mobile field capabilities. Confirm account-specific implementation details directly with Centah.
- [Centah platform overview](https://www.centah.com/) - public description of the home-services lead-management platform and integration engine.
- [Zoho CRM pricing and editions](https://www.zoho.com/crm/zohocrm-pricing.html) - official current description of Free and paid tier users, CRM features, workflows, mobile access, and API availability.
- [Zoho CRM API limits](https://www.zoho.com/crm/developer/docs/api/v8/api-limits.html) - official current API credit and concurrency limits by edition.
- [HubSpot free CRM tools](https://www.hubspot.com/pricing/crm) - official current Free and Starter positioning, user limits, record limits, and email connectivity.
- [HubSpot workflow availability](https://knowledge.hubspot.com/workflows/create-workflows) - official subscription requirements for the full workflow builder.
- [HubSpot API usage guidelines](https://developers.hubspot.com/docs/developer-tooling/platform/usage-guidelines) - official API limits and application guidance.
- [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-projects-in-chatgpt) - official guidance on project chats, files, instructions, and shared context.
- [Projects and chats](https://learn.chatgpt.com/docs/projects) - official organization guidance for ChatGPT and local projects.
- [Long-running work](https://learn.chatgpt.com/docs/long-running-work) - official guidance to keep related work in one chat, use separate chats for independent outcomes, and preserve related sources in a project.
- [Custom instructions with AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md) - official Codex instruction discovery and layering guidance.
- [Worktrees](https://learn.chatgpt.com/docs/environments/git-worktrees) - official Codex desktop guidance for isolated parallel repository work.

**Evidence note:** Centah, Zoho, and HubSpot product capabilities and tier limits above are based on official public pages reviewed July 29, 2026. Pricing, limits, and packaging can change and must be revalidated in the trial tenant before platform selection. OpenAI's current project and long-running-work guidance was reviewed July 29, 2026 for the chat strategy. CP-001 confirmed the approved real-data transfer scope, and CP-002 approved the independent-lead and prospecting workflow requirements. The plan still does not assume a Centah API contract, an approved Centah connection method, or communications compliance for purchased lists or automated outreach; those remain discovery gates.

## 16. Guided execution, sign-off, and session continuity

Execute this plan as a sequence of small, interactive work units. The durable control files are stored under `project-control/`:

- `GUIDED_WORKFLOW.md` defines how a session starts, progresses, closes, and resumes.
- `CURRENT_STATE.md` is the single restart point and must describe the current phase, active work unit, completed work, blockers, and next action.
- `SESSION_LOG.md` is append-only and records completed work, validation, decisions, sign-offs, and the saved restart point.
- `ARTIFACT_REGISTER.md` identifies authoritative project files, their synchronization state, and when they must be updated.

### Interactive work-unit cycle

1. **Orient** - read the current state, latest signed-off checkpoint, relevant plan section, and unresolved decisions; report a short starting summary.
2. **Frame** - state the work-unit outcome, inputs needed, decisions to make, acceptance checks, and anything explicitly out of scope.
3. **Work interactively** - gather information, draft or configure the smallest useful increment, and keep assumptions separate from confirmed facts.
4. **Validate** - check the output against acceptance criteria, evidence, governance rules, and downstream dependencies; identify conflicts or gaps.
5. **Review** - present the result, material changes, unresolved items, and a clear recommendation to accept, revise, or defer.
6. **Sign off** - record user approval only after the user explicitly accepts the checkpoint. Approval may cover one work unit or an entire phase gate.
7. **Synchronize and save** - update every affected authoritative artifact, reconcile statuses and decisions, append the session log, and write the exact next action to `CURRENT_STATE.md`.

### Sign-off rules

- Do not treat silence, topic changes, or partial agreement as approval.
- Before requesting sign-off, list the checkpoint ID, what is being approved, validation performed, open risks, and what approval unlocks.
- A signed-off checkpoint is immutable in the session log. Later changes supersede it with a new checkpoint and decision record rather than rewriting history.
- A phase may close only when its roadmap gate is satisfied or an explicit exception is accepted and recorded.
- Production data, external integrations, customer communications, purchases, and destructive actions always retain their separate authorization requirements; checkpoint approval does not broaden authority.

### End-of-session reconciliation

At a sign-off or whenever the user asks to stop for the day, complete these checks:

- Confirm the authoritative Markdown and control files agree on material scope, phase status, and accepted decisions.
- Update the decision log for new, changed, rejected, or superseded decisions.
- Update `CURRENT_STATE.md` with the last signed-off checkpoint, current phase, active work unit, blockers, and one precise next action.
- Append `SESSION_LOG.md` with work completed, validation evidence, user sign-off status, files changed, and the resume instruction.
- Update `ARTIFACT_REGISTER.md` when a durable artifact is added, renamed, superseded, or becomes stale.
- Verify that no assumption is labeled as confirmed, no completed item remains marked pending, and no sensitive data was copied into an unauthorized artifact.
- Mark the Word distribution copy stale when Markdown changes; regenerate and visually verify it only at a final release or explicit sharing milestone.

### Resume behavior

At the start of a later session, read `CURRENT_STATE.md` first, then the latest signed-off entry in `SESSION_LOG.md`, the relevant master-plan section, and any referenced decision or artifact. Present a brief reconciliation summary before continuing. If the files conflict, pause execution, explain the conflict, and repair the durable state before doing new work.
