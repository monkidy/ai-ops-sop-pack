# Agent Handoff Template

Use this template when transferring bounded work from one operator or agent to another.

Do not use this template to imply approval, merge readiness, live runtime permission, or permission-to-act.

## Handoff Metadata

- BRANCH:
- BASE_COMMIT:
- CURRENT_COMMIT_OR_UNCOMMITTED_STATE:
- INITIAL_STATUS:
- FINAL_STATUS:

## File Changes

- FILES_CREATED:
- FILES_MODIFIED:
- FILES_DELETED:

## Commands And Evidence

- COMMANDS_RUN:
- PASS_FAIL_BY_COMMAND:
- RAW_ERROR_IF_FAIL:
- DIFF_STAT:

## Boundary Check

Confirm explicitly:

- no live runtime opened:
- no provider call made:
- no secrets used:
- no daemon / watcher / background process started:
- no memory write:
- no ledger write:
- no permission-to-act claimed:
- no trading / order routing / leverage / portfolio authority opened:

## Risk Flags

List all unresolved risks, missing evidence, failed checks, uncertain state, or required review.

- RISK_FLAGS:

## Decision Proposed

Choose exactly one:

- REMOTE_COMMIT_READY
- PARTIAL_NEEDS_REPAIR
- STOP_RISK

Selected value:

- DECISION_PROPOSED:

## Decision Rationale

Explain why the selected decision is supported by observed evidence.

- EVIDENCE_SUPPORTING_DECISION:
- EVIDENCE_MISSING_OR_WEAK:

## Next Recommended Action

Use a bounded next action. Do not open a new scope implicitly.

- NEXT_RECOMMENDED_ACTION:

## Notes

Memory, intention, and confidence are not proof. Only observed repository state, command output, CI status, or explicit human review can support stronger status claims.
