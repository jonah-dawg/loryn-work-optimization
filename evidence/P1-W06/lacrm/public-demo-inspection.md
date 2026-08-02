# P1-W06 Less Annoying CRM Public-Demo Inspection

**Status:** Signed evidence set at CP-009; M-01 failed; Less Annoying CRM eliminated; P1-W06 closed

**Inspected:** August 1, 2026

## Authorization and boundary

- **Accepted (D-112):** Authorize the bounded P1-W06 LACRM public-demo inspection under the approved execution contract.
- Access began from the official product-tour link to the no-signup live demo.
- The evaluator selected only `Generic` and `2-5` users to launch a temporary vendor demo account.
- No name, private email, phone, address, credential, code, billing information, account, trial, external connection, real record, or customer communication was supplied.
- The inspection was read-only. Dialogs were opened to observe controls, but no record, task, field, filter, view, widget setting, or configuration was saved.

## Direct observations

### Temporary demo boundary

- The application labeled the session as a temporary demo account and kept free-trial signup as a separate link.
- Profile editing was unavailable without starting a real trial.
- The demo exposed vendor-generated sample data. No sample names, contact details, internal identifiers, or session values are retained in this evidence file.

### Workspace and M-01

- Workspace displayed a due-task widget, pipeline-report widget, activity report, and calendar preview on one screen.
- The task widget settings allowed calendar scope and task windows such as due today, future ranges, or overdue. It did not expose pipeline-item scope.
- The pipeline widget settings allowed user scope and selection of all or specific pipelines.
- The pipeline widget rendered status totals. Its settings did not offer a saved filtered record view or an actionable record list for `waiting on someone else` and missing-next-action jobs.
- The activity report is chronological activity, not the required action queue.

### Task and pipeline relationship

- A sample Task edit dialog exposed Task name, calendar, due date, assignee, `Attached contact`, and description.
- No pipeline-item relationship was exposed in the Task dialog.
- The related Contact page displayed the upcoming Task and the active Lead as separate attached-item sections.
- This directly supports the official API evidence that Tasks are Contact-scoped and does not establish a distinct Task relationship for each job pipeline item.

### Pipeline and field controls

- The CRM customization screen supported primary Contact/Company records and multiple pipelines.
- Pipeline settings exposed active and closed statuses plus custom fields.
- The custom-field dialog exposed text, text-area, number, currency, date, dropdown, radio, checkbox-list, contact-link, and file field types.
- It exposed a global `Make this field required` checkbox and display options for the pipeline report and pipeline badges.
- No conditional-requirement control or unique-value control was visible in the inspected custom-field dialog. Their availability outside this dialog remains unverified rather than inferred.
- The pipeline report exposed board/list modes, display, filter, sort, export/print, and saved-view controls. The filter menu included pipeline/contact fields and a Contact-scoped Tasks-and-events option.

## Mandatory-gate result

| Gate | Direct state | Evidence |
|---|---|---|
| M-01 Reliable daily action center | `Fail` | Workspace cannot show all five required categories as actionable records. It can show due/overdue Tasks, calendar items, activity, and pipeline/status totals, but not record-level waiting jobs and active jobs missing their own next action in that same practical view. |
| M-02 through M-13 | `Unverified` | The M-01 stopping rule ended the run before broader testing. Observed controls may inform later comparison but do not create additional pass/fail results. |

## Stopping result

The approved stopping rule fired on M-01. P1-W06 therefore stops before account authorization, a real trial, tenant configuration, synthetic fixture creation, broader scenario testing, scoring, or Loryn participation.

**Approved result at CP-009:** `Eliminated`.

CP-009 approves this sanitized evidence, the direct M-01 failure, the `Eliminated` result, and closure of P1-W06. It does not select another CRM or authorize any next candidate.

## Cleanup and remaining state

- No persistent demo changes were saved.
- The temporary demo browser tab was closed after inspection.
- No account, trial, tenant, configuration, export, download, screenshot artifact, connection, billing action, communication, or production action remains.

## Official entry point

- [LACRM product tour and live-demo link](https://www.lessannoyingcrm.com/tour)

## CP-009 approval boundary

- CP-009 approves the P1-W06 evidence and result only.
- It does not authorize an LACRM account or trial, a next CRM candidate, billing, production use, real data, an external connection, customer communication, a Loryn session, or platform selection.
- Less Annoying CRM can be reconsidered only through a later explicitly approved reopening that identifies material new evidence relevant to M-01.
