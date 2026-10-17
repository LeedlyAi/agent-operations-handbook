# Synthetic link review evidence

Task: review `sample-guide.md` without editing it.

Method: read the two relative Markdown link targets and check each target's existence in this directory. This is a local filesystem observation, not a website or indexing check.

| Source | Target | Observation |
| --- | --- | --- |
| `sample-guide.md` | `existing-appendix.md` | File exists. |
| `sample-guide.md` | `missing-appendix.md` | File is absent. This is the intentional broken link. |

Worker acceptance check: the report identifies exactly the absent target and preserves the input. The exercise is ready for independent reproduction from the handoff. Independent review status must be recorded by the reviewer rather than inferred from this document.

Commercial impact: none measured. The intended benefit is a handoff another agent can understand and verify without its original conversation.
