# Worked synthetic rehearsal

This is a local document exercise with synthetic content. It demonstrates a checkable task and a handoff. It does not connect to a production account, publish anything, or establish live operational adoption.

## Task

Review `sample-guide.md` for broken relative links. Do not edit it. Save the finding, check both link targets against the local files, and hand the result to a reviewer.

## Included state

- [Sample guide](sample-guide.md): the input, containing one intentionally broken relative link.
- [Existing appendix](existing-appendix.md): the link target that exists.
- [Evidence](evidence.md): observed local targets and acceptance check.
- [Handoff](handoff.md): the completed worker result and next review action.

## Reproduce the check

1. Read the two Markdown links in `sample-guide.md`.
2. Resolve each link relative to this directory.
3. Confirm `existing-appendix.md` exists and `missing-appendix.md` does not.
4. Compare the observed pair with `evidence.md`.
5. Open `handoff.md` and state the next action and its limit.

The missing target is intentional. Package-wide link checks must report it as an expected example finding, not repair it silently or treat it as an accidental handbook defect.

## Acceptance

The worker report correctly identifies the one missing target. A fresh reviewer can reproduce the check and identify the next permitted action from the handoff. Record that independent review separately. A local rehearsal does not prove that account access, application writes, or scheduled delivery work.
