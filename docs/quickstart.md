# Start with one task and two agent roles

Use a coordinator and a worker to document one harmless task. A good first task is reviewing a local sample document for broken internal links. Use synthetic material and avoid production accounts during the first rehearsal.

## 1. Choose the systems of record

Create or select a private operations repository for instructions, procedures, decisions, and run records. Name the existing task tracker and the business systems that own leads, sales, advertising, and analytics. Record links in private configuration without copying credentials into documentation.

Create a separate public repository for the handbook and sanitized templates if you intend to share the process. Review the files before their first publication.

## 2. Set the instructions

Copy [templates/AGENTS.md](../templates/AGENTS.md) into your private repository. Replace each bracketed item. Define:

- Who owns the outcome and who can approve consequential changes.
- Which folders, accounts, and task types an agent can change.
- What evidence must exist before a task can be completed.
- Where unfinished work and exceptions are recorded.

Permission from a task owner must be consistent with the platform's access controls. A document cannot give an agent access it does not have.

## 3. Give each role an owner

Create role cards from [templates/role.md](../templates/role.md). Begin with a coordinator and one worker. List the exact procedure each role follows and the fallback when a tool fails.

Assign each task a single active owner. Delegate separate files or responsibilities when agents work in parallel. Read current work before editing shared files. Do not overwrite another agent's changes or sweep unrelated files into a commit.

## 4. Make the task checkable

Write the requested outcome, allowed scope, source material, and acceptance check before execution.

Example:

> Review the sample guide in the assigned folder. List broken relative links with their source location. Do not edit the guide. The reviewer will check every reported link against the local files. Save the report and a handoff.

This tests assignment, evidence collection, and handoff without a live publication or real customer interaction.

## 5. Record the run

Adapt [templates/run-event.json](../templates/run-event.json). Emit a `start` event before work, a `checkpoint` when scope, evidence, or ownership changes materially, and a `finish` when the run stops. Keep the same `run_id` across its events and write timestamps in UTC.

Use `partial` for every nonfinish event. A finish event uses `ok`, `partial`, or `failed`, supported by its verification record. Missing access or missing evidence must remain visible.

The event fields have these meanings:

| Field | Meaning |
| --- | --- |
| `schema_version` | Integer version of the event contract, `2` in this example. |
| `event` | `start`, `checkpoint`, or `finish`. |
| `run_id` | Stable identifier shared by all events in a run. |
| `ts` | Event timestamp in UTC. |
| `agent` | Registered role or agent performing the work. |
| `model` | Actual caller-supplied model ID. Do not infer it from the platform name. |
| `human` | Human owner. The example uses `account-owner`; adapt it to your private contract's accepted values. |
| `client` | Private account scope or a synthetic example label. |
| `task` | Requested work. |
| `output` | Concrete artifact or current progress. |
| `impact` | Intended commercial purpose or measured outcome, distinguished explicitly. |
| `status` | `partial` before finish; `ok`, `partial`, or `failed` at finish. |
| `task_refs` | References to tasks in their source system. |
| `evidence_refs` | References to retained evidence, including verification method, time, and result. |
| `handoff` | Location of the continuation record. |
| `blockers` | Explicit missing prerequisites or exceptions. |
| `next_action` | Next concrete action or `none` after verified completion. |
| `verification` | `not_run`, `passed`, `failed`, or `partial`. |
| `changes_applied` | List of strings describing actual changes. Distinguish external effects from preparation. |

A finish event can use `ok` only when its acceptance check passed and the evidence is accessible to the reviewer. A completed analysis may have no live changes, but still needs evidence of the analysis and its check. Store verification details with the referenced evidence; the enum alone cannot establish success.

Save one JSON object per line in a private monthly JSONL ledger, or use another append-only format that your tooling validates. Avoid concurrent writes to the same file without locking or a designated writer. Make retries idempotent using the run ID, event type, and timestamp or another stable event identity.

## 6. Verify and hand off

The reviewer checks the produced artifact and the stated acceptance check. For changes to a live system, check the live destination using the procedure approved for that system. A draft saved locally is verified as a draft, not as a live change.

Write [templates/handoff.md](../templates/handoff.md) with what changed, what remains, evidence links, and the next action. Commit only the relevant files. Include the actual agent, model, human owner, and commercial purpose in the work record.

## 7. Test continuation from a fresh session

Give another agent the repository entry point, role card, task, and handoff. Omit the original conversation. Ask it to explain the state, permissions, evidence, and next action. Have it perform the next permitted step.

If it must guess, repair the missing instruction or evidence link and repeat the same test. Save the test result. Do not claim improved reliability from a rewritten instruction alone.

The included [worked synthetic rehearsal](../examples/synthetic-rehearsal/README.md) shows the task, local input, link-check evidence, finished worker handoff, and the next review action. It contains one deliberately broken link so another agent can reproduce the finding. It tests document continuation, not a live account takeover.

## 8. Add weekly review

Assign one coordinator to review the prior seven days. It reports completed outcomes, evidence gaps, failed or partial runs, business measurements, and the next three priorities. It proposes one bounded process improvement with a success check.

Configure scheduling in your chosen platform and verify the first real run and delivery. This handbook itself creates no schedule. Keep email, client messages, publication, and spending subject to the authority you explicitly granted.
