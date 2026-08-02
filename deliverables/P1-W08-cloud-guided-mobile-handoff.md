# P1-W08 - Cloud-Guided Mobile Session Handoff

**Status:** Unapproved draft - do not share or use with Loryn yet

**Phase:** Phase 1 - simplified personal CRM selection

**Work unit:** P1-W08 - finalist practical-session execution

**Source authority:** D-119 and `P1-W08-finalist-practical-session-contract.md`

## Proposed outcome

Let Loryn complete the already-approved OnePageCRM and Capsule practical sessions on her iPhone through a dedicated shared ChatGPT Project. The cloud chat acts as the neutral session guide, presents one task at a time, accepts short spoken or typed responses, and produces a sanitized handoff for repository reconciliation.

This proposal changes the facilitation method only. It does not change the approved fixtures, task order, 15-to-20-minute limit, acceptance rules, privacy boundary, tier boundary, or prohibition on CRM selection.

## Approval required before use

The following external stage requires explicit approval because it adds a shared cloud project and changes how Loryn participates:

- **Actors:** the project owner and Loryn.
- **Systems:** a dedicated shared ChatGPT Project, OnePageCRM, and Capsule on Loryn's iPhone.
- **Data:** only the synthetic fixtures and non-identifying task outcomes in this document.
- **Actions:** create the dedicated project, invite Loryn with Chat access, add this approved handoff as its only source, run one chat per finalist, and return the sanitized summaries.
- **Exclusions:** no real customer data, screenshots, credentials, account identifiers, billing, integrations, communications, production use, CRM selection, or checkpoint sign-off.
- **Stopping rules:** the existing P1-W08 rules plus immediate stop if the chat asks for private information, exposes another project member's private content, or materially increases Loryn's burden.

Drafting this file does not approve or start that stage.

## Recommended cloud structure

Create a dedicated ChatGPT Project named `Loryn CRM Finalist Sessions` only after approval.

1. Use `Only those invited`, not `Anyone with a link`.
2. Invite Loryn with `Chat` access. She does not need Edit access.
3. Add only the approved version of this handoff as a Project source.
4. Do not add the repository, the stale P0-W03 collaborator packet, CRM screenshots, account pages, exports, or private vendor messages.
5. Create two separate chats:
   - `OnePageCRM mobile session`
   - `Capsule mobile session`
6. Run the chats on different occasions if doing both together would create fatigue.

Shared-project members can see project chats, files, and member information. The dedicated minimum-source project keeps that visibility proportionate to this short task.

## Owner preparation before each session

The owner or facilitator completes this work without using session time:

- Confirm the correct synthetic tenant is open and the intended product/tier boundary is unchanged.
- Reset Jordan to overdue yesterday, Taylor to due today, and Casey to due tomorrow.
- Confirm Avery Brooks is absent.
- Confirm the phone has an ordinary network connection and no private notification is visible.
- Let Loryn sign in privately. Credentials, MFA, recovery details, and account identifiers never enter ChatGPT.
- Preconfigure a normal 20-minute phone timer. Loryn starts it only when the cloud guide tells her to begin.
- Open the correct CRM on the iPhone and the matching cloud chat.
- Tell the chat `ready` only after login, setup, timer preparation, and app switching are complete.

Chat switching, login, and facilitator reset time are not scored as CRM friction. If switching between ChatGPT and the CRM makes the test unfair, stop and use the original facilitator-led method.

## Project instructions to copy

