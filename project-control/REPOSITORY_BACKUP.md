# Repository Backup and Recovery

**Remote:** `https://github.com/jonah-dawg/loryn-work-optimization.git`  
**Branch:** `main`  
**Local checkout:** `C:\Users\jonah\Documents\GitHub\loryn-work-optimization`

## Purpose

The repository provides durable version history and recovery for the authoritative Markdown deliverables and guided-workflow control files outside the app-managed ChatGPT Project directory.

## Included

- `deliverables/*.md`
- `project-control/*.md`
- repository `README.md`
- repository `AGENTS.md`
- repository `.gitignore`

## Excluded from routine checkpoints

- real customer or prospect data;
- credentials, access tokens, cookies, or private integration payloads;
- the ChatGPT Project `sources/` mirror;
- `.docx-qa/` and other rendering intermediates;
- the stale Word distribution copy; and
- personal exports or production CRM data.

The Word distribution copy may be added only when regenerated from the current Markdown for a final release or explicit sharing milestone.

## Checkpoint synchronization

1. Finish Markdown and project-control reconciliation in the active working copy.
2. Copy the included files into the local repository checkout.
3. Review all changed files and scan for credentials and customer identifiers.
4. Commit with the checkpoint or saved-session identifier.
5. Push `main` to the configured GitHub remote.
6. Confirm the local branch and remote branch reference the same commit.

## Recovery

Clone the remote repository, read `project-control/CURRENT_STATE.md`, then read the latest entry in `project-control/SESSION_LOG.md` and the linked approved artifacts. Chat transcripts and the Word distribution copy are not authoritative restart sources.
