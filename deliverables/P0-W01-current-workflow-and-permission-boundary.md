# P0-W01 - Current Workflow and Permission Boundary

**Status:** Approved - CP-001 signed off July 29, 2026  
**Phase:** Phase 0 - Authority, workflow, and evaluation design  
**Updated:** July 29, 2026

## Work-unit outcome

Document the current Costco/Centah lead workflow and establish the boundary between synthetic experimentation and actions requiring company permission.

## Confirmed current workflow

### 1. Lead receipt

- The lead first appears in Centah.
- Centah provides the customer's name, phone number, full address, and email address.

### 2. Initial contact

- The consultant calls the lead.
- If the lead answers, the consultant schedules an initial meeting.
- She records the meeting in both Centah and her iPhone calendar.
- On the morning of the appointment, she manually contacts the customer to confirm or remind them.
- The default confirmation is a text message sent at approximately 7:45 a.m.
- She uses email or a phone call instead when the customer requests a different communication method.
- The consultant may add notes describing what the lead is interested in.
- If the lead does not answer, the consultant records notes about the contact attempt.
- Contact-attempt notes and customer-interest notes are recorded directly in Centah.
- The consultant makes up to three contact attempts before canceling the unresponsive lead in Centah.
- Canceling the lead makes it inactive; it does not permanently delete the record.

### 3. Consultation, quote, and follow-up

- The consultant meets with the client.
- She creates the quote in Google Sheets.
- Completed Google Sheets quotes are stored in her personal Google account.
- She saves the completed quote as a PDF and emails the PDF to the client.
- She enters the quoted amount in Centah under the lead information.
- The detailed quote remains in Google Sheets/PDF while Centah stores only the quoted dollar amount; the quote PDF is not attached to the Centah lead.
- She follows up until the client provides a yes or no decision.
- To find customers needing quote follow-up, she reviews prior appointments in her iPhone calendar.
- She sends follow-up text messages when time becomes available between other work.
- After sending a follow-up, she relies on the text conversation for history and on her memory for the next follow-up.
- There is no dedicated follow-up task, consistent due date, or automatic prompt.
- If the client accepts, the lead progresses to sold.
- After acceptance, the consultant sends the customer a DocuSign document.
- She sends the quote to the company coordinator, who schedules final measurements and places the order.
- The DocuSign request and the quote handoff to the company coordinator happen in parallel.
- The consultant sends the quote to the company coordinator by email.
- The email is the only confirmed record of the internal handoff; no separate task or handoff tracker is used.
- The company coordinator does not provide the consultant with updates when final measurements are scheduled or the order is placed.
- The consultant therefore has no confirmed post-handoff status view for those milestones.
- Customers may continue contacting the consultant directly for questions, follow-ups, and future repairs, but ongoing support and repair management are outside the initial CRM scope.
- The typical elapsed time from quote delivery to installation is approximately five to six weeks.
- For this plan, the required post-sale workflow is limited to one post-install follow-up due no later than six weeks after the DocuSign request is sent.
- The CRM should create or surface that follow-up from the DocuSign-sent date; it does not initially need to manage indefinite post-sale service activity.
- At the six-week checkpoint, if installation is complete, the consultant performs the post-install follow-up.
- If installation is not complete, she adds a note and reschedules the reminder for another two to three weeks.
- The two-to-three-week deferral repeats while installation remains incomplete.
- Once installation is confirmed, the open reminder becomes the single post-install follow-up.
- If the client declines, she cancels the lead in Centah using the same process used for an unreachable lead; the retained record becomes inactive.

## Draft workflow map

```text
Lead received in Centah
-> Consultant calls lead
   -> Answered: record interests as needed and schedule initial meeting
      -> Enter appointment in Centah
      -> Enter the same appointment in iPhone calendar
      -> At approximately 7:45 a.m., manually text the customer
         -> Use email or a phone call instead when requested
   -> No answer: record attempt and retry, up to three attempts
      -> Still no answer: cancel in Centah, making the retained record inactive
-> Initial meeting occurs
-> Create quote in Google Sheets
-> Save quote as PDF
-> Email PDF to client
-> Enter quoted amount in Centah
-> Review prior iPhone calendar appointments when time permits
-> Send follow-up texts
-> Follow-up history remains in text conversation
-> Next follow-up depends on memory rather than a task or due date
   -> Yes: mark/progress lead as sold
      -> In parallel:
         -> Send DocuSign to customer
         -> Email quote to company coordinator
            -> Email is the only handoff record
         -> Coordinator schedules final measurements
         -> Coordinator places the order
         -> No status update returns to consultant
      -> Typical quote-to-install cycle: approximately 5-6 weeks
      -> Follow-up checkpoint due no later than 6 weeks after DocuSign is sent
         -> Installed: perform post-install follow-up
         -> Not installed: add note and reschedule reminder by 2-3 weeks
            -> Repeat until installation is confirmed
   -> No: cancel in Centah, making the retained record inactive
```

## Current system map

| Workflow information or action | Current location |
|---|---|
| Lead identity, contact information, address, Centah lead number | Centah |
| Contact attempts and customer-interest notes | Centah |
| Appointment | Centah and iPhone Calendar |
| Morning-of confirmation | Manual text at approximately 7:45 a.m.; email or phone by customer request |
| Detailed quote | Google Sheets in the consultant's personal Google account |
| Customer quote copy | PDF sent by email |
| Quoted dollar amount | Centah |
| Quote follow-up history | Text conversation |
| Next quote follow-up | Consultant's memory and review of prior iPhone Calendar appointments |
| Accepted-sale document | DocuSign |
| Internal handoff | Quote emailed to company coordinator; email is the only handoff record |
| Final-measurement and order status | Not visible to the consultant after handoff |
| Post-install follow-up | No current task system; new CRM rule defined in this work unit |

## Confirmed workflow problems

- Appointments are entered separately in Centah and iPhone Calendar.
- Morning-of customer confirmations are sent manually.
- Quote preparation crosses Google Sheets, PDF, email, and Centah, with manual dollar-amount entry.
- Quote follow-ups have no task, due date, or consolidated activity history.
- The internal sale handoff is tracked only by email.
- The consultant receives no final-measurement or order-status update after handoff.
- Detailed customer quotes are retained in a personal Google account while Centah stores only the dollar amount.

## Open workflow and governance questions for later phases

- Whether the detailed Google Sheet/PDF quote should remain outside the CRM, be linked, or be stored as an approved CRM attachment.
- Whether the personal Google account may be connected to the selected CRM or should be replaced with an approved storage location.
- The exact Centah export/API mechanism, status dictionary, update limits, and duplicate-handling rules.

## Permission boundary

### Confirmed

- The consultant performs this work as an independent contractor.
- She may create a personal Zoho or HubSpot trial using only fictional records and no company information without company permission.
- She is permitted to copy or export real Centah/Costco customer information into another CRM.
- The permitted field set includes customer name, phone number, email address, full address, Centah notes, appointments, and quoted amount.
- Only active and sold Centah leads should be copied into and retained by the selected CRM.
- Canceled/inactive Centah leads should not transfer into the selected CRM.
- Each transferred record must include its Centah lead number as an external reference.
- A returning customer receives a new Centah lead number for each new order.
- The Centah lead number therefore belongs on the lead/opportunity (order), not on the reusable customer record.
- One customer record may be related to multiple lead/opportunity records over time.
- No real customer information has been copied into this project artifact.
- Discovery examples and repository fixtures must remain sanitized even though an approved production CRM may later hold real records.

### Unknown or deferred

- Whether full quote files, beyond the approved quoted amount, may be copied into the selected CRM.
- Whether the consultant's personal Google account may connect directly to the selected CRM.

## Acceptance status

- [x] Lead receipt and high-level contact-to-decision path captured.
- [x] Systems used at each step identified; Centah holds lead data and activity notes, while iPhone Calendar, text/phone/email, Google Sheets, PDF, DocuSign, and email support other steps.
- [x] Repeated entry, delays, and failure points identified.
- [x] Primary follow-up gap identified: quote follow-ups are found by reviewing past iPhone calendar appointments and handled when spare time permits.
- [x] Follow-up tracking gap confirmed: history remains in text conversations and the next action depends on memory.
- [x] Internal handoff gap confirmed: the emailed quote is the only record sent to the company coordinator.
- [x] Post-sale visibility gap confirmed: the consultant is not updated when final measurements are scheduled or the order is placed.
- [x] Initial post-sale scope confirmed: a six-week checkpoint after DocuSign leads to the post-install follow-up or repeated, noted two-to-three-week deferrals until installation is complete; ongoing support and repair management are out of scope.
- [x] Typical quote-to-install cycle captured: approximately five to six weeks.
- [x] Meaning of lead cancellation confirmed: the Centah record is retained and made inactive.
- [x] Declined-quote outcome confirmed: cancel the Centah lead and retain it as inactive.
- [x] Quote storage split confirmed: Google Sheets/PDF contains the detail; Centah contains only the dollar amount.
- [x] Synthetic-only and production-data permission boundaries confirmed: synthetic trials require no permission; approved fields may transfer for active and sold leads; canceled/inactive leads remain excluded.
- [x] Centah lead-number placement confirmed: store it on the lead/opportunity because each new order receives a new number.
- [x] Draft reviewed and signed off at CP-001.

## Accepted scope decisions from discovery

- Create a follow-up checkpoint due no later than six weeks after the DocuSign request is sent. If installation is complete, perform the post-install follow-up; otherwise add a note and reschedule it by two to three weeks, repeating until installation is confirmed.
- Do not include ongoing support or future repair-case management in the initial CRM scope.
- Transfer only active and sold Centah leads into the selected CRM; exclude canceled/inactive leads.
- Require the Centah lead number on every transferred lead/opportunity as the external reference used for traceability and deduplication.
- Model customers separately from orders: a returning customer may have multiple opportunities, each with a different Centah lead number.

## CP-001 approval effect

Phase 0 may rely on this workflow and permission boundary when defining the minimum CRM fields, pipeline stages, next-action rules, synthetic test records, and platform scorecard. This approval does not authorize creating a production CRM, importing real records, connecting Centah or Google, or sending customer communications.
