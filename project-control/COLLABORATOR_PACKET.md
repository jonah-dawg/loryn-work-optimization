# Shared ChatGPT Project Collaborator Packet

**Purpose:** Let the operational collaborator answer guided planning questions asynchronously from the ChatGPT mobile app while the GitHub repository remains the durable source of truth.

**Current restart point:** CP-003 is the last signed-off checkpoint. P0-W03 is ready to begin by defining mandatory CRM platform requirements before weights, scores, trial accounts, or platform selection.

## Collaboration boundary

- Use the shared ChatGPT Project for guided questions, clarification, and draft handoffs.
- Use this GitHub repository for approved requirements, decisions, artifacts, and the exact restart point.
- Shared-chat discussion is not approval. A checkpoint remains unapproved until the user explicitly signs it off.
- Do not place real customer or prospect information, credentials, production exports, private integration payloads, or restricted documents in ChatGPT or this repository.
- Do not create CRM accounts, connect Centah, Google, calendar, or email, import real records, purchase anything, or send communications during P0-W03.
- If two people want to explore different directions, branch the chat. Do not attempt to edit the same durable artifact concurrently.

## One-time shared Project setup

1. Create a cloud ChatGPT Project named `Loryn Work Optimization`.
2. Share it with the operational collaborator. Chat access is enough to answer questions; edit access is needed only if she should manage project files or instructions.
3. Paste the Project instructions below into the shared Project.
4. Add these five repository files as Project sources:
   - `project-control/COLLABORATOR_PACKET.md`
   - `project-control/CURRENT_STATE.md`
   - `project-control/GUIDED_WORKFLOW.md`
   - `deliverables/P0-W02-target-lifecycle-next-actions-and-minimum-fields.md`
   - `deliverables/window-sales-operations-master-plan.md`
5. Create one chat named `P0-W03 - Loryn guided questions` and paste the launch prompt below.
6. After an approved repository checkpoint, replace stale Project sources with the current versions and record the new checkpoint in the chat.

## Project instructions to copy

```text
You are facilitating the Loryn Work Optimization project for a two-person team. The attached Markdown sources are authoritative; chat discussion is not authoritative.

At the beginning of a guided session, state the current phase, active work unit, last signed-off checkpoint, open blockers, and the proposed session outcome. The expected starting point is CP-003 complete and P0-W03 ready to define mandatory CRM platform requirements before scorecard weights.

Ask only one decision question at a time. Use the stable question ID from the collaborator packet. Use plain, mobile-friendly language and explain unfamiliar CRM terms briefly. Allow "unknown" or "not sure" as valid answers. Do not guess, fill gaps silently, or treat silence, a topic change, or ordinary agreement as checkpoint approval.

After each answer, briefly restate what you understood and label it as one of: Confirmed operational fact, Working assumption, Preference, Proposed requirement, or Explicit approval. Ask a short clarification only when it materially changes the requirement. Then continue to the next unanswered question.

Keep existing CRM configuration ahead of custom software. Preserve the approved Costco/Centah versus independent-job boundary, the next-action and due-date rule, and human review of customer communications. Do not create accounts, connect external services, use real customer data, select a final platform, or claim that a checkpoint is signed off.

When the collaborator stops or completes the queue, produce a Markdown handoff headed "P0-W03 Collaborator Handoff" containing: source checkpoint, participant, date, answered question IDs, confirmed facts, preferences, proposed mandatory requirements, unknowns, conflicts with approved sources, follow-up questions, and explicit approvals. Quote no sensitive information. End with: "Unapproved input for repository reconciliation; CP-003 remains the last signed-off checkpoint."
```

## Mobile chat launch prompt to copy

```text
Read the Project instructions and attached sources. Confirm that CP-003 is the last signed-off checkpoint and P0-W03 is the active work unit. This session is for Loryn's operational input only; it does not approve the P0-W03 scorecard or authorize any external account or data action.

Guide Loryn through the P0-W03 question queue in COLLABORATOR_PACKET.md. Ask one question at a time, starting with LQ-001. Keep each question short enough to answer comfortably on a phone. If she says "stop," "pause," or needs to leave, immediately produce the P0-W03 Collaborator Handoff for all answers collected so far.
```

## P0-W03 operational question queue

These questions gather input. They are not pre-approved requirements and do not assign platform scores.

### LQ-001 - Essential phone actions

While parked between appointments, which actions must be easy on the phone every day: find a customer or job, see today's work, add a new prospect, record a note, change a stage, set the next action and date, confirm an appointment, open directions, or something else?

### LQ-002 - Unacceptable mobile friction

Which everyday action would make you reject a CRM if it took too many screens, repeated typing, or more than about one minute?

### LQ-003 - Daily work list

What must the opening screen show so you can immediately tell what is due today, overdue, upcoming, or waiting on someone else?

### LQ-004 - Quick prospect capture

When you meet or hear about a possible future customer, what is the least information you realistically have time to enter before moving on?

### LQ-005 - Reminders and customer contact

Which reminders must the CRM create reliably, and which calls, texts, or emails must always remain manually reviewed and sent by you?

### LQ-006 - Costco/Centah clarity

What must the CRM show so you can instantly distinguish a Costco/Centah job from an independently sourced job and know the correct next step?

### LQ-007 - Appointment and quote follow-up

What information must be visible without searching when preparing for an appointment or following up on a quote?

### LQ-008 - Installation exceptions

How should an overdue or unconfirmed installation stand out, and what would make that warning hard to miss without becoming annoying?

### LQ-009 - Weak signal and device constraints

Where do you commonly have weak service, and which actions, if any, must still work or be safely captured for later when the connection is poor?

### LQ-010 - Learning and maintenance burden

What level of setup, training, repeated data entry, or ongoing cleanup would make a CRM unrealistic for daily use?

### LQ-011 - Access and visibility

Besides you, who may need access now or later, and what should each person be able to see or change?

### LQ-012 - Final must-have check

What requirement would make you say "do not choose this CRM" even if the rest of the platform looked good?

## Repository reconciliation checklist

When the handoff returns to the repository owner or local Codex task:

1. Verify the handoff identifies CP-003 and P0-W03.
2. Separate confirmed facts, preferences, proposed requirements, unknowns, and approvals.
3. Check every proposal against the signed artifacts and master plan.
4. Resolve contradictions before drafting a scorecard requirement.
5. Keep all P0-W03 material labeled `Unapproved` until its checkpoint is explicitly signed off.
6. Update the appropriate Markdown and control files only after review.
7. Run structural, privacy, content, and Git-diff checks before committing and pushing.

## Version note

This packet is an onboarding and input-capture aid. It does not replace `CURRENT_STATE.md`, the signed session log, the approved artifacts, or the master decision log.
