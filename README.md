# Leedly Agent Operations Handbook

By Clayton Turner, founder of [Leedly](https://leedly.com/). Updated October 17, 2026.

I want another authorized agent to be able to open the record, understand the job, and continue the work. That takes a named owner, clear limits, and evidence of what happened.

This handbook shares how I document roles, assign work, hand it off, verify outcomes, and improve the process from experience at Leedly. My commercial scoreboard starts with qualified leads and sales. Search rankings, AI mentions, traffic, and advertising results help explain what contributed to those outcomes.

## Start here

1. Follow the [quickstart](docs/quickstart.md) with one harmless task.
2. Define your [roles and handoffs](docs/roles-and-handoffs.md).
3. Adopt the [measurement and improvement loop](docs/measurement-and-improvement.md).
4. Adapt the [agent instructions](templates/AGENTS.md), [role card](templates/role.md), [handoff](templates/handoff.md), and [run event](templates/run-event.json).
5. Reproduce the [worked synthetic rehearsal](examples/synthetic-rehearsal/README.md) before applying the pattern to a live account.

Use your own tools, accounts, permissions, and approval rules. These files do not install an agent, connect an account, schedule work, or grant access.

## What this package represents

| Area | Status | Meaning |
| --- | --- | --- |
| Shared instructions, role routing, work records, evidence, and human review | Documented operating practice | The handbook distills an existing agency workflow into portable instructions. It does not certify that every agent follows it on every run. |
| Public role, handoff, and event templates | Starter templates | Adapt and test them before using them with live accounts. |
| Automated sales follow-up and paid media agents | Pilot | Their presence in the operating model is not proof of an unattended production service or verified commercial results. |
| Every tool connection, scheduled run, and transfer between agent platforms | Unverified in your environment | Test each connection and a complete handoff. A configured account or scheduler entry does not establish successful execution. |

Marketing job families such as SEO, content, AI visibility, local search, sales, and paid media describe the work. A coordinator, worker, and reviewer describe how that work is assigned and checked. One agent may perform several roles when the ownership and checks remain explicit.

## The shared record

Keep reusable instructions and versioned work in GitHub. Keep live customer records in the system that owns them. Link those records from the private work ledger when access permits.

```text
Your private operations repository
  AGENTS.md                 entry instructions and limits
  roles/                    role cards with owners and fallback paths
  procedures/               repeatable steps and verification
  handoffs/                 current continuation points
  runlog/                   dated start, checkpoint, and finish events
  decisions/                accepted changes and their evidence
  reports/                  weekly findings and next actions

Your public handbook repository
  docs/                     reusable, reviewed instructions
  templates/                generic examples others can adapt
```

Keep private operational evidence out of the public repository. Publish a separate, reviewed explanation or synthetic example. Publishing a repository does not make private links accessible to its readers.

## The execution loop

1. The human owner defines the outcome, limits, and publication or spending authority.
2. The coordinator selects a role and records the task, acceptance check, and dependencies.
3. The worker records a start event, performs the authorized work, and saves evidence.
4. The reviewer checks the result against the acceptance check and destination.
5. The worker writes a finish event or a handoff with blockers and the next action.
6. The weekly coordinator proposes a specific process improvement from the evidence.
7. A separate run tests the improvement before it becomes the default procedure.

Agreement between agents is a review outcome. It does not prove a deployment, ranking change, or sale.

## Make the public process useful to humans and agents

Give each procedure a plain title, a direct answer, prerequisites, numbered steps, a worked example, a verification method, and a recovery path. Link related procedures. Record the version and meaningful update date.

Use a website guide for the human explanation and GitHub for reusable templates and change history. Keep one maintained source for each procedure and identify that source in any published rendering.

Google says its existing SEO practices apply to AI Overviews and AI Mode. Important content should be readable as text, accessible to crawling, and linked from relevant pages. No special AI file or schema is required. Inclusion remains uncertain. [Google Search Central](https://developers.google.com/search/docs/appearance/ai-features)

The optional [llms.txt](llms.txt) in this package is a navigation aid for readers and agents. It carries no claim about rankings or AI citations.

## Definition of a successful handoff

A second agent can open the role card and latest handoff, identify the owner and permissions, locate the evidence, and state the next action without needing the original conversation. It can then complete a permitted test or explain the exact missing prerequisite.

Do that test before describing the process as portable. Repeat it when tools, permissions, or procedures change.

## Work with Leedly

Want help adapting this process to your marketing team? [Request an agent implementation review](https://leedly.com/contact-us/). To see the marketing work these roles support, read [Leedly's marketing agents guide](https://leedly.com/ai-marketing-agents/).
