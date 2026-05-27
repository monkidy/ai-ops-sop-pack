# AI Ops SOP Pack

"AI Ops SOP Pack" by Hichem Benali, licensed under [CC BY 4.0](./LICENSE). Source: https://github.com/monkidy/ai-ops-sop-pack.

> **Status: V0.1 — public GitHub documentation release; GitHub Release v0.1.1 published**
>
> Human review has passed. This repository is public as the canonical GitHub publication of AI Ops SOP Pack.
>
> GitHub Release v0.1.1 is published as a documentation visibility and status alignment release. No PDF, sale channel, runtime, provider integration, or external announcement has been opened.

## What this pack is

A consolidated, externally-readable bundle of Standard Operating Procedures (SOPs) for teams documenting and reviewing AI-assisted engineering work: PR audit discipline, cold recovery procedures, agent handoff format, and operator guides.

The pack is a **documentation pack**, not a runtime, not a tool, not a service.

## Use this when

Use this pack when your team needs to reduce:

- false readiness claims after AI-assisted work
- weak PR handoffs
- unsafe merge assumptions
- context-loss recovery risk after editor or workstation crashes
- confusion between evidence, review, approval, and permission-to-act

If you only read one file first, read [`content/04_agent_handoff_format.md`](./content/04_agent_handoff_format.md).

## Intended audience

AI Ops / Platform / SRE / engineering teams documenting or reviewing AI-assisted engineering work who need bounded operating procedures for:

- human-led cold recovery after editor or workstation crashes during PR / merge review
- auditing pull requests with strict head-guard discipline before merge
- bringing a workstation back online after cold start without re-engaging long contexts
- exchanging bounded handoffs between agents or operators under explicit decision values
- reviewing local text-only operator paths without any live runtime

## Pack contents

Start with [`START_HERE.md`](./START_HERE.md) for the external reading guide, recommended reading order, portability notes, and adaptation boundaries.

The pack lives in `content/`. See `content/_INDEX.md` for the consolidated audit index with per-file provenance, sizes, and review-tag history. See `source_pr_references.md` for the per-file PR-to-source mapping.

| File | Purpose |
|------|---------|
| `content/01_oom_recovery_sop.md` | OOM Recovery SOP v0 — human-led cold recovery after OOM during a PR/merge gate |
| `content/02_pr_final_audit_head_guard_sop.md` | PR Final Audit + Head Guard SOP v0 — bounded merge review procedure with head-guard discipline |
| `content/03_cold_start_operator_runbook.md` | Cold-Start Operator Runbook v0 — workstation product index + entry points |
| `content/04_agent_handoff_format.md` | Agent Handoff Format v0 — minimum handoff structure + allowed decision values |
| `content/05_operator_guide.md` | Operator Guide — Avatar Text-Only Stack v0 — ASSO-derived local text-only case study, not a generic drop-in SOP |

## Templates

Copyable templates live in `templates/`:

| File | Purpose |
|------|---------|
| `templates/agent_handoff_template.md` | Blank handoff structure for bounded operator / agent transfer |
| `templates/pr_final_audit_checklist.md` | Blank checklist for final PR audit and head-guard review |
| `templates/oom_recovery_checklist.md` | Blank checklist for cold recovery after OOM / editor crash |
| `templates/cold_start_checklist.md` | Blank checklist for local workstation cold start |

Templates are documentation aids only. They do not grant approval, merge authority, runtime authority, or permission-to-act.

## Examples

Filled examples live in `examples/`:

| File | Purpose |
|------|---------|
| `examples/pr_crash_recovery_filled_example.md` | Fictitious non-live walkthrough combining OOM recovery, PR final audit, and agent handoff |

Examples are illustrative only. They do not prove production readiness and should not be copied without replacing all evidence with observations from your own environment.

## Release notes

See [`CHANGELOG.md`](./CHANGELOG.md) for public documentation-pack changes.

Release notes for v0.1.1 live in [`release_notes/v0.1.1.md`](./release_notes/v0.1.1.md). Release notes for v0.1.0 remain available in [`release_notes/v0.1.0.md`](./release_notes/v0.1.0.md).

