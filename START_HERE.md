# START_HERE — AI Ops SOP Pack v0

This file is the external reading guide for AI Ops SOP Pack v0.

Use it before reading the individual SOP files.

## What this repository is

AI Ops SOP Pack v0 is a public documentation pack for bounded AI-agent operations.

It provides small, auditable operating procedures for:

- recovering from a workstation or editor crash during a PR / merge gate
- performing a final PR audit with strict head-guard discipline
- restarting a local operator workstation after a cold start
- handing work from one agent or operator to another without overclaiming readiness
- reviewing a local text-only operator path as a case study

The pack is published as Markdown documentation under CC BY 4.0.

## What this repository is not

This repository is not:

- a runtime
- an agent framework
- a trading system
- a provider integration
- a production certification
- a permission-to-act mechanism
- a permission-to-trade mechanism
- a sales asset
- a commercial offer
- a guarantee of correctness or safety in your environment

Do not treat any SOP as operational authority. Each procedure must be adapted, reviewed, and approved inside the reader's own environment.

## Intended reader

This pack is mainly for:

- AI Ops teams
- platform teams
- SRE / reliability teams
- engineering operators working with AI-assisted pull requests
- teams that need conservative handoff and review discipline around agents

The reader should already understand Git, pull requests, local validation, review gates, and operational boundaries.

## Recommended reading order

Read in this order:

1. `README.md` — repository status, license, scope, and non-goals.
2. `START_HERE.md` — this guide.
3. `content/04_agent_handoff_format.md` — most portable file; read first if you want a reusable handoff structure.
4. `content/02_pr_final_audit_head_guard_sop.md` — PR merge discipline and head-guard procedure.
5. `content/01_oom_recovery_sop.md` — cold recovery after crash during a PR / merge gate.
6. `content/03_cold_start_operator_runbook.md` — local workstation cold-start example; ASSO-derived and environment-specific.
7. `content/05_operator_guide.md` — local text-only avatar operator case study; strongly ASSO-derived and not generic.
8. `templates/` — blank copyable templates for handoff, PR audit, OOM recovery, and cold start.
9. `source_pr_references.md` — provenance mapping to source PRs.
10. `content/_INDEX.md` — consolidation audit index and historical release-work notes.

## Generic vs ASSO-derived files

### More portable

- `content/04_agent_handoff_format.md`
- `content/02_pr_final_audit_head_guard_sop.md`
- `content/01_oom_recovery_sop.md`
- `templates/agent_handoff_template.md`
- `templates/pr_final_audit_checklist.md`
- `templates/oom_recovery_checklist.md`
- `templates/cold_start_checklist.md`

These can be adapted by other teams with moderate rewriting.

### More environment-specific

- `content/03_cold_start_operator_runbook.md`
- `content/05_operator_guide.md`

These preserve ASSO-specific commands, paths, statuses, and local proof language. Treat them as case studies or internal-derived examples, not drop-in generic SOPs.

## How to adapt safely

When adapting a file, keep the conservative status discipline:

- distinguish observed evidence from inferred state
- keep source status separate from current distribution status
- keep local validation separate from CI validation
- keep readiness separate from approval
- keep documentation separate from runtime authority
- keep handoff separate from permission-to-act

Replace environment-specific commands, paths, URLs, branch names, checkers, and proof reports with equivalents from your own environment.

Do not remove stop conditions just to make a procedure look simpler.

Use the blank templates only after reading the related SOP. A template is a capture surface for observed evidence, not a substitute for review.

## Decision vocabulary

The pack intentionally uses conservative decision states.

Use `PASS` only when the required evidence is actually observed.

Use `REPAIR_REQUIRED` or `PARTIAL_NEEDS_REPAIR` when useful work exists but proof is incomplete.

Use `STOP_RISK` when required access, state, tooling, permission, or validation is missing.

Do not upgrade a status because the work feels close. Status follows evidence.

## Stop conditions

Stop immediately if an adaptation introduces:

- live runtime execution not explicitly reviewed
- provider calls not explicitly reviewed
- secrets or wallet access
- daemon, watcher, background service, or hidden process
- autonomous action authority
- trading, order routing, leverage, or portfolio authority
- memory or ledger writes not explicitly reviewed
- publication, sales, or client-contact claims not explicitly approved
- any wording that turns documentation into permission

## Current publication status

Current pack status: public V0 GitHub release.

The source closeout statuses preserved inside some SOPs are historical provenance. They do not override the current repository status and do not grant operational authority.

No PDF, sale channel, runtime, provider integration, or external announcement is implied by this file.

## Minimal use path

If you only need one reusable artifact, start with:

- `content/04_agent_handoff_format.md`
- `templates/agent_handoff_template.md`

If you need PR merge discipline, read:

- `content/02_pr_final_audit_head_guard_sop.md`
- `templates/pr_final_audit_checklist.md`

If you are recovering from a crash during a PR / merge gate, read:

- `content/01_oom_recovery_sop.md`
- `templates/oom_recovery_checklist.md`

If you need local cold-start structure, read:

- `content/03_cold_start_operator_runbook.md`
- `templates/cold_start_checklist.md`

If you are evaluating the original ASSO-derived operating style, read the full pack in order.
