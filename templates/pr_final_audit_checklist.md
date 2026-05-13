# PR Final Audit Checklist Template

Use this checklist before marking a pull request as ready for merge or before performing a bounded merge procedure.

Completing this checklist records review evidence only. It does not approve or perform a merge, and it does not grant merge authority by itself.

## PR Metadata

- Repository:
- PR number:
- PR title:
- Base branch:
- Head branch:
- Expected head commit:
- Reviewer / operator:
- Date:

## Precheck

Confirm before continuing:

- local branch is correct:
- local worktree is clean or explicitly accounted for:
- base branch is current:
- PR state has been checked on GitHub:
- expected head commit is known:
- no unreviewed local changes are included:

## Evidence Reviewed

- diff reviewed:
- changed files reviewed:
- tests / checks reviewed:
- CI status reviewed:
- local validation reviewed, if applicable:
- documentation impact reviewed:
- rollback or repair path understood:

## Head Guard

- observed PR head commit:
- expected PR head commit:
- match confirmed:
- merge command or action will preserve head guard:

Stop if the PR head changed and the new head has not been reviewed.

## Boundary Review

Confirm explicitly:

- no live runtime opened:
- no provider call introduced:
- no secrets introduced:
- no daemon / watcher / background process introduced:
- no memory write introduced:
- no ledger write introduced:
- no permission-to-act introduced:
- no trading / order routing / leverage / portfolio authority introduced:

## Decision

Choose exactly one:

- PASS
- REPAIR_REQUIRED
- STOP_RISK

Selected value:

- DECISION:

## Required Follow-Up

- follow-up action:
- owner:
- evidence required before stronger status:

## Final Statement

Write one sentence that separates evidence from approval.

- FINAL_STATEMENT:
