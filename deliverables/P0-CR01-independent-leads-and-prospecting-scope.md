# P0-CR01 - Independent Leads and Prospecting Scope

**Status:** Approved at CP-002  
**Approved:** July 29, 2026  
**Recorded:** July 29, 2026  
**Triggered during:** P0-W02 pipeline design

## Confirmed requirement

The consultant receives or develops business outside the Centah/Costco channel. The CRM must support:

- independently sourced leads that may never exist in Centah;
- prospect records for people who are not ready to request a quote or schedule a consultation;
- future-client prospecting with deliberate follow-up dates instead of relying on text history or memory; and
- conversion of a qualified prospect into the normal consultation, quote, sale, installation-check, and post-install workflow.

## Immediate modeling consequences

- `Lead source` is required for every prospect or opportunity.
- The source must preserve enough detail to distinguish referrals, builders, networking, past customers, social media, purchased lists, local businesses, direct outreach, and Centah/Costco.
- A prospect may be created with partial information when only a business name or social-media identity is known.
- Every prospect requires a name or business identifier, at least one reachable channel or location, a source, a next action, and a follow-up date.
- A Centah lead number is required only when the source record came from Centah. It is not required for independently sourced prospects or opportunities.
- Prospecting is a pre-opportunity workflow and should not distort the active sales pipeline.
- A reusable customer/person record may exist before an opportunity or order exists.
- When a prospect becomes a real sales opportunity, the CRM must preserve the prospecting history.

## Proposed boundary for discovery

The first design should distinguish:

1. **Prospect:** a possible future client who is not yet ready for the active sales process.
2. **Independent lead:** a person who has shown enough interest to begin contact attempts or schedule a consultation, but whose lead did not originate in Centah.
3. **Centah lead:** a Centah-originated opportunity governed by the existing Centah transfer and identifier rules.

These definitions are proposals until the discovery questions below are answered and the user signs off.

## Discovery record

### Prospect and independent-lead sources

The system must support all of the following sources:

- referrals;
- builders;
- networking;
- past customers;
- social media;
- purchased lists;
- local businesses;
- direct outreach; and
- Centah/Costco for the existing governed channel.

The CRM should record both a broad source category and optional source detail, such as the referring person, builder, event, social platform, list/vendor, business, campaign, or Costco/Centah context. The treatment of purchased lists and outbound contact remains subject to a later consent and communications-compliance review.

### Minimum prospect record

The approved minimum record is:

- a person name, business name, or social-media identity;
- at least one reachable channel or location: phone, email, social handle, or address;
- prospect source and optional source detail;
- next action; and
- follow-up date.

Other details may be added later. A prospect with only a business name or social-media account is valid if the record still includes a practical next action and date.

### Prospecting activities

The CRM must support these activity types:

- call;
- text;
- email;
- social-media message;
- in-person visit or networking conversation;
- mailed material;
- referral request or introduction;
- research or preparation; and
- general note.

Each completed activity records its result and either establishes the next action and follow-up date or closes the prospect. Activity logging does not authorize automatic customer communication; initial use remains human-reviewed and manually sent.

### Default reminder cadence

The CRM will propose these defaults, all of which the consultant may override:

| Prospect condition | Default next reminder |
|---|---:|
| Engaged and requested information | 2 days |
| Warm prospect or referral | 7 days |
| Cold outreach or purchased-list prospect | 30 days |
| Long-term prospect | 90 days |
| Past customer with possible future work | 6 months |

These are reminder intervals, not automatic-send schedules. A prospect must always have a deliberate next action and date unless it has been closed or placed on a documented no-contact hold.

### Qualification and workflow convergence

- A direct independent inquiry about a current window-covering need enters the active sales workflow without first becoming a long-term prospect.
- A prospect converts into an active client opportunity when the person confirms a real project and an initial meeting date is scheduled.
- General interest, accepting information, or a possible future need does not trigger conversion; the record remains in prospecting.
- The prospect's source and activity history carry forward when it converts.
- Once the initial meeting is scheduled, an independent opportunity follows the same consultation, quote, follow-up, accepted/sold, installation-check, and post-install process as a Centah/Costco opportunity, except for the post-acceptance document step below.

### Post-acceptance source branch

| Opportunity source | Required post-acceptance actions |
|---|---|
| Centah/Costco | Send DocuSign and email the quote to the internal order coordinator in parallel. |
| Outside Centah/Costco | Do not send DocuSign; email the quote to the internal order coordinator. |

This branch must be driven by source so the CRM never presents DocuSign as required for independent business.

### Installation-check anchor

- For Centah/Costco sales, the six-week installation-check timer begins on the DocuSign-sent date.
- For sales outside Centah/Costco, the timer begins on the date the quote is emailed to the internal order coordinator.
- If installation has not occurred at the checkpoint, add a note and defer the reminder by two to three weeks, repeating until installation is confirmed; then perform the single post-install follow-up already approved in CP-001.
- Installation is expected to occur no later than three months after the sold quote is emailed to the internal order coordinator.
- The workflow must not silently extend ordinary installation reminders beyond that three-month boundary; an unconfirmed installation at that point must appear as an exception requiring attention.

If installation remains unconfirmed at three months, the CRM must:

1. flag an overdue-installation exception;
2. create a same-day task to contact the internal order coordinator for status;
3. require the result to be recorded;
4. prompt the consultant to contact the customer if the coordinator cannot confirm installation; and
5. keep the installation unconfirmed until a person verifies it rather than marking it installed automatically.

### Prospect outcomes and exit rules

| Condition | CRM outcome |
|---|---|
| Real project confirmed and initial meeting scheduled | Convert to an active opportunity and preserve source and history. |
| Prospect asks to be contacted later | Keep active with the requested follow-up date. |
| Three prospecting attempts receive no answer | Move to long-term nurture and create one final reminder for 90 days later. |
| Final nurture attempt receives no answer | Archive as `No response`. |
| Prospect declines | Archive as `Not interested`. |
| Prospect requests no further contact | Mark `Do not contact` immediately and suppress future outreach reminders. |
| Contact information is invalid | Archive as `Invalid information`. |
| Record is a duplicate | Merge or archive as `Duplicate` while preserving relevant history. |

Archived prospects remain searchable and are not permanently deleted through the normal workflow. Only active prospects require a next action and date.

### Communication preferences and permission record

The CRM must record:

- preferred contact method;
- how and when the contact information was obtained;
- contact-permission status: `Unknown`, `Directly provided`, `Existing relationship`, or `Opted out`;
- overall do-not-contact status, date, and reason; and
- channel-specific opt-outs when a person permits one channel but not another.

These fields inform the workflow but do not by themselves establish legal compliance. Importing purchased lists and enabling automated outreach remain blocked until a separate communications-compliance review is completed.

### Past-customer prospecting

- After the single post-install follow-up, an eligible past customer receives a prospecting reminder six months later.
- The outreach may seek additional window-covering work and referrals.
- Outreach may use a letter, email, text, or call according to the customer's preferred and permitted channel.
- A customer who opted out or has an unresolved installation or service problem is excluded from promotional prospecting.
- Any new order creates a new opportunity while retaining the reusable customer history and original-order history.

- If no new project results, reminders repeat at 6, 12, 18, and 24 months after the post-install follow-up, then stop.
- Any explicit rejection or opt-out stops the sequence immediately and marks the customer `Do not contact` for promotional outreach.
- If a new order results, create a new opportunity; any later past-customer cycle is based on that order's completed post-install workflow.

### System boundary by source

- Only Costco-originated leads are processed through Centah.
- Costco/Centah opportunities require their Centah lead number and follow the approved Centah transfer and authority rules.
- Independently sourced prospects and opportunities remain only in the selected CRM and do not receive a Centah lead number.
- Independent business is not manually entered into Centah and is not part of any future Centah synchronization.

## CP-002 acceptance review

- [x] Prospect, independent lead, and Centah lead are distinguishable.
- [x] Prospect sources and source details are defined.
- [x] Partial-record minimum fields are defined.
- [x] Prospecting activity types and default reminder cadence are defined.
- [x] Qualification and conversion into the sales workflow are defined.
- [x] Exit, archive, no-response, and do-not-contact rules are defined.
- [x] Communication-preference and permission fields are defined.
- [x] Source-specific DocuSign, internal handoff, and installation-check rules are defined.
- [x] Past-customer prospecting cadence and two-year maximum are defined.
- [x] Centah applies only to Costco-originated opportunities.

No implementation, live data use, CRM account configuration, or customer communication occurred during this scope change.

## Effect on current work

CP-002 approved this scope and it has been incorporated into Master Plan Version 1.6. P0-W02 is now ready to define separate but connected prospecting and active-opportunity lifecycles. The approved CP-001 current-state workflow remains valid for Centah/Costco leads and is extended, not superseded, by this change.