## How to use

Each file is self-contained Markdown. Read `START_HERE.md` first, then read the consolidated SOPs and adapt the procedures to your environment. Keep the boundaries that the SOPs declare (no live, no provider, no runtime authority): they are part of the design discipline, not optional extras.

For operational use, read the relevant SOP first, then copy the corresponding blank template from `templates/` and fill it with observed evidence from your own environment. Use `examples/` only to understand how the pieces can fit together; do not treat examples as authority.

The "Trace de cycle ACE" appendix at the end of files 01 and 02 documents the production method (add → review → closeout → arbitration). It is informational and helps readers see how the SOP was hardened, not a procedure to imitate verbatim.

## Status

- **Version** : V0.1
- **Human review** : PASS
- **Publication** : PUBLIC_GITHUB_REPOSITORY
- **Public visibility** : PUBLIC
- **PDF** : NOT_GENERATED
- **Latest tag** : v0.1.1
- **Latest GitHub Release** : PUBLISHED — v0.1.1
- **Previous tag** : v0.1.0
- **Previous GitHub Release** : PUBLISHED — v0.1.0
- **Initial tag** : v0.0.0
- **Initial GitHub Release** : PUBLISHED — v0.0.0
- **Sale** : NOT_OPENED
- **Latest mission** : v0.1.1 documentation visibility and status alignment release published; no PDF, no sale channel, no runtime, no provider integration, no external announcement.
- **Review markers** : 0 remaining (`<<<REVIEW_HICHEM_5c3b>>>` count is zero across `content/*.md`; verified by the integrity checker `scripts/sop_pack_content_integrity_check.py --max-review 0` on the source repository)
- **License** : CC BY 4.0. The official CC BY 4.0 legal text is bundled in `LICENSE` (fetched verbatim from `creativecommons.org/licenses/by/4.0/legalcode.txt`). No placeholder remains.
- **Source mapping** : present at `source_pr_references.md` (per-file PR-to-source mapping for traceability).

## What this pack is not

- Not a product. Not an offer. Not a sales asset.
- Not a runtime. Not a tool. Not a service.
- Not production-ready. Not certified. Not warrantied.
- Not a claim of operational authority over your environment.
- Not a permission-to-act, permission-to-trade, or permission-to-publish on your behalf.

The pack carries no warranty of any kind. Procedures are described for operational reference; any adoption is at the reader's responsibility.

## License and attribution

The official CC BY 4.0 legal text is bundled in `LICENSE`. The attribution for redistribution is:

> "AI Ops SOP Pack" by Hichem Benali, licensed under CC BY 4.0. Source: https://github.com/monkidy/ai-ops-sop-pack.

The pack is published in this public GitHub repository as its canonical source. GitHub Releases v0.0.0, v0.1.0, and v0.1.1 have been published. No PDF has been compiled, and no commercial channel has been opened. External announcement is not automatic and remains a separate explicit decision.

## Next steps

- ~~Human review pass.~~ **DONE** — human review status: PASS.
- ~~Public GitHub repository.~~ **DONE** — this repository, public.
- ~~Tag `v0.0.0`.~~ **DONE** — pushed to this repository.
- ~~GitHub Release v0.0.0.~~ **DONE** — published.
- ~~Usability polish.~~ **DONE** — START_HERE, templates, filled example, case-study guidance, changelog, and v0.1.0 release notes.
- ~~Tag `v0.1.0`.~~ **DONE** — pushed to this repository.
- ~~GitHub Release v0.1.0.~~ **DONE** — published.
- ~~GitHub Release v0.1.1.~~ **DONE** — documentation visibility and status alignment release published.
- **OPTIONAL / NOT GENERATED** — PDF compilation. May be added later as a release asset or in a dedicated follow-up; intentionally not produced in this pass.
- **OBSERVATION ONLY** — external visibility is not automatic. Any announcement, distribution, or commercial use remains a separate explicit pass.

This V0.1 publication is intentionally sober: a public canonical Markdown documentation repository under CC BY 4.0, nothing more. Any PDF distribution, sale channel, or broader announcement will be a separate, explicit pass.
