# Roles and handoffs

A role card tells an agent which work it owns, how to run it, and where the next agent should start. Keep the card near the procedure and update both when a tested change is accepted.

## Coordination roles

| Role | Owns | Produces | Completion check |
| --- | --- | --- | --- |
| Human owner | Outcomes, priorities, and authority | Scope and decisions | Requested business outcome and limits are explicit. |
| Coordinator | Routing, dependencies, and the weekly review | Assigned tasks, evidence links, and priorities | Every active task has an owner, acceptance check, and continuation point. |
| Worker | One assigned task within a stated scope | Changes, artifacts, and run events | The artifact exists and the acceptance check has been performed. |
| Reviewer | Evidence and acceptance checks | Findings, pass or fail, and remaining limits | It examines the result independently and states what was actually checked. |

Assign the coordinator to a platform that can reach the records and run on the required schedule. Choose from measured access and delivery, then record the fallback. An intended architecture is not proof that the chosen runtime is available.

## Marketing job families

| Job family | Main work | Useful evidence | Business connection |
| --- | --- | --- | --- |
| SEO and content | Search intent, page quality, technical fixes, and useful content | Before and after page observations, search data, and approved artifacts | Qualified organic inquiries and sales linked through the CRM |
| AI visibility | Controlled buyer-question samples and source analysis | Exact prompts, provider conditions, answers, cited URLs, and collection status | Observed discovery and qualified inquiries, with attribution limits stated |
| Local search | Business information, local pages, reviews, and map visibility | Matched listing, scan conditions, and source observations | Calls, appointments, or jobs that can be verified |
| Paid media | Campaign analysis and authorized campaign changes | Authenticated account measurements, change history, and conversion checks | Cost per qualified lead, acquisition cost, and sales |
| Sales operations | Qualification rules and authorized follow-up workflows | CRM events, delivery checks, dispositions, and approved message versions | Qualified opportunities, booked meetings, and collected revenue |

Paid media and automated sales workflows should remain marked `pilot` until their permissions, execution, and outcome checks have passed in the environment where they will run.

## Minimum role card

Every card includes its owner, backup, trigger, input records, required tools, exact permitted scope, procedure, outputs, acceptance check, and escalation path. State current capability as one of:

- `documented`: a procedure exists, execution has not been verified here.
- `pilot`: execution is being tested within a stated limit.
- `verified`: a dated test and evidence establish the specific capability.
- `unavailable`: a required prerequisite currently prevents execution.

`verified` describes a named capability under recorded conditions. It does not establish permanent access or general autonomy.

## Handoff contract

The handoff points to the latest accepted state, pending changes, evidence, blockers, and the next action. It names the next owner and the authority that action requires. Keep observations separate from interpretations and recommendations.

For example, a failed analytics request is a collection failure. It cannot support a conclusion that traffic or leads were zero. A saved campaign draft is a draft. It cannot support a claim that advertising is running.

Do not place credentials, personal information, customer records, or private evidence in a public handoff. A public worked example uses synthetic data and labels it clearly.

## Continue an interrupted run

Read the latest handoff and events, inspect the destination, and reconcile recorded external effects before retrying. Confirm the original runner has stopped before taking over side effects. A record of ownership in Git is advisory and does not provide an atomic lock.

Use a new run ID for the replacement execution and preserve the logical task reference. Link the earlier run in the handoff or an optional `resumes_run_id` field. For the same external action, reuse the effect receipt or idempotency key. A missing finish event does not prove that a post, lead, campaign, or other write never happened.

## When agents disagree

Record the disputed claim and the evidence each reviewer used. Resolve the decision with a source check or a defined experiment. The coordinator records the accepted decision and any remaining uncertainty. Escalate material business decisions to the human owner when the granted authority does not cover them.

Count agreement only from agents that participated in the review. Do not attribute a vote or approval to another runtime merely because its instructions were read.
