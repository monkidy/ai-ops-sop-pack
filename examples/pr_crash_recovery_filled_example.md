# Filled Example — PR Crash Recovery And Handoff

This is a fictitious, non-live example showing how to use the SOP pack and templates together.

It is not based on a real incident. It does not imply runtime authority, provider access, trading permission, merge approval, or production readiness.

## Scenario

A local editor crashed during final review of a pull request. The operator needs to recover state, verify the pull request, avoid reloading long context, and hand off the result conservatively.

## Scope

- Repository: `example-org/example-agent-service`
- PR: `#42`
- Base branch: `main`
- Head branch: `docs/update-agent-handoff`
- Expected PR head: `abc1234`
- Operator: `operator-a`
- Date: `2026-05-12`

## Files Used From This Pack

- `content/01_oom_recovery_sop.md`
- `content/02_pr_final_audit_head_guard_sop.md`
- `content/04_agent_handoff_format.md`
- `templates/oom_recovery_checklist.md`
- `templates/pr_final_audit_checklist.md`
- `templates/agent_handoff_template.md`

## Step 1 — OOM / Crash Recovery

### Incident Metadata

- Repository: `example-org/example-agent-service`
- Branch before crash, if known: `docs/update-agent-handoff`
- PR number: `#42`
- Operator: `operator-a`
- Date / time: `2026-05-12 09:40 UTC`
- Crash context: editor OOM during PR final review

### Immediate Post-Crash Rules

- long context was not relaunched automatically: `yes`
- no live runtime was started: `yes`
- no provider call was made: `yes`
- no daemon / watcher / background process was started: `yes`
- no secrets were exposed: `yes`
- no destructive command was run: `yes`

### GitHub / PR State Check

Observed state only:

- PR exists: `yes`
- PR state: `open`
- PR merged: `no`
- PR head commit: `abc1234`
- PR base branch: `main`
- merge commit, if already merged: `not applicable`

Example commands:

```text
gh pr view 42 --json state,headRefOid,baseRefName,mergeStateStatus
```

### Local Git State Check

- current branch: `docs/update-agent-handoff`
- local HEAD: `abc1234`
- worktree status: `clean`
- remote fetched: `yes`
- local branch aligned with remote: `yes`

Example commands:

```text
git branch --show-current
git rev-parse HEAD
git status -sb
git fetch origin
```

### Recovery Decision

- DECISION: `PASS`

Rationale:

- GitHub PR exists and is open.
- Local branch and PR head match expected commit `abc1234`.
- Worktree is clean.
- No live/runtime/provider/secrets boundary was crossed.

## Step 2 — PR Final Audit

### PR Metadata

- Repository: `example-org/example-agent-service`
- PR number: `#42`
- PR title: `docs: update agent handoff guidance`
- Base branch: `main`
- Head branch: `docs/update-agent-handoff`
- Expected head commit: `abc1234`
- Reviewer / operator: `operator-a`
- Date: `2026-05-12`

### Precheck

- local branch is correct: `yes`
- local worktree is clean or explicitly accounted for: `yes`
- base branch is current: `yes`
- PR state has been checked on GitHub: `yes`
- expected head commit is known: `yes`
- no unreviewed local changes are included: `yes`

### Evidence Reviewed

- diff reviewed: `yes`
- changed files reviewed: `yes`
- tests / checks reviewed: `not applicable; documentation-only PR`
- CI status reviewed: `yes; neutral / no required CI for docs-only path`
- local validation reviewed, if applicable: `markdown links inspected locally`
- documentation impact reviewed: `yes`
- rollback or repair path understood: `yes; revert documentation commit if needed`

### Head Guard

- observed PR head commit: `abc1234`
- expected PR head commit: `abc1234`
- match confirmed: `yes`
- merge command or action will preserve head guard: `yes; use platform merge with observed head, or CLI equivalent with expected head check`

Stop condition was not triggered because the PR head did not move.

### Boundary Review

- no live runtime opened: `yes`
- no provider call introduced: `yes`
- no secrets introduced: `yes`
- no daemon / watcher / background process introduced: `yes`
- no memory write introduced: `yes`
- no ledger write introduced: `yes`
- no permission-to-act introduced: `yes`
- no trading / order routing / leverage / portfolio authority introduced: `yes`

### PR Audit Decision

- DECISION: `PASS`

Final statement:

> Observed evidence supports bounded documentation review readiness for PR #42 at head `abc1234`; this does not by itself grant merge authority or runtime authority.

## Step 3 — Agent / Operator Handoff

### Handoff Metadata

- BRANCH: `docs/update-agent-handoff`
- BASE_COMMIT: `main@def5678`
- CURRENT_COMMIT_OR_UNCOMMITTED_STATE: `abc1234`, worktree clean
- INITIAL_STATUS: `RECOVERY_AFTER_EDITOR_CRASH`
- FINAL_STATUS: `BOUNDED_REVIEW_READY`

### File Changes

- FILES_CREATED: `none`
- FILES_MODIFIED: `docs/agent_handoff.md`
- FILES_DELETED: `none`

### Commands And Evidence

- COMMANDS_RUN:
  - `gh pr view 42 --json state,headRefOid,baseRefName,mergeStateStatus`
  - `git branch --show-current`
  - `git rev-parse HEAD`
  - `git status -sb`
  - `git fetch origin`
- PASS_FAIL_BY_COMMAND: all required checks passed
- RAW_ERROR_IF_FAIL: none
- DIFF_STAT: documentation-only change, 1 file modified

### Boundary Check

- no live runtime opened: `confirmed`
- no provider call made: `confirmed`
- no secrets used: `confirmed`
- no daemon / watcher / background process started: `confirmed`
- no memory write: `confirmed`
- no ledger write: `confirmed`
- no permission-to-act claimed: `confirmed`
- no trading / order routing / leverage / portfolio authority opened: `confirmed`

### Risk Flags

- RISK_FLAGS:
  - CI not required for this docs-only PR in the example repository.
  - Human maintainer approval still required before merge.

### Decision Proposed

- DECISION_PROPOSED: `REMOTE_COMMIT_READY`

### Decision Rationale

- EVIDENCE_SUPPORTING_DECISION:
  - PR state observed.
  - PR head and local head match expected commit.
  - Worktree clean.
  - Scope is documentation-only.
  - Boundaries preserved.
- EVIDENCE_MISSING_OR_WEAK:
  - No human maintainer approval recorded in this example.
  - No production runtime validation relevant or performed.

### Next Recommended Action

- NEXT_RECOMMENDED_ACTION: maintainer review of PR #42 at head `abc1234`; merge only if maintainer approval and repository policy allow it.

## What This Example Does Not Prove

This example does not prove:

- production readiness
- runtime safety
- live agent readiness
- provider integration safety
- CI sufficiency for another repository
- permission-to-act
- merge approval
- trading safety
- order routing safety

## Reuse Notes

When adapting this example, replace every repository-specific field with observed evidence from your environment.

Do not copy the `PASS` or `REMOTE_COMMIT_READY` decisions unless your own evidence supports them.
