# OOM Recovery Checklist Template

Use this checklist after an out-of-memory crash, editor crash, or local workstation interruption during a PR / merge gate.

The goal is human-led cold recovery with minimal context reload and no uncontrolled action.

## Incident Metadata

- Repository:
- Branch before crash, if known:
- PR number, if applicable:
- Operator:
- Date / time:
- Crash context:

## Immediate Post-Crash Rules

Confirm before continuing:

- long context was not relaunched automatically:
- no live runtime was started:
- no provider call was made:
- no daemon / watcher / background process was started:
- no secrets were exposed:
- no destructive command was run:

## GitHub / PR State Check

Record observed state only.

- PR exists:
- PR state:
- PR merged:
- PR head commit:
- PR base branch:
- merge commit, if already merged:

## Local Git State Check

Run short, bounded checks only.

- current branch:
- local HEAD:
- worktree status:
- remote fetched:
- local branch aligned with remote:

## Observable Context Realignment

Confirm only with observable evidence. Do not infer hidden agent memory alignment.

- resumed workspace matches pre-crash evidence:
- resumed PR state matches pre-crash evidence:
- resumed branch and HEAD match pre-crash evidence:
- resumed notes / handoff context match pre-crash evidence:
- uncertainty or missing evidence recorded:

## Recovery Action

Choose the smallest safe action:

- no action required:
- fast-forward main only:
- repair local state:
- stop and escalate:

Commands used:

```text

```

## Validation

- local state clean or explicitly accounted for:
- expected branch active:
- expected commit observed:
- required non-live checks passed:
- no live / provider / runtime action occurred:

## Decision

Choose exactly one:

- PASS
- REPAIR_REQUIRED
- STOP_RISK

Selected value:

- DECISION:

## Stop Conditions

Stop if:

- GitHub / PR state cannot be verified
- local repository state diverges unexpectedly
- worktree contains unexplained changes
- resumed workspace / PR / branch / HEAD / notes cannot be matched to pre-crash evidence
- a live runtime, provider, secret, daemon, watcher, wallet, trading, or order-routing request appears
- the recovery would require destructive action without explicit review

## Final Handoff

- final observed state:
- unresolved risks:
- next recommended action:
