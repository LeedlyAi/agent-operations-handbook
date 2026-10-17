# Handoff: synthetic local link review

- Run ID: `synthetic-link-review-001`.
- Current owner: example worker.
- Next owner: example reviewer.
- Result: worker link review complete; independent review pending.
- Scope: read local example files, verify the report, and record review. No live account or publication authority.

## Requested outcome

Identify broken relative links in `sample-guide.md` and preserve the input.

## Current state and evidence

The guide contains two relative links. `existing-appendix.md` exists. `missing-appendix.md` is absent by design. The finding and method are in [evidence.md](evidence.md).

No input link was changed. No external action occurred. No business or discovery result is claimed.

## Next action

The reviewer reads `sample-guide.md`, checks both target files, and records whether the evidence identifies exactly the intended missing target. Preserve the broken link because it is the test fixture. If the observations differ, record the changed file or directory state before deciding what to do.

## Continue from a fresh session

Read this handoff, then `README.md`, `sample-guide.md`, and `evidence.md` in this directory. No original conversation is needed. Record the independent check and its limits in your own private run ledger or review artifact.
