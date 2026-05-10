# Source PR references — AI Ops SOP Pack

This document maps each consolidated file in `content/` to the source pull requests on `monkidy/asso-execution-bridge` that produced its raw material, and records the consolidation type applied.

It serves as the traceability surface for the pack. It is not itself part of the operational SOPs.

---

## Per-file mapping

### `content/01_oom_recovery_sop.md`

- **Consolidation type** : 3B (cycle SOP — closeout body + Trace de cycle ACE appendix)
- **Source PRs** :
  - **PR #81** — Capital Engine: add OOM recovery SOP v0 (merged 2026-05-01)
  - **PR #82** — Capital Engine: review OOM recovery SOP v0 (merged 2026-05-01)
  - **PR #83** — Capital Engine: closeout OOM recovery SOP v0 (merged 2026-05-01)
- **Source files on `main`** :
  - `docs/capital_engine/documentation_operatoire_oom_recovery_sop_v0.md` (PR #81)
  - `docs/capital_engine/documentation_operatoire_oom_recovery_sop_v0_review.md` (PR #82)
  - `docs/capital_engine/documentation_operatoire_oom_recovery_sop_v0_closeout.md` (PR #83)
- **Notes** : closeout content used as body of the consolidated file; `add` and `review` summarized in the « Trace de cycle ACE » appendix.

### `content/02_pr_final_audit_head_guard_sop.md`

- **Consolidation type** : 3B + arbitration (cycle SOP with internal model arbitration)
- **Source PRs** :
  - **PR #87** — Capital Engine: add PR final audit head guard SOP v0 (merged 2026-05-01)
  - **PR #88** — Capital Engine: review PR final audit head guard SOP v0 (merged 2026-05-01)
  - **PR #89** — Capital Engine: closeout PR final audit head guard SOP v0 (merged 2026-05-01)
  - **PR #90** — Capital Engine: arbitrate PR final audit head guard SOP v0 internal model (merged 2026-05-01)
- **Source files on `main`** :
  - `docs/capital_engine/documentation_operatoire_pr_final_audit_and_head_guard_sop_v0.md` (PR #87)
  - `docs/capital_engine/documentation_operatoire_pr_final_audit_and_head_guard_sop_v0_review.md` (PR #88)
  - `docs/capital_engine/documentation_operatoire_pr_final_audit_and_head_guard_sop_v0_closeout.md` (PR #89)
  - `docs/capital_engine/documentation_operatoire_pr_final_audit_and_head_guard_sop_v0_internal_model_arbitration.md` (PR #90)
- **Notes** : closeout body + 4-step Trace de cycle ACE appendix (add → review → closeout → internal_model_arbitration).

### `content/03_cold_start_operator_runbook.md`

- **Consolidation type** : single source merge (#143), with workstation README absorbed as contextual preamble
- **Source PR** :
  - **PR #143** — docs(workstation): add cold-start operator runbook index v0 (merged 2026-05-07)
- **Source files on `main`** :
  - `docs/product/asso_workstation/asso_workstation_cold_start_operator_runbook_v0.md` (PR #143) — body
  - `docs/product/asso_workstation/README.md` (PR #143) — absorbed as `## Contexte Workstation` preamble
- **Notes** : single source PR; the runbook body is the canonical content; the workstation README provided the product-index preamble.

### `content/04_agent_handoff_format.md`

- **Consolidation type** : single source (no consolidation)
- **Source PR** :
  - **PR #27** — AGENT_HANDOFF_REMOTE_COMMIT_READY_BOUNDARY_REPAIR (merged 2026-04-29)
- **Source file on `main`** :
  - `docs/asso_runtime/asso_agent_handoff_contract.md` (PR #27)
- **Notes** : the H1 was aligned to the pack frontmatter title (`Agent Handoff Format v0`) in mission 5c.3.c; the original source file uses the noun « Contract » which describes the same artifact.

### `content/05_operator_guide.md`

- **Consolidation type** : 4A (3-file fusion — Avatar Text-Only Stack)
- **Source PR** :
  - **PR #31** — AVATAR_TEXT_ONLY_V0_OPERATOR_GUIDE_AND_SINGLE_RUNNER (merged 2026-04-29)
- **Source files on `main`** :
  - `docs/asso_runtime/avatar/asso_avatar_text_only_v0_finish.md` (PR #31)
  - `docs/asso_runtime/avatar/asso_avatar_text_only_v0_operator_guide.md` (PR #31)
  - `docs/asso_runtime/avatar/asso_avatar_text_only_v0_usage.md` (PR #31)
- **Notes** : three source files fused into a single consolidated file with three head sections (Usage, Operator Guide, Finish). « Sourced from PR #31 (finish + operator_guide + usage) » footer present in the consolidated file.

---

## Note on `content_raw/`

The `content_raw/` directory present on this branch is **internal traceability material**. It contains the raw filtered copies of the source files (mission 5c.2) before the consolidation passes (3B / 4A / 3A / 4B / 5c.3.c repairs / 5c.3.d alignment).

**`content_raw/` is not destined for publication.** It is kept on this branch only as audit material to allow reviewers to trace each consolidated paragraph back to its raw source. When the pack is published externally, only the following are intended for distribution:

- `README.md` (root)
- `LICENSE` (root)
- `source_pr_references.md` (root, this file)
- `content/01_oom_recovery_sop.md`
- `content/02_pr_final_audit_head_guard_sop.md`
- `content/03_cold_start_operator_runbook.md`
- `content/04_agent_handoff_format.md`
- `content/05_operator_guide.md`
- `content/_INDEX.md` *(audit index — distribution-or-not to be confirmed by maintainer)*

The branch's other artifacts (`content_raw/`, `EXTRACT_SOP_PACK_SCOPE.md`, `docs/project_evidence/`, `docs/project_checkpoints/`, `scripts/sop_pack_content_integrity_check.py`) are repository-internal. They do not travel with a published distribution.

---

## Cluster context

The pack consolidates cluster K01 « AI Ops SOP Pack » as defined in `EXTRACTION_INVENTORY.md` §2.4 and §4.1, and scoped in `EXTRACT_SOP_PACK_SCOPE.md`. The scope §1.4 lists 23 cluster-K01 files explicitly **excluded** from this pack (10 project_checkpoints, 10 internal CI/lint checkers, 1 README_RUN.md, 2 ex-ambiguous scripts). The mapping above lists only the **13 source files** that were retained per scope §1.3 and folded into the **5 consolidated files** per scope §3.3.

---

## Verification

To verify this mapping against the repo, the canonical references are:

- `EXTRACT_SOP_PACK_SCOPE.md` §1.2 (PR list) and §1.3 (source file list)
- `content_raw/_INDEX.md` (raw copies, mission 5c.2, with per-file P1/P2/P3/P4 counts)
- `content/_INDEX.md` (consolidated index, missions 5c.3 / 5c.3.b / 5c.3.c / 5c.3.d)
- The HTML provenance comment at the top of each `content/*.md` file (`SOURCE_PRS:`, `CONSOLIDATION_TYPE:`, `SOURCE_FILES:` fields)