```text
You are the neutral mobile-session guide for P1-W08, a comparison of OnePageCRM Professional and Capsule Starter. The attached handoff is authoritative for this session. CP-010 remains the last signed checkpoint, D-119 authorizes only the bounded synthetic evaluation, and no CRM is selected.

Protect the participant's privacy. Never ask for or repeat a real name beyond the synthetic fixtures, email address, telephone number other than the reserved synthetic numbers, credential, MFA code, recovery detail, account identifier, tenant URL, screenshot, notification, or real customer information. Do not ask the participant to upload images or files. If private information appears or is offered, tell the participant to stop and contact the project owner without repeating it.

Guide exactly one finalist session per chat. Confirm the product name before starting. Do not combine products in one chat. Do not browse the web, use apps or connectors, operate the CRM, send communications, or claim that a task succeeded without the participant's report.

Wait for the participant to say ready. Then tell the participant to start the preconfigured 20-minute phone timer and begin Task 1. Do not claim that you can independently measure elapsed time. Present the six tasks from the attached handoff one at a time and in order. After each task, ask for only one of: done, help, blocked, or stop. Short voice or typed answers are enough; the participant has no documentation assignment.

If the participant says help, use the exact neutral prompt: What would you try next? Count that prompt. If the participant still needs help, give only one label-level hint from the approved hint bank in the handoff and count it as product-specific help. Never invent a button, menu, saved state, or product behavior. If the hint bank does not resolve the issue, record blocked and continue only if the participant wants to continue.

After each reported completion, ask one short check: Did the change visibly save? Record clear, uncertain, or failed. Do not ask for screenshots or account details.

Stop immediately if the participant says stop, the external timer sounds, a login/device/network/accessibility problem makes the comparison unfair, billing or an external connection is requested, a real communication could be sent, real data is needed, or private information could enter the chat.

At the end, ask the short feedback questions in the handoff. Then produce the exact sanitized result format from the handoff. Do not include raw chat excerpts, credentials, account information, private names, or unsupported inferences. End with: Unapproved participant input for local repository reconciliation; CP-010 remains the last signed checkpoint; no CRM is selected.
```

## Approved label-level hint bank

The cloud guide may use only these hints after the neutral recovery prompt fails:

| Product | Concept | Allowed hint |
|---|---|---|
| OnePageCRM | Person record | Look for `Contacts`. |
| OnePageCRM | Follow-up | Look for an `Action` or `Next Action`. |
| OnePageCRM | Work due now | Look for the `Action Stream`. |
| OnePageCRM | Project status | Look for the `Pipeline` or the contact's deal. |
| Capsule | Person record | Look for `People & Organizations` or `People`. |
| Capsule | Follow-up | Look for `Tasks`. |
| Capsule | Work due now | Open the task list and use its due-date groups. |
| Capsule | Project status | Look for the `Sales Pipeline` or the person's opportunity. |

If the visible mobile label differs, the guide records a blocked step or requests the owner to revise the approved hint bank after the session. It does not improvise navigation instructions.

## Launch prompt for each finalist chat

Replace `[PRODUCT]` with `OnePageCRM` or `Capsule` and `[ORDER]` with `first` or `second`. Use one first session and one second session; record the chosen order rather than asking the cloud guide to infer it.

```text
Read the Project instructions and the attached P1-W08 cloud-guided mobile handoff. This chat is only for the [PRODUCT] mobile session on an iPhone 17 Pro Max running iOS 26.6. This is the [ORDER] finalist session.

Confirm the product, session order, privacy boundary, synthetic-only rule, and external 20-minute timer rule. Do not give Task 1 until I say ready and then confirm that I started the timer. Guide one task at a time and accept short replies: done, help, blocked, or stop. Ask the cross-product preference only if this is the second session. At the end, produce the sanitized P1-W08 Mobile Session Handoff for this product.
```

## Common participant tasks

The guide presents these tasks without adding product-specific navigation:

1. Create Avery Brooks from the synthetic text lead: phone `202-555-0144`, source `Referral`, note `Asked about living-room roller shades`, status `New`, and a next action due tomorrow.
2. Find Jordan Lee first by last name and then by phone `202-555-0116`; review the record and complete or reschedule the overdue action.
3. Open Taylor Morgan, explain what happened previously, add `Customer asked for a fabric-color comparison`, and set the next follow-up.
4. Open today's and overdue work and identify what needs attention now.
5. Move Casey Rivera to `Appointment Scheduled` and confirm that the earlier call note is still understandable.
6. Return to the main work view and explain what should happen next.

## Short feedback questions

After Task 6 or a stopping rule, ask one question at a time:

1. `Would you use this CRM, use it with reservations, or not use it?`
2. `What felt easiest?`
3. `What felt most annoying or confusing?`
4. In the second finalist chat only: `Which do you prefer: OnePageCRM, Capsule, no preference, or neither? Why?`

## Sanitized result format

```markdown
# P1-W08 Mobile Session Handoff

- Product: [OnePageCRM or Capsule]
- Tier boundary: [Professional-equivalent or Starter]
- Date: [date only]
- Device: iPhone 17 Pro Max; iOS 26.6
- Fixture reset confirmed by owner: [Yes or No]
- Session order: [First or Second]
- Approximate task time: [participant-reported minutes from the external timer, excluding setup and login]
- Stopping rule reached: [None or short sanitized reason]

| Task | Result | Neutral prompts | Product hints | Visible save |
|---|---|---:|---:|---|
| 1 - Create Avery | [Completed / Completed with help / Blocked / Stopped] | [count] | [count] | [Clear / Uncertain / Failed / Not reached] |
| 2 - Find and update Jordan | [...] | [...] | [...] | [...] |
| 3 - Review and update Taylor | [...] | [...] | [...] | [...] |
| 4 - Today and overdue work | [...] | [...] | [...] | [...] |
| 5 - Move Casey and verify history | [...] | [...] | [...] | [...] |
| 6 - Return to main work view | [...] | [...] | [...] | [...] |

- Today/overdue clarity: [Clear / Usable with help / Blocked / Not reached]
- History clarity: [Clear / Usable with help / Blocked / Not reached]
- Next-action discipline: [Maintained / Not maintained / Unverified]
- Routine burden: [one short sanitized observation]
- Participant acceptability: [Would use / Would use with reservations / Would not use]
- Participant reason: [one short sanitized reason]
- Preference after second session: [OnePageCRM / Capsule / No preference / Neither / Not asked]
- Preference reason: [one short sanitized reason or Not asked]
- Fairness or method limitation: [None or short note, including chat-switching burden]

Unapproved participant input for local repository reconciliation; CP-010 remains the last signed checkpoint; no CRM is selected.
```

## Return path

Because the proposed Project is shared, the owner can read each finished chat without asking Loryn to copy or reformat anything. The owner returns the two sanitized handoffs to the local repository task, checks them against the approved contract, removes any private or unsupported content, and prepares the P1-W08 result and recommendation for explicit review. Chat output is participant input, not repository authority, CRM selection, or checkpoint approval.

## Official ChatGPT basis

- OpenAI documents that shared Projects are available on web, iOS, and Android and that Chat access lets a member interact with the Project's chats, files, and instructions.
- OpenAI also documents that shared-project members can see Project chats, files, and member information. This is why the proposed Project is dedicated, invite-only, and limited to this single approved handoff.
- Source: [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-projects-in-chatgpt).

## Draft acceptance review

- [x] One dedicated chat is used per finalist.
- [x] The approved six-task order and synthetic fixtures are preserved.
- [x] The guide asks one mobile-friendly question at a time.
- [x] Loryn can answer with short voice or typed responses and has no evidence-writing assignment.
- [x] The neutral recovery prompt and counted label-level hints preserve comparability.
- [x] The 20-minute, privacy, billing, connection, communication, and fairness stopping rules are preserved.
- [x] The result format is sanitized and ready for repository reconciliation.
- [x] The cloud Project remains uncreated and unshared pending explicit approval.

## Proposed next action

Review or revise this draft. If accepted, explicitly approve the P1-W08 cloud-guided mobile handoff and authorize the exact dedicated shared-Project stage described above. Only then create or share the Project and begin Loryn's first finalist chat.
