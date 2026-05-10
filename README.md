# AI Ops SOP Pack

"AI Ops SOP Pack" by Hichem Benali, licensed under [CC BY 4.0](./LICENSE).

> **Statut : DRAFT — pre-publication human review pending**
>
> All 11 review markers from prior consolidation passes have been resolved. The official CC BY 4.0 license text has been bundled in `LICENSE` (mission 5c.3.h). One step remains before the pack can be released externally:
>
> - a final human review pass (and optional PDF compilation) must confirm publication-readiness end-to-end
>
> Until this step is complete, this pack is DRAFT. The LICENSE is now the official CC BY 4.0 text; the pack is not yet published.

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

- **Version** : V0 (DRAFT)
- **Latest mission** : 5c.3.h official CC BY 4.0 license text bundling
- **Review markers** : 0 remaining (`<<<REVIEW_HICHEM_5c3b>>>` count is zero across `content/*.md`; verified by `scripts/sop_pack_content_integrity_check.py --max-review 0`)
- **License** : CC BY 4.0 per `EXTRACT_SOP_PACK_SCOPE.md` §5. The official CC BY 4.0 legal text has been bundled into `LICENSE` (mission 5c.3.h — fetched verbatim from `creativecommons.org/licenses/by/4.0/legalcode.txt`). No placeholder remains.
- **Source mapping** : present at `source_pr_references.md` (per-file PR-to-source mapping for traceability).
- **PDF** : not produced in this pass. Optional follow-up depending on distribution channel.

## What this pack is not

- Not a product. Not an offer. Not a sales asset.
- Not a runtime. Not a tool. Not a service.
- Not production-ready. Not certified. Not warrantied.
- Not a claim of operational authority over your environment.
- Not a permission-to-act, permission-to-trade, or permission-to-publish on your behalf.

The pack carries no warranty of any kind. Procedures are described for operational reference; any adoption is at the reader's responsibility.

## License and DRAFT notice

The official CC BY 4.0 legal text is now bundled in `LICENSE` as of mission 5c.3.h. The attribution for redistribution is:

> "AI Ops SOP Pack" by Hichem Benali, licensed under CC BY 4.0. Source: \<URL of the publication repository, to be fixed at publication time\>.

The pack remains **DRAFT** pending a final human review pass. Do not publish, sell, or redistribute as a finalized artifact until the maintainer's final review is complete.

## Next steps before publication

1. ~~Bundle official CC BY 4.0 license text.~~ **DONE (5c.3.h)** — official text fetched verbatim from `creativecommons.org/licenses/by/4.0/legalcode.txt` and written to `LICENSE`.
2. A final human review pass confirms publication-readiness end-to-end (re-runs the integrity checker, validates the LICENSE text, validates `source_pr_references.md`, optionally produces a PDF compilation).
3. The maintainer publishes the pack under the chosen distribution channel (per `EXTRACT_SOP_PACK_SCOPE.md` §6.2 options).

This DRAFT is pending the final human review pass (step 2) before any publication.
