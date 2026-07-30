# Artifact Register

**Updated:** July 29, 2026

| Artifact | Authority | Current status | Update trigger |
|---|---|---|---|
| `../deliverables/window-sales-operations-master-plan.md` | Authoritative product and delivery plan | Version 1.17; current | Material scope, architecture, roadmap, risk, governance, process, or decision change |
| `../deliverables/window-sales-operations-master-plan.docx` | Non-authoritative editable distribution copy | Version 1.4; stale by design until final release or explicit sharing milestone | Regenerate and visually verify only for a release or requested sharing copy |
| `GUIDED_WORKFLOW.md` | Authoritative session and checkpoint procedure | Current | Workflow-control rule changes |
| `CURRENT_STATE.md` | Authoritative restart point | P0-W02 in progress; Decisions 1 through 10 approved and Decision 11 next after CP-002 | Every sign-off, session stop, blocker, or active-work-unit change |
| `SESSION_LOG.md` | Append-only execution history | S-015 records Decision 10 and the one-week quote follow-up; CP-002 remains the last completed work-unit checkpoint | Every sign-off or session close |
| `ARTIFACT_REGISTER.md` | Artifact authority and synchronization inventory | Current | Artifact added, renamed, superseded, or found stale |
| `../deliverables/P0-W01-current-workflow-and-permission-boundary.md` | Signed P0-W01 workflow and permission boundary | Approved at CP-001 | Supersede only through a later signed checkpoint |
| `../deliverables/P0-CR01-independent-leads-and-prospecting-scope.md` | Signed scope-change record | Approved at CP-002 | Supersede only through a later signed checkpoint |
| `REPOSITORY_BACKUP.md` | Repository location, synchronization boundary, and recovery instructions | Current | Repository, branch, tracked scope, or working-copy policy changes |

## Planned artifacts not yet created

| Artifact | Planned phase | Purpose |
|---|---|---|
| Lead-to-install workflow map | Phase 0 | Document the current Costco/Centah workflow and failure points |
| Source-of-truth matrix | Phase 0 | Define the authoritative system and allowed edits for each field group |
| CRM platform scorecard | Phase 0-1 | Compare Zoho, HubSpot, and Centah-only baseline using weighted evidence |
| CRM field dictionary | Phase 1 | Define fields, types, requirements, source systems, and mappings |
| Centah integration discovery record | Phase 0-3 | Record confirmed interfaces, access, contracts, limits, and support model |

## Synchronization rule

The Markdown master is authoritative. Material Markdown changes make the Word distribution copy stale, but do not require an immediate rebuild. At a final release or explicit sharing milestone, regenerate Word from the current Markdown, render and inspect every page, run structural checks, and then mark that specific Word version current.

The GitHub repository is the durable backup for Markdown and project-control artifacts. Until its local checkout is attached or opened as the primary Codex project, reconcile the app-managed working copy into the repository at each saved checkpoint and never copy real customer data, credentials, synchronized project sources, or temporary rendering files.
