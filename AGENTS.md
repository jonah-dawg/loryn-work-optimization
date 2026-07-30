# Loryn Work Optimization

## Project objective

Design and implement a mobile-first CRM workflow for an independent window-covering sales consultant. Configure an existing CRM before authorizing custom application development.

## Required orientation

Before beginning work:

1. Read `project-control/CURRENT_STATE.md`.
2. Read the latest entry in `project-control/SESSION_LOG.md`.
3. Read the linked signed artifacts and relevant master-plan sections.
4. Report the current phase, active work unit, last approval, open blockers, and proposed outcome.

## Authority and sign-off

- `deliverables/window-sales-operations-master-plan.md` is the product source of truth.
- `project-control/CURRENT_STATE.md` is the restart source of truth.
- Signed session-log entries are immutable; record later corrections in a new entry.
- Do not treat discussion, silence, or a topic change as approval.
- Label unfinished designs `Unapproved` and do not build downstream work on them.

## Product rules

- Existing CRM configuration comes before a custom API, application, or website.
- Every active prospect or opportunity needs a next action and due date unless it has an explicit closed or exception state.
- Only Costco-originated opportunities use Centah or require a Centah lead number.
- A customer may have multiple opportunities; each opportunity represents one project or order.
- Keep customer-facing communications human-reviewed until a later approved automation gate.

## Privacy and security

- Never commit real customer or prospect data, credentials, tokens, cookies, production exports, or private integration payloads.
- Use synthetic examples in requirements, tests, screenshots, and fixtures.
- Do not log sensitive payloads.
- Do not connect production accounts or send customer communications without explicit authorization for that action.

## Artifact policy

- Update Markdown and project-control files at saved checkpoints.
- Generate and visually verify Word only at a final release or explicit sharing milestone.
- Do not commit `.docx-qa/`, temporary render files, or the ChatGPT Project `sources/` mirror.
- Review the complete Git diff for sensitive data before every push.

## Change discipline

- Preserve unrelated repository changes.
- Make focused changes tied to one work unit or checkpoint.
- Record material accepted, rejected, or superseded decisions in the master decision log.
- Run appropriate structural, privacy, content, and implementation checks before reporting completion.
