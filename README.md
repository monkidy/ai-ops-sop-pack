# AI Ops SOP Pack

"AI Ops SOP Pack" by Hichem Benali, licensed under [CC BY 4.0](./LICENSE). Source: https://github.com/monkidy/ai-ops-sop-pack.

> **Status: V0 — public GitHub publication; no packaged release or PDF yet**
>
> Human review has passed. This repository is now public as the canonical GitHub publication of AI Ops SOP Pack v0.
>
> No PDF, packaged release, sale channel, or external announcement has been opened yet.

## What this pack is

A consolidated, externally-readable bundle of Standard Operating Procedures (SOPs) for teams that operate AI agents in production: incident response, PR audit discipline, cold-start procedures, agent handoff format, and operator guides.

The pack is a **documentation pack**, not a runtime, not a tool, not a service.

## Intended audience

AI Ops / Platform / SRE teams running AI agents in production who need bounded operating procedures for:

- recovering from out-of-memory crashes during a PR / merge gate
- auditing pull requests with strict head-guard discipline before merge
- bringing a workstation back online after cold start without re-engaging long contexts
- exchanging bounded handoffs between agents under explicit decision values
- running text-only avatar smoke tests locally without any live runtime

## Pack contents

The pack lives in `content/`. See `content/_INDEX.md` for the consolidated audit index with per-file provenance, sizes, and review-tag history. See `source_pr_references.md` for the per-file PR-to-source mapping.

| File | Purpose |
|------|---------|
| `content/01_oom_recovery_sop.md` | OOM Recovery SOP v0 — cold reprise procedure after OOM during a PR/merge gate |
| `content/02_pr_final_audit_head_guard_sop.md` | PR Final Audit + Head Guard SOP v0 — bounded merge procedure with head-guard discipline |
| `content/03_cold_start_operator_runbook.md` | Cold-Start Operator Runbook v0 — workstation product index + entry points |
| `content/04_agent_handoff_format.md` | Agent Handoff Format v0 — minimum handoff structure + allowed decision values |
| `content/05_operator_guide.md` | Operator Guide — Avatar Text-Only Stack v0 — local non-live operator path for text-only avatar |

## How to use

Each file is self-contained Markdown. Read the consolidated SOPs and adapt the procedures to your environment. Keep the boundaries that the SOPs declare (no live, no provider, no runtime authority): they are part of the design discipline, not optional extras.

The "Trace de cycle ACE" appendix at the end of files 01 and 02 documents the production method (add → review → closeout → arbitration). It is informational and helps readers see how the SOP was hardened, not a procedure to imitate verbatim.

## Status

- **Version** : V0
- **Human review** : PASS
- **Publication** : PUBLIC_GITHUB_REPOSITORY
- **Public visibility** : PUBLIC
- **PDF** : NOT_GENERATED
- **Tag** : v0.0.0
- **GitHub Release** : NOT_CREATED
- **Sale** : NOT_OPENED
- **Latest mission** : 5c.3.m public GitHub publication, no PDF, no announcement
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

The pack is published in this public GitHub repository as its canonical source. No GitHub Release has been cut, no PDF has been compiled, and no commercial channel has been opened. The author has frozen any external announcement for a 14-day post-publication observation window.

## Next steps

- ~~Human review pass.~~ **DONE** — human review status: PASS.
- ~~Public GitHub repository.~~ **DONE** — this repository, public, tag `v0.0.0`.
- ~~Tag `v0.0.0`.~~ **DONE** — pushed to this repository.
- **NOT CREATED** — GitHub Release. Reserved for a later pass; not authorized in this publication step.
- **OPTIONAL / NOT GENERATED** — PDF compilation. May be added later as a release asset or in a dedicated follow-up; intentionally not produced in this pass.
- **FROZEN for 14 days after publication** — external announcement (LinkedIn, X, Reddit, Show HN, personal channels). The author will observe passively before any communication step.

This V0 publication is intentionally sober: a public canonical repository under CC BY 4.0, nothing more. Any release packaging, PDF distribution, sale channel, or announcement will be a separate, explicit pass.
