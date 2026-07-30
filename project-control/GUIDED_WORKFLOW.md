# Guided Project Workflow

**Purpose:** Execute the Window Sales Operations plan through small, interactive, verifiable steps while preserving a reliable restart point between sessions.

## Control hierarchy

1. `../deliverables/window-sales-operations-master-plan.md` - product scope, roadmap, architecture, risks, and decision log.
2. `CURRENT_STATE.md` - current execution position and the first file to read when resuming.
3. `SESSION_LOG.md` - append-only history of work, validation, sign-offs, and handoffs.
4. `ARTIFACT_REGISTER.md` - authoritative artifacts and synchronization status.

If the files conflict, stop new work, identify the latest explicit user sign-off, and reconcile the files before continuing.

## Session opening

At the beginning of each session:

1. Read `CURRENT_STATE.md`.
2. Read the latest signed-off checkpoint in `SESSION_LOG.md`.
3. Read the relevant master-plan phase, decision entries, and linked artifacts.
4. Check for contradictions, stale status, or unsynchronized material changes.
5. Tell the user:
   - current phase and work unit;
   - last signed-off checkpoint;
   - open blockers or decisions;
   - the proposed outcome for this session.

## Chat organization

- Keep one pinned project chat for the active guided work unit and its checkpoint review.
- Continue in that chat while refining the same outcome.
- Start a new project chat for a materially different outcome, such as platform evaluation, Centah research, CRM configuration, implementation, security review, or release preparation.
- Use `CURRENT_STATE.md`, the latest signed `SESSION_LOG.md` entry, and linked approved artifacts as the handoff packet; no chat transcript is authoritative.
- Do not let two chats edit the same durable artifact concurrently. Independent research or isolated implementation may use separate chats and must reconcile results into the guided chat before sign-off.
- Pin the active guided chat. Archive completed outcome chats after their accepted results are incorporated into the durable files.

## Work-unit contract

Each work unit must define:

- **ID:** stable identifier such as `P0-W01`.
- **Outcome:** one observable result.
- **Inputs:** information or access required.
- **In scope / out of scope:** explicit boundaries.
- **Acceptance checks:** evidence needed to call the unit complete.
- **Approval effect:** what the next step is allowed to rely on.

Work through the unit interactively. Ask only for information needed for the current decision, allow `unknown` as an answer, and record unknowns without guessing. Separate confirmed facts, working assumptions, proposals, and accepted decisions.

## Review and sign-off

Before asking for sign-off, provide a checkpoint packet containing:

- checkpoint ID and title;
- result being approved;
- validation performed and evidence produced;
- decisions made or superseded;
- unresolved questions, risks, and deferred work;
- files that will be synchronized;
- next work unit unlocked by approval.

The checkpoint remains **Awaiting sign-off** until the user explicitly accepts it. Natural wording is sufficient, but the clearest form is `Sign off <checkpoint ID>`.

There are two checkpoint levels:

- **Work-unit checkpoint:** approves a bounded artifact, rule set, configuration, or discovery result.
- **Phase-gate checkpoint:** confirms the phase gate in the master roadmap has been met or accepts a documented exception.

## Session close and durable handoff

At sign-off, or when the user asks to stop without signing off:

1. Reconcile all facts, decisions, statuses, and open questions changed during the session.
2. Update the master Markdown plan when scope, architecture, roadmap, risk, or a material decision changed.
3. Mark the Word distribution copy stale when the master Markdown changes. Regenerate and visually verify Word only at a final release or explicit sharing milestone.
4. Update `CURRENT_STATE.md` with the exact restart point.
5. Append an entry to `SESSION_LOG.md`; never rewrite a signed-off entry.
6. Update `ARTIFACT_REGISTER.md` for added, superseded, or stale artifacts.
7. Run appropriate structural, privacy, and content checks.
8. When the repository backup is available, synchronize the approved Markdown/control artifacts, review the Git diff for sensitive data, and commit and push the checkpoint unless the user requests a local-only pause.
9. Give the user a compact closing summary and the next-session starting point.

If a session ends without sign-off, preserve drafts but label them **Unapproved**. The next session resumes at review or revision, not at the downstream step.

## Synchronization checklist

- [ ] Current phase and work-unit status agree across durable files.
- [ ] The decision log contains every material accepted, rejected, or superseded choice.
- [ ] Assumptions and unknowns are not presented as confirmed facts.
- [ ] Completed items are not still marked pending.
- [ ] The authoritative Markdown and project-control files agree on material content.
- [ ] The Word distribution copy is labeled current or stale; if this is a release/sharing milestone, it has been regenerated and visually verified.
- [ ] The artifact register identifies the current authoritative version.
- [ ] The session log includes validation, sign-off status, and files changed.
- [ ] `CURRENT_STATE.md` contains one precise next action.
- [ ] No live customer data, credentials, or restricted documents were copied without approval.
- [ ] The repository backup either contains the saved checkpoint or is explicitly marked pending.

## Permission boundary

Project checkpoint approval authorizes progression within the documented plan. It does not by itself authorize production data access, creation of company-owned accounts, paid subscriptions, customer communications, Centah/Costco integration access, deployment, or destructive operations. Obtain those approvals separately when reached.
